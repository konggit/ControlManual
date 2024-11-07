# 术语介绍  

## 数据端口
用于数据发送和接收的通讯端口  
> [!NOTE]  
> Highlights information that users should take into account, even when skimming.

|   **名字**   |   **值**  |   **外部端口名字**   |
| :--------: |  :--------:  | :-------: |
| 端口0   |  0   |   IP  |
| 端口1   |  1   |    RS485    |
| 端口2   |  2   |   RS422  |
| 端口3   |  3   |   COM1  |
| 端口4   |  4   |   COM2  |
| 端口5   |  5   |   COM3  |
| 端口6   |  6   |   COM4  |
| 端口7   |  7   |   COM5  |
| 端口8   |  8   |   COM6  |
| 端口9   |  9   |   CAN   |
| 端口10   |  9   |   COM7  |
| 端口11   |  10   |   COM8  |
| 端口12   |  11  |   COM9  |
| 端口13   |  12   |   COM10  |
| 端口14   |  13   |   COM11  |
| 端口15   |  14   |   COM12  |
| 端口16   |  15   |   COM13  |
| 端口17   |  16   |   COM14  |

带扩展串口主机

|   **名字**   |   **值**  |   **外部端口名字**   |
| :--------: |  :--------:  | :-------: |
| 端口0   |  0   |   IP  |
| 端口1   |  1   |    RS485    |
| 端口2   |  2   |   RS422  |
| 端口3   |  3   |   COM1  |
| 端口4   |  4   |   COM2  |
| 端口5   |  5   |   COM3  |
| 端口6   |  6   |   COM4  |
| 端口7   |  7   |   COM5  |
| 端口8   |  8   |   COM6  |
| 端口9   |  9   |   COM7  |
| 端口10   |  10   |   COM8  |
| 端口11   |  11  |   COM9  |
| 端口12   |  12   |   COM10  |
| 端口13   |  13   |   COM11  |
| 端口14   |  14   |   COM12  |
| 端口15   |  15   |   COM13  |
| 端口16   |  16   |   COM14  |
| 端口17   |  17   |   CAN  |


## 用户命令

定义一串数据 当中控收到这串数据数据时候会认为是一个完整的命令，它可以当作事件表中某个事件的一个触发源。  
我们经常会在**事件表** 的事件源中的**用户命令x**  来匹配使用


## 预设命令
预先定义一串数据为一个命令，用户只要指定中控要发送第几号命令，我们经常会在**事件表** 的事件类型中的**发送命令** 中调用第几条预置命令