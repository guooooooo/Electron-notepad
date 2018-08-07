# Electron-notepad

> 实现简单记事本，熟悉下Electron，API丰富强大，一套代码即可实现跨系统桌面应用。

## 项目要点

- 项目使用electron-forge。相当于electron的一个脚手架，可以让我们更方便的创建、运行、打包electron项目。
- package.json中main配置项为主进程入口文件

## 使用到的主要API

- 主进程使用 BrowserWindow 实例创建页面。 每个 BrowserWindow 实例都在自己的渲染进程里运行页面。 当一个 BrowserWindow 实例被销毁后，相应的渲染进程也会被终止。
- 使用窗口实例的 loadURL 方法加载远程 URL 或者加载本地 HTML 文件。
- Menu 用来创建原生应用菜单和上下文菜单。
- MenuItem 菜单项可设置 lable ,内置 role , accelerator 快捷键, click 事件等属性。
- 通过 webContents.send 从主进程向渲染器进程发送异步消息，可以发送任意参数。
- ipcMain 在主进程处理从渲染器进程（网页）发送出来的异步和同步信息。 从渲染器进程发送的消息将被发送到该模块。
- ipcRenderer 从渲染进程发送同步或异步的消息到主进程。也可以接收主进程回复的消息。
- remote 在渲染进程中使用主进程模块。GUI 相关的模块 (如 dialog、menu 等)。
