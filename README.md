# Typecho SMMS 图床插件

一个支持 SM.MS 图床的 Typecho 插件，可以将上传的图片同步保存到 SM.MS 图床和本地服务器。

## 功能特点

- 自动上传图片到 SM.MS 图床
- 本地备份功能，防止图床失效
- 支持检测重复图片，避免重复上传
- 统一的本地存储目录管理
- 返回 SM.MS 的图片直链，支持 CDN 加速
- 支持多张图片批量上传
- 支持一键插入 Markdown 或 HTML 格式
- 图片管理面板，支持预览和删除
- 自动记录图片尺寸信息
- 显示上传数量统计
- 支持图片全屏预览
- 支持快速复制图片链接
- 显示多图上传进度

## 安装方法

1. 下载本插件，解压后将文件夹重命名为 `SMMS`
2. 将插件上传到 Typecho 的 `/usr/plugins/` 目录下
3. 登录管理后台，在"控制台"→"插件"中找到 "SMMS"，点击"启用"
4. 在插件设置中填入你的 SM.MS API Token

## 配置说明

- **API Token**: 必填项，在 [SM.MS](https://sm.ms/) 注册账号后获取 [Token 获取地址](https://sm.ms/home/apitoken)
- **服务器域名**: 选择 SMMS 图床的服务器域名
  - smms.app (国内域名，推荐)
  - sm.ms (国外域名)
- **本地存储目录**: 可选项，设置图片同步到本地的存储目录名，位于 /usr/uploads/ 下，留空则不保存到本地

## 使用方法

1. 在文章编辑页面右侧可以看到新增的"图床"标签页
2. 点击"选择图片上传"可以选择单张或多张图片上传
3. 上传完成后可以在列表中看到图片预览
4. 每张图片支持以下操作：
   - 点击"插入"将图片以 Markdown 格式插入文章
   - 点击"插入 HTML"将图片以 HTML 格式插入文章
   - 点击"删除"可以同时删除远程和本地的图片

## 注意事项

1. 确保 PHP 运行环境支持 CURL 扩展
2. 确保本地存储目录具有写入权限
3. 上传的图片会同时占用本地存储空间和 SM.MS 的空间配额
4. 免费版 SM.MS 有每日上传限制，请注意控制上传数量，详见 [SM.MS 定价](https://sm.ms/pricing/)

## 常见问题

**Q: 上传失败怎么办？**
A: 请检查：

- API Token 是否正确
- 网络连接是否正常
- 图片大小是否超出限制
- 是否超出当日上传限额

**Q: 为什么要本地备份？**
A: 为了防止图床服务不稳定或者图片被删除，本地备份可以作为应急方案。

## 更新日志

### v1.1.0

- 新增图片管理面板
- 支持批量上传功能
- 添加一键插入 Markdown/HTML 功能
- 记录并显示图片尺寸信息
- 添加上传数量统计
- 新增图片全屏预览功能，支持 ESC 快捷键关闭
- 支持点击图片名称快速复制图片链接
- 新增上传进度显示
- 优化新建文章时的图片关联逻辑
- 优化上传体验和错误提示

### v1.0.0

- 初始版本发布
- 支持基础图片上传功能
- 支持本地备份
- 支持重复图片检测

## 开源协议

本插件采用 MIT 协议开源。

## 致谢

感谢 [SM.MS](https://sm.ms/) 提供的图床服务。
