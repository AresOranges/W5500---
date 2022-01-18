# W5500以太网网络模块
淘宝链接：  https://m.tb.cn/h.fPzf7fQ?tk=vZWs2cICR8c  
相关博客： 1. https://blog.csdn.net/qq_45659777/article/details/121952778?utm_medium=distribute.pc_relevant.none-task-blog-2~default~baidujs_baidulandingword~default-0.pc_relevant_default&spm=1001.2101.3001.4242.1&utm_relevant_index=3  
  2. https://blog.csdn.net/weixin_46129506/article/details/122149700  

# SPI通信  
同步 全双工通信  
（同步：发送方发出数据后，等待收方发回响应后，再发下一个数据包  
    异步：发送方发出数据后，接着发送下一个数据包，不等待收方发回响应）  

SPI总共有4根线：  
SCLK (Serial Clock) 串行时钟 传输时钟信号的信号线。    
CS (SS) 片选信号（从设备选择） 用于选择从设备的信号线，低电平有效。  
MOSI (Master Out Slave In) 主设备出，从设备入  
MISO (Master In Slave Out) 主设备入，从设备出。  

上升沿发送，下降沿接收，高位先发送。  

CPOL：时钟极性选择，为0时SPI总线空闲为低电平，为1时SPI总线空闲为高电平  
CPHA：时钟相位选择，为0时在时钟第一个跳变沿采样，为1时在时钟第二个跳变沿采样  

# 客户端模式  
必须设置的网络参数：  
unsigned char Gateway_IP[4]; //网关IP地址，4个字节  
unsigned char Sub_Mask[4]; //子网掩码，4个字节  
unsigned char Phy_Addr[6]; //物理地址(MAC)，6个字节，第一个字节必须为偶数  
unsigned char IP_Addr[4]; //本机IP地址，4个字节
unsigned char S0_Port[2]; //端口0的端口号，2个字节
unsigned char S
