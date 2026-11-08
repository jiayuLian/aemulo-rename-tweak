# AemuloRename

Aemulo 2.0（com.amywhile.Aemulo，build 1432）的卡片重命名插件。

Aemulo 本身没有改备注名的入口，只能在 PC 上改 `TagDatabase.sqlite3`。
这个 dylib 在 Home 页导航栏加一个「改名」按钮，直接读写同一个库的 `name` 列。

- 零依赖：不链 CydiaSubstrate / ElleKit，TrollStore 设备可用
- 不改 App 任何内部实现，只挂 `UIViewController` 的 `viewDidLoad` / `viewDidAppear`
- 兜底入口：窗口上**双指长按** 0.8 秒

## 用法

首选 **TrollFools** 注入 `AemuloRename.dylib`（原位注入，保留数据）。
整包注入版见 Releases。

## 构建

推 main 触发 GitHub Actions（macos-14），产物在 artifact `AemuloRename`。
