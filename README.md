# STM32
STM32F103C8T6新建程序让他跑起来
1. Uvision里面新建project 他会自己创建这么多程序
![image](https://github.com/user-attachments/assets/d0a3788f-3dca-449d-8f88-9beded991ecd)
2. 我们需要加入STM32启动文件，最基础的那种Startup文件，把下面图一放在Startup文件夹里面
![image](https://github.com/user-attachments/assets/3080c582-9a70-446a-8468-14619869ac4a)
![image](https://github.com/user-attachments/assets/524122ee-a4ab-43b7-9736-0f0347ea5454)
4. 我们还需要一些文件放在Startup里面，一个是用来说明STM32每个引脚对应的寄存器。还有一个是下图中的system文件，是用来配置时钟的。我们的主频72MHz就是这个两个文件配置的。把下面三个粘贴到startup
![image](https://github.com/user-attachments/assets/f82f4569-94a7-44b5-999b-a62da6be2016)
为什么我们这里选的是.md的这个，这个是根据不同芯片选的，见下表
![image](https://github.com/user-attachments/assets/029f9f20-01bc-4378-8ba9-394abc056167)
5.我们还需要添加内核寄存器描述文件到我们的startup文件夹（第四步添加的是device support，现在添加的是core support）。（.c是一些内核配置函数，.h是一些内核寄存器描述文件。）
![image](https://github.com/user-attachments/assets/7d398071-a885-4d25-8a31-dd5045e0451b)
6. 文件夹里面操作后要添加启动文件了，这个时候只能添加一个启动程序，我们用的板子添加这个.md程序
![image](https://github.com/user-attachments/assets/cadee412-14f8-4288-90b5-51ba8c3d6901)
7. 刚刚添加进来的.h路径我们要让软件能找到就要添加其路径。
   点击魔术棒，点击C，C++，点击path
   ![image](https://github.com/user-attachments/assets/1451bbe3-d6be-4c9d-8ef5-3de1632c8967)
8. 下面我们把main文件添加到我们的工程里面。下面将演示如何添加main.c
![image](https://github.com/user-attachments/assets/6ccc753b-08fb-4578-8b19-ade825cee48d)
右击target1-add group
![image](https://github.com/user-attachments/assets/c07e3fa9-dbc1-41fc-8dbe-25a84675a734)
把group名字改成user之后，右击user，add new item。然后添加main.c，注意要选放在user文件夹里面
![image](https://github.com/user-attachments/assets/4b763a31-ba40-445c-b554-1bb27e6d47d3)



