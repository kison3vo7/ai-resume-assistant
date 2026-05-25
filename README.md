# AI 简历助手 - 部署指南

## 项目介绍
一款面向年轻人的 AI 简历优化 + 面试模拟 + 岗位匹配度分析工具。单页 HTML 应用，无需后端即可运行。

## 快速部署到 Vercel（建议方案）

### 第一步：创建 GitHub 仓库
1. 打开 https://github.com 并登录你的账号
2. 点击右上角 `+` → `New repository`
3. 仓库名填写 `ai-resume-assistant`
4. 选择 `Public`
5. 点击 `Create repository`

### 第二步：上传代码
**方式一（推荐 - 直接拖拽）：**
1. 进入刚创建好的仓库页面
2. 将 `index.html` 和 `vercel.json` 两个文件直接拖到浏览器页面上
3. 滚动到底部，点击 `Commit changes`

**方式二（命令行）：**
```bash
git clone https://github.com/你的用户名/ai-resume-assistant.git
cd ai-resume-assistant
# 将 index.html 和 vercel.json 复制到这个文件夹
git add .
git commit -m "初始部署"
git push
```

### 第三步：部署到 Vercel
1. 打开 https://vercel.com 并登录（建议用 GitHub 账号登录）
2. 点击 `Add New` → `Project`
3. 在 GitHub 列表中找到 `ai-resume-assistant`，点击 `Import`
4. 所有选项保持默认，直接点击 `Deploy`
5. 等待约 30 秒，部署完成！
6. Vercel 会给你一个域名，例如 `ai-resume-assistant.vercel.app`

✅ 部署完成后，任何人通过这个域名就能打开使用了！

### 第四步：绑定自定义域名（可选）
1. 在 Vercel 项目页面进入 `Settings` → `Domains`
2. 输入你拥有的域名（如 `jianli.ai`）
3. 按照提示在 DNS 管理后台添加 CNAME 记录

## 后续维护

### 更新代码
1. 修改 `index.html` 文件
2. 重新 push 到 GitHub（Vercel 会自动重新部署）

### 查看统计数据
Vercel 控制台 → `Analytics` 页面可查看访问量、来源等

## 微信小程序版本（后续）
如果想转成微信小程序，需要：
1. 注册微信小程序开发者账号（https://mp.weixin.qq.com）
2. 个人版 300 元/年，企业主体免费
3. 使用 Taro / uni-app 框架迁移代码
4. 接入微信登录 + 微信支付
5. 提交审核上线

## 技术说明
- 纯前端应用，使用 React 18 + createElement（无 JSX）
- CSS 自定义变量，无第三方 UI 库
- AI 功能支持双模式：演示模式（内置模拟数据）和 DeepSeek API 模式
- 响应式设计，适配手机 + 电脑
