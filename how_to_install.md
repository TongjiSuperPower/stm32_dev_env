## 1 安装 STM32CubeMX
1. 创建ST帐户（后续多个步骤需要）：https://www.st.com.cn/content/st_com/zh/user-registration.html
2. 下载安装包（版本>=6.11）：https://www.st.com.cn/zh/development-tools/stm32cubemx.html
3. 安装：按照推荐/默认选项一步一步往下走即可。
4. 启动后登录ST帐户，如果提示`This feature requires internet connection...`，重新打开软件即可。
![](imgs/cubemx_login.png)
5. 选择INSTALL/REMOVE，如果提示`The Updater is already in use and checking the server.`耐心等待即可。
![](imgs/cubemx_install.png)
6. 勾选STM32F4，点击Install，如果使用达妙H7开发板，还需勾选STM32H7。
![](imgs/cubemx_stm32f4.png)

## 2 安装 STM32CubeCLT
1. 下载安装包（版本>=1.15）：https://www.st.com.cn/zh/development-tools/stm32cubeclt.html
2. 安装：按照推荐/默认选项一步一步往下走即可。
    - 如果遇到`Error launching installer`，请将安装程序移动到不包含中文的路径下。
    - 如果遇到`Error! Can't initialize plug-ins directory. Please try again later.`：
        1. 在C盘根目录下新建Temp文件夹
        ![](imgs/mkdir_temp.png)
        2. 打开环境变量
        ![](imgs/open_env_var_edit.png)
        3. 按照下图步骤分别将`TMP`和`TEMP`中的内容修改为`C:\Temp`，注意`TMP`和`TEMP`都要修改
        ![](imgs/edit_temp.png)

3. 检查安装是否成功：
    1. 打开powershell
    ![](imgs/open_powershell.png)
    2. 依次输入下面三行命令（注意空格），如果输出和下图一致则安装成功。
        ```
        cmake --version
        ninja --version
        arm-none-eabi-gcc --version
        ```
        ![](imgs/check_clt.png)

## 3 安装 Visual Studio Code
1. 下载安装包（版本>=1.92）：https://code.visualstudio.com
2. 安装时注意勾选这两个选项
![](imgs/install_vscode.png)
3. 启动后选择左侧插件图标打开插件面板
![](imgs/open_extension.png)
4. 安装C++插件
![](imgs/install_cpp_ext.png)
5. 安装CMake Tools插件
![](imgs/install_cmake_ext.png)
6. 安装Cortex-Debug插件
![](imgs/install_cortex_ext.png)
7. 如果插件面板和下图一致则安装成功
![](imgs/extensions.png)

## 4 安装 OpenOCD
1. 下载压缩包（版本>=20231002）：https://gnutoolchains.com/arm-eabi/openocd/
2. 解压至C盘根目录
![](imgs/extract_openocd.png)
3. 打开解压后的文件夹中的`bin`文件夹，复制其路径
![](imgs/copy_openocd_path.png)
4. 打开环境变量
![](imgs/open_env_var_edit.png)
5. 按照下图步骤添加所复制的路径
![](imgs/add_openocd_path.png)
6. 检查安装是否成功：
    1. 打开powershell
    ![](imgs/open_powershell.png)
    2. 输入`openocd --version`，如果输出和下图一致则安装成功。
        ![](imgs/check_openocd.png)

## 5 安装 SerialPlot
1. 下载安装包：https://github.com/hyOzd/serialplot/releases/tag/v0.13.0
2. 安装：按照推荐/默认选项一步一步往下走即可。

## 6 安装 Git
1. 下载安装包：https://git-scm.com/download/win
![](imgs/download_git.png)
2. 安装：按照推荐/默认选项一步一步往下走即可。
