# 主机介绍

&emsp;&emsp;**C2 中控**使用无需编程概念，完成串口、红外、继电器、IO通道工作。  

- 主机内置2路网络模块接口，可根据实际情况调整为TCP server（默认）、UDP client。  
- 内置5路RS232[C21 主机带13路串口]/ 1 路RS485可选端口/ 1路RS422/RS485/RS232 可配接口。  
- 内置8路IR 发送。  
- 内置8路继电器弱电控制。  
- 内置8路数字输入信号。  
- 轻松实现自定义命令，定时器控制，红外学习。  

## 整体接口布局

<table border="1">
<tr>  
<td  > </td>
<td  > </td>
<td >扩展接口5</td>
<td >扩展接口6</td>

</tr>
<tr> 
<td>WAN 口</td>
<td>LAN 口</td>
<td>接口1</td>
<td>接口2</td>
<td>接口3</td>
<td>接口4</td>
<td>接口5</td>
<td>电源12V</td>
</tr>
</table>

## 主机接口1

<table border="1">
<tr>                      
<td colspan= "3" >COM3</td>
<td colspan= "3" >COM4</td>
<td colspan= "3" >COM5</td>
<td colspan= "3" >COM6</td>
</tr>
<tr> 
<td>RS232_TX</td>
<td>RS232_RX</td>
<td>AGND</td>
<td>RS232_TX</td>
<td>RS232_RX</td>
<td>AGND</td>
<td>RS232_TX</td>
<td>RS232_RX</td>
<td>AGND</td>
<td>RS232_TX</td>
<td>RS232_RX</td>
<td>AGND</td>
</tr>
<tr> 
<td>CAN_L</td>
<td>CAN_H</td>
<td>AGND</td>
<td>RS485_B</td>
<td>RS485_A</td>
<td>GND</td>
<td>RS422_TX+<br>RS485_A+</td>
<td>RS422_TX-<br>RS485_B-<br>RS232_TX</td>
<td>RS422_RX+<br>RS232_RX</td>
<td>RS422_RX-</td>
<td>AGND</td>
<td>AGND</td>
</tr>
<tr>
<td colspan= "3" >CAN</td>
<td colspan= "3" >RS485</td>
<td colspan= "6" >RS422</td>
</tr>
</table>

- TX 表示 数据数据有中控发出,RX 表示数据输入到中控  
- 一般 TX 连接 9 针母串口(DB9) 的第2脚；RX 连接 9 针母串口(DB9) 的第3脚;AGND 连接 9 针串口(DB9) 的第5脚  

|中控|DB9母座|   |电脑DB9公座|数据方向|  
|:------:|-----|----|----|-----|
| TX  | 2 |---->| 2 | 中控到电脑|
| RX  | 3 |<----| 3 | 电脑到中控|  

## 主机接口2

<table border="1">
<tr>                        
<td colspan= "2" class="center-text" >IR1</td>
<td colspan= "2" class="center-text" >IR2</td>
<td colspan= "2" class="center-text" >IR3</td>
<td colspan= "2" class="center-text" >IR4</td>
<td colspan= "2" class="center-text" >IR5</td>
<td colspan= "2" class="center-text" >IR6</td>                        
</tr>
<tr>
<td>IR1</td>
<td>AGND</td>
<td>IR2</td>
<td>AGND</td>
<td>IR3</td>
<td>AGND</td>
<td>IR4</td>
<td>AGND</td>
<td>IR5</td>
<td>AGND</td>
<td>IR6</td>
<td>AGND</td>
</tr>
<tr>
<td>RS232_TX</td>
<td>RS232_RX</td>
<td>AGND</td>
<td>RS232_TX</td>
<td>RS232_RX</td>
<td>AGND</td>
<td>AGND</td>
<td>AGND</td>
<td>AGND</td>
<td>IR7</td>
<td>IR8</td>
<td>AGND</td>
</tr>
<tr>
<td colspan= "3" class="center-text">COM7</td>
<td colspan= "3" class="center-text">COM8</td>
<td colspan= "4" class="center-text">IR7</td>
<td colspan= "2" class="center-text">IR8</td>
</tr>
</table>

## 主机接口3

<table border="1">
<tr>
<td colspan= "3" class="center-text" >DI5</td>
<td colspan= "3" class="center-text">DI6</td>
<td colspan= "3" class="center-text">DI7</td>
<td colspan= "3" class="center-text">DI8</td>
</tr>
<tr>
<td>12V</td>
<td>DI5+</td>
<td>DI5-</td>
<td>12V</td>
<td>DI6+</td>
<td>DI6-</td>
<td>AGND</td>
<td>DI7+</td>
<td>DI7-</td>
<td>AGND</td>
<td>DI8+</td>
<td>DI8-</td>
</tr>
<tr>
<td>12V</td>
<td>DI1+</td>
<td>DI1-</td>
<td>12V</td>
<td>DI2+</td>
<td>DI2-</td>
<td>AGND</td>
<td>DI3+</td>
<td>DI3-</td>
<td>AGND-</td>
<td>DI4+</td>
<td>DI4-</td>
</tr>
<tr>
<td colspan= "3" class="center-text">DI1</td>
<td colspan= "3" class="center-text">DI2</td>
<td colspan= "3" class="center-text">DI3</td>
<td colspan= "4" class="center-text">DI4</td>
</tr>
</table>

## 主机接口4  

<table border="1">
<tr>
<td colspan= "3" class="center-text">Relay5</td>
<td colspan= "3" class="center-text">Relay6</td>
<td colspan= "3" class="center-text">Relay7</td>
<td colspan= "3" class="center-text">Relay8</td>
</tr>
<tr>
<td>Relay5_A</td>
<td>Relay5_B</td>
<td>AGND</td>
<td>Relay6_A</td>
<td>Relay6_B</td>
<td>AGND</td>
<td>Relay7_A</td>
<td>Relay7_B</td>
<td>AGND</td>
<td>Relay8_A</td>
<td>Relay8_B</td>
<td>AGND</td>
</tr>
<tr>
<td>Relay1_A</td>
<td>Relay1_B</td>
<td>AGND</td>
<td>Relay2_A</td>
<td>Relay2_B</td>
<td>AGND</td>
<td>Relay3_A</td>
<td>Relay3_B</td>
<td>AGND</td>
<td>Relay4_A</td>
<td>Relay4_B</td>
<td>AGND</td>
</tr>
<tr>
<td colspan= "3" class="center-text">Relay1</td>
<td colspan= "3" class="center-text">Relay2</td>
<td colspan= "3" class="center-text">Relay3</td>
<td colspan= "4" class="center-text">Relay4</td>
</tr>
</table>  

## 主机接口5
0 到10V 可调电压输出  此接口默认为保留接口。
<table border="1">
<tr>  
<td >VO+</td>
<td >VO-</td>
<td >AGND</td>
</tr>

</table>

## 扩展接口6

<table border="1">
<tr>                      
<td colspan= "3" >COM9</td>
<td colspan= "3" >COM10</td>
<td colspan= "3" >COM11</td>
<td colspan= "3" >COM12</td>
</tr>
<tr> 
<td>RS232_TX</td>
<td>RS232_RX</td>
<td>AGND</td>
<td>RS232_TX</td>
<td>RS232_RX</td>
<td>AGND</td>
<td>RS232_TX</td>
<td>RS232_RX</td>
<td>AGND</td>
<td>RS232_TX</td>
<td>RS232_RX</td>
<td>AGND</td>
</tr>
</table>

## 扩展接口7

<table border="1">
<tr>                      
<td colspan= "3" >COM13</td>
<td colspan= "3" >COM14</td>
<td colspan= "3" >COM15</td>
<td colspan= "3" >COM16</td>
</tr>
<tr> 
<td>RS232_TX</td>
<td>RS232_RX</td>
<td>AGND</td>
<td>RS232_TX</td>
<td>RS232_RX</td>
<td>AGND</td>
<td>RS232_TX</td>
<td>RS232_RX</td>
<td>AGND</td>
<td>RS232_TX</td>
<td>RS232_RX</td>
<td>AGND</td>
</tr>
</table>

## 前面板介绍

<table border="1">
<tr>                      
<td rowspan= "2" >液晶屏</td>
<td rowspan= "2" >电源指示灯</td>
<td rowspan= "2" >红外接收头</td>
<td colspan= "1" >RS485 数据指示灯</td>
<td colspan= "1" >RS422 数据指示灯</td>
<td colspan= "1" >COM3 数据指示灯</td>
<td colspan= "1" >COM4 数据指示灯</td>
<td colspan= "1" >COM5 数据指示灯</td>
<td colspan= "1" >按键1</td>
<td colspan= "1" >按键2</td>
</tr>
<tr> 
<td>COM6 数据指示灯</td>
<td>COM7 数据指示灯</td>
<td>COM8 数据指示灯</td>
<td>保留</td>
<td>保留</td>
<td>按键3</td>
<td>按键4</td>
</tr>
</table>





