# FreeMCHost 自动续期脚本

> 专为 FreeMCHost 免费 Minecraft 服务器设计的自动化工具：
> 1. **服务器唤醒（Auto Start）**：无论服务器是否开机，均点击 **Start** 开机（已开机状态无影响）。
> 2. **长效租期续期（Billing Renew）**：巡检 `PLAN: Billing` 到期时间，低于 46 小时门槛自动完成免费的 `60 hours` 租期加时。
> 3. 本脚本经超200次以上修改，终于稳定，实测仅对**Free机器(不带fast或mini)**版本单台机子适配良好。若需要多台并行或其余类型机器不适配请自行修改！

━━━━━━━━━━━━━━━━━━━━━━

### 🔐 Secrets 配置说明

| Secret 名称         | 是否必填 | 说明                                              |
|---------------------|----------|---------------------------------------------------|
| FREE_EMAIL         | ✅ 必填  | 登录邮箱                          |
| FREE_PASSWORD      | ✅ 必填  | 登录密码                          |
| SERVER_PAGE_URL    | ✅ 必填  | 服务器控制台链接,如（https://freemchost.com/app/servers/7f2d81a4-26c3-49e7-950b-4c82f16d7039）        |
| NODE_LINK          | ❌ 可选  | 代理链接（如 vless:// vmess:// trojan:// hysteria2:// tuic:// anytls:// socks5:// )|
| TG_BOT_TOKEN       | ❌ 可选  | Telegram Bot Token（用于发送通知）       |
| TG_CHAT_ID         | ❌ 可选  | Telegram Chat ID（接收通知的用户或群组 ID） |    

━━━━━━━━━━━━━━━━━━━━━━

## 注意事项
* 必填变量必须要填写
* NODE_LINK支持的代理协议有：vmess,vless,hysteria2,tuic,anytls,socks5等
* 自动续期不代表可以无底线的薅羊毛,不建议多账号
* cron运行时间不一定准确,得根据实际到期时间修改,可在设置里暂停actions功能再开启
* github定时任务队列太拥挤 为确保工作流准时且定时执行，建议自行部署CF或VPS的外部触发

## ⚠️ 免责声明
* 本程序仅供学习了解, 非盈利目的，如转载须注明来源。
* 使用本程序必循遵守部署服务器所在地、所在国家和用户所在国家的法律法规, 程序作者不对使用者任何不当行为负责。
