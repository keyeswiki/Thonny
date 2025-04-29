# ESP32--Thonny软件下载安装和使用方法

在开始构建项目之前，你需要首先做一些准备，这是非常重要的，你不能跳过。

<span style="color: rgb(255, 76, 65);">**特别注意：**</span>下面的压缩包文件一定要下载，后面会用到。

[CP2102驱动_Python固件和代码](CP2102驱动_Python固件和代码.zip) 

## 一、安装Thonny(重要)：

Thonny是一个免费、开源的软件平台，体积小，界面简单，操作简单，功能丰富，是一个适合初学者的Python IDE。在本教程中，我们使用这个IDE在整个过程中开发ESP32。Thonny支持多种操作系统，包括Windows, Mac OS,  Linux。
### 1.下载Thonny软件：

(1) 进入软件官网：[https://thonny.org](https://thonny.org) 下载Thonny软件，最好下载最新版的，否则可能不支持ESP32.

(2) Thonny的开源代码库：[https://github.com/thonny/thonny](https://github.com/thonny/thonny)

请按照官网的指导安装或点击下面的链接下载安装。(请根据您的操作系统选择相应的选项.)

|操作系统|下载链接/方法|
| :--: | :--: |
|MAC OS：|[https://github.com/thonny/thonny/releases/download/v3.2.7/thonny-3.2.7.pkg](https://github.com/thonny/thonny/releases/download/v3.2.7/thonny-3.2.7.pkg)|
|Windows：|[https://github.com/thonny/thonny/releases/download/v3.2.7/thonny-3.2.7.exe](hhttps://github.com/thonny/thonny/releases/download/v3.2.7/thonny-3.2.7.exe)|
|Linux：|最新版本:(如下)
```
Binary bundle for PC (Thonny+Python): 
bash <(wget -O - https://thonny.org/installer-for-linux) 
With pip:
pip3 install thonny
Distro packages (may not be the latest version):
Debian, Rasbian, Ubuntu, Mint and others:
sudo apt install thonny
Fedora:
sudo dnf install thonny
```
|

![Img](./media/__Thonny__1img-20230407164139.png)

![Img](./media/__Thonny__2img-20230407164143.png)

### 2.Windows上安装Thonny软件：

A.下载后的Thonny图标如下。

![Img](./media/Windows___Thonny__1img-20230407164156.png)

B.双击“thonny-4.0.2.exe”，会出现下面对话框，我这里是选择“![Img](./media/Windows___Thonny__2img-20230407164219.png)”进行操作的。你也可以选择“![Img](./media/Windows___Thonny__3img-20230407164228.png)”进行操作的。

![Img](./media/Windows___Thonny__4img-20230407164239.png)

C.如果您不熟悉电脑软件安装，您可以一直单击“**Next**”直到安装完成。

![Img](./media/Windows___Thonny__5img-20230407164257.png)

![Img](./media/Windows___Thonny__6img-20230407164306.png)

D.如果您需要更改Thonny软件的安装路径，可以单击“**Browse...**”进行修改。选择安装路径后，单击“**OK**”。

如果您不想更改安装路径，只需单击“**Next**”；然后又继续单击“**Next**”。

![Img](./media/Windows___Thonny__7img-20230407164314.png)

![Img](./media/Windows___Thonny__8img-20230407164325.png)

E.选中“**Create desktop icon**”，Thonny软件会在你的桌面上生成一个快捷方式，方便你稍后打开Thonny软件。

![Img](./media/Windows___Thonny__9img-20230407164341.png)

F.单击“**Install**”安装软件。

![Img](./media/Windows___Thonny__10img-20230407164353.png)

G.在安装过程中，您只需等待安装完成，千万不要点击“**Cancel**”，否则将无法安装成功。

![Img](./media/Windows___Thonny__11img-20230407164405.png)

H.一旦看到如下界面，就表示已经成功安装了Thonny软件，点击“**Finish**”就可以。

![Img](./media/Windows___Thonny__12img-20230407164412.png)

I.如果你在安装过程中选择了“**Create desktop icon**”，则可以在桌面上看到如下图标。

![Img](./media/Windows___Thonny__13img-20230407164419.png)

## 二、Thonny软件基本配置 
                                         
A.双击Thonny软件的桌面图标，可以看到如下界面，同时还可以进行语言选择(<span style="color: rgb(255, 76, 65);">这里选择简体中文</span>)和初始设置。设置完了点击“**Let’s go！**”。

![Img](./media/Thonny______1img-20230407164446.png)

![Img](./media/Thonny______2img-20230407164453.png)

![Img](./media/Thonny______3img-20230407164457.png)

![Img](./media/Thonny______4img-20230407164500.png)

![Img](./media/Thonny______5img-20230407164507.png)

B.选择“**视图**”→“**文件**”和“**Shell**”。

![Img](./media/Thonny______6img-20230407164524.png)

![Img](./media/Thonny______7img-20230407164531.png)

![Img](./media/Thonny______8img-20230407164535.png)

## 三、安装CP2102驱动：

ESP32通过CP2102驱动下载代码。所以在使用它之前，我们需要在计算机中安装CP2102驱动程序。

### Windows 系统

#### 检查CP2102驱动是否已经安装

1. 用USB线连接计算机和ESP32。

![Img](./media/__CP2102__1img-20230407164720.png)

2. 进入计算机主界面，选择“**此电脑**”，右键单击选择“**管理**”。

![Img](./media/__CP2102__2img-20230407164747.png)

3.单击“**设备管理器**”。如果你的计算机已经安装了CP2102驱动，则可以看到“**Silicon Labs CP210x USB to UART Bridge(COMx)**”。

![Img](./media/__CP2102__3img-20230407164755.png)

#### 安装CP2102驱动

1. 如果未安装CP2102驱动，界面显示如下。

![Img](./media/__CP2102__4img-20230407164826.png)

2.单击“**CP2102 USB to UART Bridge Controller**”，右键选择“**更新驱动程序(P)**”。

![Img](./media/__CP2102__5img-20230407164834.png)

3.单击“**浏览我的电脑以查找驱动程序(R) **”.

![Img](./media/__CP2102__6img-20230407164842.png)

4.单击“浏览(R)...”选择CP210x_6.7.4(驱动路径：**..\CP2102 驱动文件-Windows**)，单击“**下一页**”

![Img](./media/__CP2102__7img-20230407164850.jpg)

5. 等待CP2102驱动安装完成。当界面显示如下时，表示已安装CP2102驱动。你可以关闭该界面。

![Img](./media/__CP2102__8img-20230407164900.png)

6.ESP32与计算机连接时，界面显示如下。

![Img](./media/__CP2102__9img-20230407164907.png)

## 四、烧入Micropython固件(重要)

要在ESP32主板上运行Python程序，我们需要先将固件烧入到ESP32主板。

### 下载Micropython固件

microPython官方网站：[http://micropython.org/](http://micropython.org/)

网页列出microPython的ESP32固件：[https://micropython.org/download/esp32/](https://micropython.org/download/esp32/)

![Img](./media/__Micropython__1img-20230407183736.png)

本教程中使用的固件是：esp32-20210902-v1.19.bin

我们的文件夹中也提供了这个固件：“**..\Python_固件**”。
![Img](./media/__Micropython__2img-20230407183923.png)

### 烧入Micropython固件

用USB线连接计算机和ESP32主板。

![Img](./media/__Micropython__3img-20230407184019.png)

确保驱动程序已成功安装，并能正确识别COM端口。打开设备管理器并展开“**端口(COM和LPT)**”。

![Img](./media/__Micropython__4img-20230331154259.png)

<span style="color: rgb(255, 76, 65);">注意：不同的电脑，COM端口可能不同，这是正常情况。</span>

<br>
<br>

1. 打开Thonny，点击“**运行**” ，选择 “**配置解释器**”。

![Img](./media/__Micropython__5img-20230331154547.png)

2.选中“**MicroPython (ESP32)**”，选中“**Silicon Labs CP210x USB to UART Bridge(COM7)**”，然后点击“**安装或更新MicroPython**”。

![Img](./media/__Micropython__6img-20230331154754.png)

![Img](./media/__Micropython__7img-20230331154903.png)

![Img](./media/__Micropython__8img-20230331154946.png)

3.弹出如下对话框，“**Port**”选择“**Silicon Labs CP210x USB to UART Bridge(COM7)**”，单击“**Browse...**”选择之前准备好的microPython固件<span style="color: rgb(0, 209, 0);">esp32-20220618-v1.19.1.bin</span>。检查“Erase flash before installing”和“Flash mode”，然后点击“**安装**”，等待安装完成提示。（<span style="color: rgb(255, 76, 65);">注意：如果安装固件失败，请再次点击“**安装**”，然后按住ESP32主板上的Boot键![Img](./media/__ESP32____Boot_img-20230407184236.png)，出现上传进度百分比再松开Boot键。</span>）

![Img](./media/__Micropython__9img-20230331155325.png)

![Img](./media/__Micropython__10img-20230407184613.png)

![Img](./media/__Micropython__11img-20230407184841.png)

4.等待安装完成。安装完成后先点击“**关闭**”再点击“**好的**”就行。

![Img](./media/__Micropython__12img-20230407185010.png)

![Img](../media/__Micropython__13img-20230407185140.png)

![Img](./media/__Micropython__14img-20230407185217.png)

5.关闭所有对话框，转到主界面，点击“![Img](./media/_________img-20230407185304.png)”。如下图所示：

![Img](./media/__Micropython__15img-20230407185538.png)

6.到目前为止，一切准备工作都已就绪。

## 五、测试代码：

### 测试Shell命令

在“Shell”窗口中输入“print('hello world')”并按Enter键。

![Img](./media/__Shell__img-20230407185641.png)

### 在线运行

ESP32需要连接到计算机时，它是在线运行。用户可以使用Thonny编写和调试程序。

1. 打开Thonny并单击![Img](./media/__img-20230407185656.png)“打开”。

![Img](./media/____1img-20230407185706.png)

2.在新弹出的窗口中，单击“**此电脑**”。

![Img](./media/____2img-20230407185717.png)

在新的对话框中，在路径：“..\项目01 Hello World” 中选择“**Project_01_HelloWorld.py**”。

![Img](./media/____3img-20230407190647.png)

![Img](./media/____4img-20230407190808.png)

单击![Img](./media/__img-20230407195758.png), “Hello World”将在“Shell”窗口中打印出来。

![Img](./media/____5img-20230407190858.png)

<span style="color: rgb(255, 76, 65);">注意：</span>在线运行时，如果按下ESP32的复位键，用户的代码将不会再次执行。

## 六、Thonny常见的操作：

### 上传代码到ESP32

为了方便起见，我们以“**项目10 8×8点阵屏**”为例。在“**项目10 8×8点阵屏**”文件夹中选择“ht16k33\.py”，右键单击鼠标，选择“**上传到/**”将代码上传到ESP32的根目录中。

![Img](./media/_____ESP32-1img-20230407192206.png)

![Img](./media/_____ESP32-2img-20230407192235.png)

### 下载代码到电脑

在“MicroPython 设备”中选择“boot\.py”，右键选择“**下载到…**”把代码下载到你的电脑里。

![Img](./media/_______img-20230407192442.png)

### 删除ESP32根目录下的文件

在“MicroPython 设备”中选择“ht16k33\.py”，右键单击它且选择“**删除**”，将“ht16k33\.py”从ESP32的根目录中删除。

![Img](./media/__ESP32_____1img-20230407192540.png)

![Img](./media/__ESP32_____2img-20230407192610.png)

![Img](./media/__ESP32_____3img-20230407192636.png)













