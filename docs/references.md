# 一手参考资料

以下资料核对于 2026-10-29。外部案例只说明其作者报告的结果，不代替本机证据。

| 来源 | 本报告使用范围 |
| --- | --- |
| [soimy/c3rb3r-rescue，固定 commit 130933a95bf823bafc998a9d122b055075660319](https://github.com/soimy/c3rb3r-rescue/tree/130933a95bf823bafc998a9d122b055075660319) | 参考事件报告组织方式、候选验证思路和适用性边界；对其公开材料进行了本机样本验证 |
| [Synology-SA-24:20 DSM (PWN2OWN 2024)](https://www.synology.com/en-global/security/advisory/Synology_SA_24_20) | CVE-2024-10441 的厂商描述及 DSM 7.2.1 分支修复版本；不作为本机确实遭该漏洞利用的直接证据 |
| [Ryan Emmons / Rapid7：Disguise delimit，DEF CON 33 白皮书](https://assets.contentstack.io/v3/assets/blte4f029e766e6b253/bltad0709de42b54e82/689604359f008cdd02f69917/disguise-delimit-whitepaper.pdf) | `LD_DEBUG_OUTPUT` 的 `.PID` 文件名机制和 DSM 插件环境变量注入路径；用于解释本机残片 |

本机事实来源为所有者私有取证记录，其脱敏定位见[证据索引](../evidence/evidence-index.json)。本仓库独立撰写，不复制参考项目的长段文字、源码或恢复密钥。仓库没有重新声明第三方材料的许可。
