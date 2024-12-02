# XGpioPs_SetDirectionPin函数的用法
## 1.1定义
函数原型为`void XGpioPs_SetDirectionPin(const XGpioPs *InstancePtr, u32 Pin, u32 Direction){......}`作用是设置对应的MIO接口（`u32 Pin`）为输入还是输出（`u32 Data`为0则为输入，`u32 Data`为1则为输出）
-`const XGpioPs *InstancePtr`为GPIO设备的驱动程序实例
-`u32 Pin`是对应的MIO接口
-`u32 Data`指定该接口为输入还是输出
## 1.2实例
- `#define MIO_LED             0;`           //led连接到 MIO0
-`XGpioPs Gpio;`                //GPIO设备的驱动程序实例
-`XGpioPs_SetDirectionPin(&Gpio, MIO_LED, 1);`  //指定该引脚为输出
