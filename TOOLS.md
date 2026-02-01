# TOOLS.md - Local Notes

Skills define *how* tools work. This file is for *your* specifics — the stuff that's unique to your setup.

---

## 📍 重要位置

### Allen 的家（主机位置）
- **地址：** 江苏省无锡市滨湖区太湖街道融创星光广场
- **坐标：** 120.28023335205711, 31.484230718577805
- **查询示例：**
  ```bash
  # 周边餐厅
  mcporter call @amap/amap-maps-mcp-server.maps_around_search keywords:"餐厅" location:"120.280233,31.484231" radius:"1000" --output json

  # 天气查询
  mcporter call @amap/amap-maps-mcp-server.maps_weather city:"无锡" --output json
  ```

---

## What Goes Here

Things like:
- Camera names and locations
- SSH hosts and aliases  
- Preferred voices for TTS
- Speaker/room names
- Device nicknames
- Anything environment-specific

## Examples

```markdown
### Cameras
- living-room → Main area, 180° wide angle
- front-door → Entrance, motion-triggered

### SSH
- home-server → 192.168.1.100, user: admin

### TTS
- Preferred voice: "Nova" (warm, slightly British)
- Default speaker: Kitchen HomePod
```

## Why Separate?

Skills are shared. Your setup is yours. Keeping them apart means you can update skills without losing your notes, and share skills without leaking your infrastructure.

---

Add whatever helps you do your job. This is your cheat sheet.

## Important Paths

### Jedi's Folders
- **Working Folder:** `/Users/allen/Documents/Jedi` - 可以自由操作，用于临时文件、脚本等
- **Output Folder:** `/Users/allen/Nutstore Files/01/Jedi` - 保存输出文档（md等），自动同步到云端，跨平台可访问
  - 用途：保存报告、指南、文档等需要长期保留和跨设备查看的内容
  - 特性：坚果云自动同步，可在手机/平板/其他电脑上查看
  - 示例：`OpenClaw迁移指南.md` 已保存在此

## Development Preferences

### Python
- **默认版本：** Python 3.12
- **运行命令：** `python3.12` 或 `python3.12 -m pip`
- **代码要求：** 确保在 Python 3.12 上运行，使用 3.12 兼容的语法特性

## GitHub

- **GitHub 账号：** jerkallen
- **本地 Git 配置：** Allen (89628895@qq.com) ✅
- **gh CLI 状态：** 未登录 ❌（需要 `gh auth login`）
- **可以使用 GitHub 仓库** 进行代码开发
- **规则：**
  - ✅ 可以新建项目
  - ❌ 不要动原来的项目
- **注意事项：**
  - 🔒 API keys 绝不能上传到 GitHub
  - 🔐 敏感配置文件要加入 .gitignore

## 阿里云服务器

- **服务器 IP：** 47.110.156.72
- **用户：** root
- **私钥路径：** `~/.ssh/aliyun.pem` (权限 600)
- **已部署项目：**
  - LearnWithDaniel (英语单词学习助手) - http://47.110.156.72
- **系统：** Ubuntu 24.04 (Linux 6.8.0-63-generic)
- **Python：** 3.12.3
- **Web 服务器：** Nginx + Gunicorn
- **进程管理：** Supervisor
- **注意事项：**
  - 🔒 私钥极其敏感，绝不外传
  - ✅ 可以自主使用此密钥连接服务器进行部署和维护
