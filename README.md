# 数值分析大作业——图像变形处理
本项目目标是编写程序对人脸图像进行扭曲变形，以及图像的扭曲与畸变变换。项目使用C++/Qt5.12.4/OpenCV4在VS2019上配置编译（MSVC_2017_x64）。
## 可执行文件及UI界面
UI界面的执行需要在Windows64位系统中使用，可以打开\face_strech_ui\x64\Release\Face_Strech_UI.exe进行使用。
<img src="https://github.com/ChenDRAG/hello-world/blob/master/Screenshot%20from%202019-10-20%2000-37-10.png?raw=true" width=600 alt="UI">  

- 游戏模式提供7或13两种选择
- 7巧板状态下，可调整“选择”索引，从数据库中选择数据。
- 你可以将图片绝对地址填入加载框中，点击load加载自定义数据
- 加载好数据后，点击结果直接获得结果
- 你也可以点击演示，此时程序获取结果后将允许您点击< h或 > 按钮观察程序底层的搜索过程。

- 所有的搜索都可以在1s内完成，如果超出这个时间可能是出现了异常

## 文件说明
- /src/solver.py 包含了对七巧板的整套解决方案（核心代码）
- /src/solver_nine_pieces.py 包含对十三巧板解决方案，为了方便（时间原因），我直接在七巧板文件基础上做了修改而没有过于考虑封装
- /src/mainUI.py 主界面文件，调用核心算法并完成图形化工作
- /src/Window.py 这是pyqt根据ui文件自动生成的文件，包含对界面的图形化定义
  
## 结果

<img src="https://raw.githubusercontent.com/ChenDRAG/hello-world/master/Screenshot%20from%202019-10-20%2000-37-52.png" width=600 alt="ex1">

<img src="https://github.com/ChenDRAG/hello-world/blob/master/Screenshot%20from%202019-10-20%2000-39-37.png?raw=true" width=600 alt="ex2">

## 作者
作者：清华大学自动化系自76班 陈华玉  
邮箱：chenhuay17@mails.tsinghua.edu.cn  
github：chendrag
