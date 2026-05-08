# 巴西数据处理工具

data.ai CSV → Excel 底稿，一键处理。

## 部署步骤（首次，约5分钟）

### 1. 新建 GitHub 仓库

1. 打开 https://github.com/new
2. 填写仓库名，如 `brazil-data-tool`
3. 选择 **Public**
4. 点击 **Create repository**

### 2. 上传文件

把以下两个文件上传到仓库根目录：
- `index.html`
- `classification_rules.json`

上传方式：在仓库页面点 **Add file → Upload files**，拖入两个文件，点 **Commit changes**。

### 3. 开启 GitHub Pages

1. 进入仓库 **Settings → Pages**
2. Source 选择 **Deploy from a branch**
3. Branch 选择 **main**，目录选 **/ (root)**
4. 点 **Save**

等待约1分钟，页面会显示你的网址：
```
https://你的用户名.github.io/brazil-data-tool/
```

---

## 日常使用

1. 打开链接
2. 选择月份，上传 data.ai CSV（Overall 必传，分类别可选）
3. 填入 TikTok / Kwai 手动覆盖值
4. 点"开始处理"
5. 下载 Excel 底稿

---

## 更新分类规则库

当出现新 App 需要归类时：

1. 在工具的"未知 App"标签里为新 App 选择分类
2. 点"保存选中分类到规则库"→ 自动下载 `classification_rules.json`
3. 将下载的文件上传到 GitHub 仓库，**替换原有文件**
4. 下次打开工具时自动加载最新规则

---

## 文件说明

| 文件 | 说明 |
|------|------|
| `index.html` | 完整工具，无需安装任何依赖 |
| `classification_rules.json` | App 分类规则库，可手动编辑 |

## 注意事项

- TikTok 和 Kwai 的时长需要手动填入（来自内部看板和竞对监控）
- 上传分类别 CSV（7个）后，各分类合计数字更准确；只上传 Overall 时合计为近似值
- WhatsApp Messenger 和 WhatsApp Business 自动合并
- Instagram 自动归入泛短视频
