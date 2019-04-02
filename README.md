# QTReleaser -- QT应用软件可视化打包发布程序
### 操作
1. 初次使用时配置路径 (设置界面)
- 输入配置名称, 选择或输入windeployqt.exe的路径, 选择或输入QML安装路径 (可选). 
- 可以增加十条配置, 可以自由增加, 保存与删除. 
2. 选择配置 (主界面)
- 根据保存的配置名称选择配置, 当配置中有QML安装路径时可选Qt Widgets Application和Qt Quick Application两种项目类型, 若未保存QML安装路径则只有Qt Widgets Application可选. 
- 选择或输入release文件路径. 
- 根据需要, 选择要增加的其他参数, 也可自己填写. (可选)
3. 生成 (主界面)
- 直接点击生成按钮即可. 
- 输出信息会在完成后弹出在新窗口. 
4. 其他
- 文件菜单中可以打开配置文件目录, 也可点击 "打开配置文件" 并在程序中对配置文件进行浏览, 更改. 
### 注意
- 程序还未对用户所填路径进行彻底的校验检查, 只是检查了文件名和删除首尾空格而已, 因此需要用户确认自己所填路径正确无误. 
