# proton-wrapper
方便命令行使用 Proton 运行 exe 的简易包装器。

## 快捷方式

运行 Windows 安装包后，wrapper 会自动扫描当前 prefix 中的 `.lnk` 快捷方式，并导出到 Linux 应用菜单：

```sh
shorin-proton-wrapper -p ~/Games/foo-prefix ~/Downloads/setup.exe
```

也可以手动重新扫描：

```sh
shorin-proton-wrapper -p ~/Games/foo-prefix --export-shortcuts
```

## Gamescope 显示适配

运行环境设置界面支持 Gamescope、全屏、游戏分辨率、帧率限制、FSR 和 MangoHud。默认窗口化。CLI 也可以直接使用：

```sh
shorin-proton-wrapper --gamescope --res 1280x720 --fps 60 --fsr game.exe
```

MangoHud 为可选功能，未安装时设置界面会禁用对应选项：

```sh
shorin-proton-wrapper --mangohud game.exe
```

高级用户可以追加原生 Gamescope 参数：

```sh
shorin-proton-wrapper --gamescope --args "--mangoapp" game.exe
```
