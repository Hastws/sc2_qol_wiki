# 星际争霸 2 优化设置指南 (Windows)

> QoL = Quality of Life（生活质量优化）

---

## 1. 系统设置

### 1.1 键盘连发速度优化（推荐）

#### 方法一：控制面板设置

1. 打开 **控制面板 → 键盘**（或运行 `control keyboard`）
2. 调整以下选项：
   - **重复延迟（Repeat delay）**：调到 **最短**
   - **重复速度（Repeat rate）**：调到 **最快**
3. 点击"应用"

#### 方法二：注册表调整（可选，更精确）

路径：`HKEY_CURRENT_USER\Control Panel\Keyboard`

| 键名 | 值 | 说明 |
|------|-----|------|
| `KeyboardDelay` | `0` | 最短延迟 |
| `KeyboardSpeed` | `31` | 最快速度 |

> ⚠️ 修改后需要**重新登录或重启**才能生效。  
> 📝 Windows 的键盘重复速度有系统上限，调到头就是极限了。

---

### 1.2 关闭鼠标加速

**设置 → 蓝牙和其他设备 → 鼠标 → 其他鼠标选项 → 指针选项**

取消勾选 **"增强指针精确度（Enhance pointer precision）"**

---

## 2. 游戏画质优化

### High 画质下的推荐步骤（最清晰）

#### 步骤 1：设置游戏画质

在游戏设置里将 **Graphic Settings**（以及 Textures）调到你想要的档位（如 High）。

#### 步骤 2：退出游戏

关闭 StarCraft II 后再修改配置文件。

#### 步骤 3：修改 `variables.txt`（核心）

在 `Documents/StarCraft II/` 目录下找到 `variables.txt`，在末尾追加：

```ini
GraphicsOptionShadowQuality=0
shadowmapsize=1
```

**效果**：在 Medium/High/Ultra/Extreme 画质下移除 3D 阴影，同时保留 blob 阴影（游戏内选项无法实现）。

#### ⚠️ 重要注意

如果 blob 阴影"突然消失"：
- **原因**：在 Options 里更改任何设置（甚至点 OK）都可能导致 blob 阴影消失
- **解决**：重新在 `variables.txt` 末尾追加上述两行，并尽量避免在 Options 里修改设置

---

## 3. 游戏内设置

### 3.1 游戏玩法

✅ 勾选**除"启用简易命令卡"以外**的所有复选框

> ⚠️ "启用选择敌方单位"功能存在争议，可能会导致一些问题。

### 3.2 声音设置

❌ 取消勾选以下选项：
- **响应声音**
- **环境声音**
