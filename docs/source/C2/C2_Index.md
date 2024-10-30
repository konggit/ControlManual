# 主机介绍

&emsp;&emsp;**C2 中控**使用无需编程概念，完成串口、红外、继电器、IO通道工作。

&emsp;&emsp;主机内置2路网络模块接口，可根据实际情况调整为TCP server（默认）、UDP client。
&emsp;&emsp;内置5路RS232/ 1 路RS485可选端口/ 1路RS422/RS485/RS232 可配接口。
&emsp;&emsp;内置8路IR 发送
&emsp;&emsp;内置8路继电器弱电控制
&emsp;&emsp;内置8路数字输入信号
&emsp;&emsp;轻松实现自定义命令，定时器控制，红外学习

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
<td>RS422_TX+/RS485_A+</td>
<td>RS422_TX-/RS485_B-/RS232_TX</td>
<td>RS422_RX+/RS232_RX</td>
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
<td>IR7-</td>
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
<td>DI2+</td>
<td>DI2-</td>
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