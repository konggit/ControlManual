# 主机指令介绍

## 中控指令数据结构

一个WORD 字节，低字节先发,以下所有的数字都是16进制,CRC 可以设置关闭，发送00 00
<table border="1"  cellspacing="1" cellpadding="1" align="left">                    
<tr>
<td>BYTE1</td>
<td>BYTE2</td>
<td>BYTE3</td>
<td>BYTE4</td>
<td>BYTE5</td>
<td>BYTE6</td>
<td>BYTE7</td>
<td>BYTE8</td>
<td>BYTE9</td>
<td>BYTE10</td>
<td>BYTE11</td>
<td>...</td>
</tr>
<tr>
<td colspan= "2">BeginID</td>
<td colspan= "5">Header</td>
<td colspan= "5">Playload</td>
</tr>
<tr>
<td colspan= "2">ID</td>
<td colspan= "1">eType</td>
<td colspan= "2">wPayloadSize</td>
<td colspan= "2">wCRC</td>
</tr>
<tr>
<td >BE</td>
<td >EF</td>
<td >XX</span></td>
<td colspan= "1">LowByte</td>
<td colspan= "1">HighByte</td>
<td colspan= "1">LowByte</td>
<td colspan= "1">HighByte</td>
<td colspan= "1">DATA1</td>
<td colspan= "1">DATA2</td>
<td colspan= "1">DATA3</td>
<td colspan= "1">DATA4</td>
<td >...</td>
</tr>
</table>

## 指令说明

提示：一个WORD 字节，低字节先发,以下所有的数字都是16进制,CRC 可以设置关闭，发送00 00
COM 值选择 0:IP,1:RS485,2:RS422,3:COM1,4:COM2,5:COM3,6:COM4,7:COM5,8:COM6,9:CAN
COMs 值选择 bit0:IP,bit1:RS485,bit2:RS422,bit3:COM1,bit4:COM2,bit5:COM3,bit6:COM4,bit7:COM5,bit8:COM6,bit9:CAN
RS422 Mode 0: RS232,1:RS485;2:RS422
cFlag Bit7: 1 Enable;Bit6~0: 0：单次,1:每日,2:每周,4:每月，8：每年,10:每小时,20 每分钟,40 间隔


<table border="1"  cellspacing="1" cellpadding="1" align="left">                    
<tr>
<td>包类型</td>
<td>BYTE1</td>
<td>BYTE2</td>
<td>BYTE3</td>
<td>BYTE4</td>
<td>BYTE5</td>
<td>BYTE6</td>
<td>BYTE7</td>
<td>BYTE8</td>
<td>BYTE9</td>
<td>BYTE10</td>
<td>BYTE11</td>
<td>BYTE12</td>
<td>BYTE13</td>
<td>BYTE14</td>
<td>BYTE15</td>
<td>BYTE16</td>
<td>BYTE17</td>
<td>BYTE18</td>
<td>BYTE19</td>
<td>BYTE20</td>
<td>BYTE21</td>
<td>BYTE22</td>
<td>BYTE23</td>
<td>BYTE24</td>
<td>BYTE25</td>
<td>BYTE26</td>
<td>BYTE27</td>
<td>BYTE28</td>
<td>BYTE29</td>
<td>BYTE30</td>
<td>...</td>
</tr>
<tr>
<td>设置RS422端口模式</td>
<td>BE</td>
<td>EF</td>
<td>0D</td>
<td>02</td>
<td>00</td>
<td>00</td>
<td>00</td>
<td>02</td>
<td>RS422 Mode</td>
</tr>
<tr>
<td>读取RS422端口模式</td>
<td>BE</td>
<td>EF</td>
<td>0E</td>
<td>01</td>
<td>00</td>
<td>00</td>
<td>00</td>
<td>02</td>
</tr>
<tr>
<td>设置波特率</td>
<td>BE</td>
<td>EF</td>
<td>0F</td>
<td>07</td>
<td>00</td>
<td>00</td>
<td>00</td>
<td>COM</td>
<td colspan= "4">dwBraund</td>
<td>cDataBits</td>
<td>cParity</td>
<td>cStopBits</td>
</tr>
<tr>
<td>读取波特率</td>
<td>BE</td>
<td>EF</td>
<td>10</td>
<td>01</td>
<td>00</td>
<td>00</td>
<td>00</td>
<td>COM 1~8</td>
</tr>
<tr>
<td>串口数据间隔设置</td>
<td>BE</td>
<td>EF</td>
<td>12</td>
<td>03</td>
<td>00</td>
<td>00</td>
<td>00</td>
<td>COM</td>
<td colspan= "2">wTime</td>
</tr>

<tr>
<td>IP 地址设置</td>
<td>BE</td>
<td>EF</td>
<td>13</td>
<td>15</td>
<td>00</td>
<td>00</td>
<td>00</td>
<td>00</td>
<td colspan= "4">Wan IP</td>
<td colspan= "4">Wan Mask</td>
<td colspan= "4">GateIP</td>
<td colspan= "4">Lan IP</td>
<td colspan= "4">Lan Mask</td>
</tr>
<tr>
<td>蜂鸣器设置</td>
<td>BE</td>
<td>EF</td>
<td>14</td>
<td>01</td>
<td>00</td>
<td>00</td>
<td>00</td>
<td>ON 0/OFF 1</td>

</tr>
<tr>
<td>红外学习</td>
<td>BE</td>
<td>EF</td>
<td>18</td>
<td>01</td>
<td>00</td>
<td>00</td>
<td>00</td>
<td>IR Number 1~16</td>
</tr>
<tr>
<td>红外发送</td>
<td>BE</td>
<td>EF</td>
<td>19</td>
<td>02</td>
<td>00</td>
<td>00</td>
<td>00</td>
<td>IR Port 1~8</td>
<td>IR Number 1~16</td>
</tr>
<tr>
<td>数据单端口转发</td>
<td>BE</td>
<td>EF</td>
<td>54</td>
<td>xx</td>
<td>xx</td>
<td>00</td>
<td>00</td>
<td>COM</td>
<td>Data1</td>
<td>Data2</td>
<td>...</td>
</tr>
<tr>
<td>数据多端口转发</td>
<td>BE</td>
<td>EF</td>
<td>55</td>
<td>xx</td>
<td>xx</td>
<td>00</td>
<td>00</td>
<td colspan= "2">COMs</td>
<td>Data1</td>
<td>Data2</td>
<td>...</td>
</tr>
<tr>
<td>单个继电器设置</td>
<td>BE</td>
<td>EF</td>
<td>56</td>
<td>02</td>
<td>00</td>
<td>00</td>
<td>00</td>
<td>Rly Port 1~8</td>
<td>OPEN 0/CLOSE 1</td>
</tr>
<tr>
<td>多个继电器设置</td>
<td>BE</td>
<td>EF</td>
<td>57</td>
<td>02</td>
<td>00</td>
<td>00</td>
<td>00</td>
<td>Rly bits port</td>
<td>OPEN 0/CLOSE 1</td>
</tr>
<tr>
<td>读取数字输入</td>
<td>BE</td>
<td>EF</td>
<td>58</td>
<td>01</td>
<td>00</td>
<td>00</td>
<td>00</td>
<td>DI port 1~8</td>

</tr>
<tr>
<td>事件表设置</td>
<td>BE</td>
<td>EF</td>
<td>59</td>
<td>06</td>
<td>00</td>
<td>00</td>
<td>00</td>
<td>TableIndex 1~255</td>
<td>EventSource</td>
<td>EventType</td>
<td>EventParam</td>
<td colspan= "2">wDelays</td>
</tr>
<tr>
<td>设置预置命令</td>
<td>BE</td>
<td>EF</td>
<td>5B</td>
<td>xx</td>
<td>xx</td>
<td>00</td>
<td>00</td>
<td>cIndex 1~32</td>
<td>ASCII 0:/HEX 1</td>
<td>Datas 1~127</td>
</tr>
<tr>
<td>读取命令设置</td>
<td>BE</td>
<td>EF</td>
<td>5C</td>
<td>01</td>
<td>00</td>
<td>00</td>
<td>00</td>
<td>cIndex 1~32</td>
</tr>
<tr>
<td>发送预置命令到某个端口</td>
<td>BE</td>
<td>EF</td>
<td>5D</td>
<td>02</td>
<td>00</td>
<td>00</td>
<td>00</td>
<td>COM</td>
<td>cIndex 1~32</td>
</tr>
<tr>
<td>设置用户命令</td>
<td>BE</td>
<td>EF</td>
<td>5E</td>
<td>xx</td>
<td>xx</td>
<td>00</td>
<td>00</td>
<td>cIndex 1~64</td>
<td>ASCII 0:/HEX 1</td>
<td>Datas 1~30</td>
</tr>
<tr>
<td>读取用户命令</td>
<td>BE</td>
<td>EF</td>
<td>5F</td>
<td>01</td>
<td>00</td>
<td>00</td>
<td>00</td>
<td>cIndex 1~64</td>
</tr>
<tr>
<td>定时器设置</td>
<td>BE</td>
<td>EF</td>
<td>62</td>
<td>08</td>
<td>00</td>
<td>00</td>
<td>00</td>
<td>cIndex 1~8</td>
<td>cFlag</td>
<td colspan= "2">wYear</td>
<td>cMonth</td>
<td>cDay</td>
<td>cMin</td>
<td>cSec</td>
</tr>
<tr>
<td>定时器使能设置</td>
<td>BE</td>
<td>EF</td>
<td>64</td>
<td>02</td>
<td>00</td>
<td>00</td>
<td>00</td>
<td>cIndex 1~8</td>
<td>Enable 0/Disable 1</td>
</tr>
<tr>
<td>设置CAN波特率</td>
<td>BE</td>
<td>EF</td>
<td>64</td>
<td>04</td>
<td>00</td>
<td>00</td>
<td>00</td>
<td colspan= "4">dwBaud</td>
</tr>
<tr>
<td>读取CAN波特率</td>
<td>BE</td>
<td>EF</td>
<td>65</td>
<td>00</td>
<td>00</td>
<td>00</td>
<td>00</td>
</tr>
<tr>
<td>设置CAN滤波器</td>
<td>BE</td>
<td>EF</td>
<td>67</td>
<td>00</td>
<td>0A</td>
<td>00</td>
<td>00</td>
<td>cFilterID 0~12</td>
<td>MaskMode 0/List Mode 1</td>
<td colspan= "4">dwFilterID</td>
<td colspan= "4">dwFilterMask</td>
   
</tr>
<tr>
<td>读取CAN滤波器</td>
<td>BE</td>
<td>EF</td>
<td>68</td>
<td>01</td>
<td>00</td>
<td>00</td>
<td>00</td>
<td>cFilterID 0~12</td>
</tr>
<tr>
<td>读取CAN滤波器</td>
<td>BE</td>
<td>EF</td>
<td>69</td>
<td>00</td>
<td>00</td>
<td>00</td>
<td>00</td>
</tr>
</table>
