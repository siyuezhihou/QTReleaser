# QTReleaser -- QT应用软件可视化打包发布程序
### 操作
- 1. 初次使用时配置路径 (设置界面)
    - 新增配置
        - 方法1. 使用自动录入功能, 指定目录, 快速自动录入新配置并自动命名, 也可随时结束录入. 
        - 方法2. 输入配置名称, 选择或输入windeployqt.exe的路径, 选择或输入QML安装路径 (可选). 
        - 方法3. 在软件内或在资源管理器直接打开配置文件并进行更改 (第四条)
    - 可以增加十条配置, 可以自由增加, 保存与删除. 
- 2. 选择配置 (主界面)
    - 选择是否使用简单打包模式. (详见下方对打包模式的介绍)
    - 根据保存的配置名称选择windeployqt配置, 非简单打包模式下当配置中有QML安装路径时可选Qt Widgets Application和Qt Quick Application两种项目类型, 若未保存QML安装路径则只有Qt Widgets Application可选. 
    - 选择, 输入, 或者直接拖拽文件至主界面以获取待发布文件路径. 
    - 根据需要, 选择要增加的其他参数, 也可自己填写. (可选)
- 3. 生成 (主界面)
    - 直接点击生成按钮即可. 
    - 输出信息会在打包完成后弹出在新窗口. 
- 4. 其他
    - 文件菜单中可以打开配置文件目录, 也可点击 "打开配置文件" 并在程序中对配置文件进行浏览, 更改. 
### 简单打包模式
**简单打包模式脱离了windeployqt.exe, 由程序自主完成基础打包.**
#### 优势
- 使用非简单打包模式 (即依赖windeployqt), 可能会发生打包后依旧缺少动态链接库的情况, 而简单打包模式不会发生. 
- 在本软件中使用简单打包模式只需要设置编译版本和待打包文件路径即可直接生成, 简单迅速. 
- 只进行必要的打包, 占用空间少. 
#### 劣势
- 暂时无法进行复杂打包. 
#### 适用情形: 
- 当应用软件没有使用非基础功能, 不需要使用windeployqt.exe进行打包. 
- 当使用windeployqt.exe打包失败, 仍然缺少某些基础动态链接库, 需要使用简单打包模式补全. 
- 当用户对打包后占用空间大小有要求时. 
### 注意
- 非简单打包模式下文件路径不能有空格, 原因为非简单模式打包依赖控制台运行windeployqt.exe, 若要使控制台识别带空格的路径, 必须要加上双引号, 而QString不支持双引号, 也无法转义. 如果不使用QString, 输出结果会变得bijiaomaf. 这个问题留着以后慢慢解决. 
### 待更新
### 已知BUG
