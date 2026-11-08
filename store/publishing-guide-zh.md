# Grey Black White — Microsoft Edge Add-ons 发布步骤

> 说明：Microsoft Edge Add-ons 的上传/发布必须在 **Partner Center** 中登录你自己的 Microsoft 账号完成。我无法代替你登录账号、勾选协议或点击 Publish；但我已经把**可直接上传的包、商店文案、Logo、截图和逐项填写内容**都准备好了。你只需按下面步骤操作。

## 已准备好的文件

```
Grey-Black-White-v2.3.0.zip     ← 在 Partner Center 上传的商店包（manifest.json 在 zip 根目录）
logo-300.png                     ← Store logo（300×300）
screenshots/01-main-1280x800.png ← 截图 1（1280×800）
screenshots/02-palette-1280x800.png ← 截图 2（1280×800）
listing.md                       ← 名称、长短描述、分类、搜索词、隐私问答、审核备注
privacy-policy.html              ← 隐私政策页面（可自行托管）
privacy-policy.md                ← 隐私政策 Markdown
```

## 1. 注册 Partner Center / Edge 开发者账号

1. 打开 https://partner.microsoft.com/dashboard/microsoftedge/overview
2. 使用你的 Microsoft 账号登录。
3. 加入 **Microsoft Edge** 计划。个人开发者注册免费；按页面要求完成账号验证（可能需要邮箱/身份验证，视账号情况而定）。
4. 记录你的 **Publisher display name**（发布者显示名），它会展示在商店。

## 2. 创建扩展并上传商店包

1. 在 Partner Center 的 **Microsoft Edge** 工作区，点击 **Create new extension**。
2. 上传 `Grey-Black-White-v2.3.0.zip`。
   - 这是主题专用包，里面只有 `manifest.json` 和图标；没有脚本、没有权限。
3. 等待包校验通过，检查 Extension overview；扩展名称应为 **Grey Black White**，版本 **2.2.0**。

## 3. Availability（可用性）

- Visibility：**Public**
- Markets：**All markets**（或按你的需要选择）
- 免费（Free）

## 4. Properties（属性）

- Category：**Themes**（如果列表里没有，选最接近的主题/个性化分类）
- Website：可留空
- Support contact：填你的邮箱或支持页面
- Mature content：**No**

## 5. Privacy（隐私）

按以下内容填写：

- **Single purpose**
  `Applies a static, monochrome light theme to the Microsoft Edge browser interface.`
- **Permission justification**
  本包没有声明任何权限；若页面显示权限列表为空，无需填写。
- **Are you using remote code?**
  **No**
- **Data usage**
  所有用户数据类型都不勾选；确认不收集、不出售、不共享数据，并勾选相应认证项。
- **Privacy policy URL**
  扩展不收集数据，通常不是必填。如果 Partner Center 仍要求 URL，可把 `privacy-policy.html` 发布到 GitHub Pages / Gist / Notion 等公开页面，填入其 URL。
  - 使用前把页面里的 `[YOUR SUPPORT EMAIL]` 换成你的联系邮箱。

## 6. Store listing（商店详情页）

语言选择 **English (en-US)**（商店包 manifest 使用英文名称/描述）。

- **Extension name**：自动读取 `Grey Black White`
- **Description**：粘贴 `listing.md` 中“Full description”全文（至少 250 字符）
- **Extension logo**：上传 `logo-300.png`
- **Screenshots**：上传两张 1280×800 截图（可只传第一张，最多 6 张）
- **Short description**：自动来自 manifest：
  `A minimal light Edge theme with a pure black title bar, #333333 toolbar, and a bright page area.`
- **Search terms**（最多 7 个，每个 ≤30 字符）：
  `grey theme`, `black theme`, `monochrome`, `minimal theme`, `light theme`, `edge theme`, `grey black white`
- YouTube video：可留空
- Small / Large promotional tile：可选，不上传也可以提交

## 7. Certification notes（审核备注）

粘贴 `listing.md` 的 “Notes for certification” 段落。核心内容是：这是纯主题扩展，无脚本、无权限、无网络；安装后黑色标题栏、#333333 工具栏、浅色页面；不需要测试账号。

## 8. 提交审核

点击 **Publish** 提交认证。Microsoft Edge Add-ons 认证通常最多需要 **7 个工作日**。通过后商店状态会变成 **In the Store**，并生成公开的 listing URL。

## 注意

- 商店包和截图里的名称必须保持一致：**Grey Black White**。
- 截图是主题配色预览图（1280×800），展示黑色标题栏、#333333 工具栏和浅色页面；如你有真实 Edge 截图，也可以替换。
- 商店包的 `description` 只能较短（Chromium 限制 132 字符）；完整的商店描述请在 Partner Center 的 Description 字段粘贴 `listing.md` 里的长描述。
- 如果页面提示隐私政策 URL 必填，必须先把隐私政策发布到一个公开可访问的 URL。
