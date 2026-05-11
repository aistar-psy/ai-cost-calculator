# AI心理对话成本测算工具

这是一个用于测算AI心理对话项目年度成本的工具，支持多种大模型选择和详细的成本拆解。

## 功能特点

- 📊 支持多种国内外大模型（豆包、千问、DeepSeek、GPT、Claude等）
- 💰 详细的成本拆解（文本对话、语音、知识库、垂类模型）
- 📝 历史测算记录保存和查看
- 🔒 后台配置模式（Token配置、语音配置、其他费用锁定）
- 📱 响应式设计，支持移动端访问

## 使用说明

### 基础使用（市场人员）

1. 填写基础参数：学生总人数、月活跃率、人均对话数等
2. 选择使用的模型（默认为 doubao-seed-2.0-mini [32-128k]）
3. 点击"开始测算"查看年度成本
4. 测算记录自动保存到左侧历史列表

### 后台配置（管理员）

1. 点击页面右下角的 ⚙️ 设置按钮
2. 输入管理员密码：`admin123`
3. 进入管理员模式后可修改：
   - Token配置（单轮输入/输出Token数）
   - 语音配置（转写/合成单价）
   - 其他费用（知识库、垂类模型等）

## 部署到 GitHub Pages

### 方法一：通过 GitHub 网页操作

1. 登录 GitHub，创建新仓库（例如：`ai-cost-calculator`）
2. 上传 `index.html` 文件到仓库
3. 进入仓库 Settings → Pages
4. Source 选择 `main` 分支，点击 Save
5. 等待几分钟后，访问 `https://你的用户名.github.io/ai-cost-calculator`

### 方法二：通过命令行部署

```bash
cd cost-calculator
git add index.html README.md
git commit -m "Initial commit: AI cost calculator"
git branch -M main
git remote add origin https://github.com/你的用户名/ai-cost-calculator.git
git push -u origin main
```

然后在 GitHub 仓库设置中启用 Pages。

## 技术栈

- 纯 HTML + CSS + JavaScript
- 使用 localStorage 保存历史记录
- 无需后端服务器

## 修改管理员密码

编辑 `index.html`，找到这一行：

```javascript
const ADMIN_PASSWORD='admin123';
```

改成你想要的密码即可。

## 更新模型价格

如需更新模型价格，编辑 `index.html` 中的 `modelPrices` 对象。

## License

MIT
