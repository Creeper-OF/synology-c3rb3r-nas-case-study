# 参考资料与外部收录

以下资料核对于 2026-10-29。外部案例只说明其作者报告的结果，不代替本机证据。

| 来源 | 本报告使用范围 |
| --- | --- |
| [soimy/c3rb3r-rescue，固定 commit 130933a95bf823bafc998a9d122b055075660319](https://github.com/soimy/c3rb3r-rescue/tree/130933a95bf823bafc998a9d122b055075660319) | 参考事件报告组织方式、候选验证思路和适用性边界；对其公开材料进行了本机样本验证 |
| [Synology-SA-24:20 DSM (PWN2OWN 2024)](https://www.synology.com/en-global/security/advisory/Synology_SA_24_20) | CVE-2024-10441 的厂商描述及 DSM 7.2.1 分支修复版本；不作为本机确实遭该漏洞利用的直接证据 |
| [Ryan Emmons / Rapid7：Disguise delimit，DEF CON 33 白皮书](https://assets.contentstack.io/v3/assets/blte4f029e766e6b253/bltad0709de42b54e82/689604359f008cdd02f69917/disguise-delimit-whitepaper.pdf) | `LD_DEBUG_OUTPUT` 的 `.PID` 文件名机制和 DSM 插件环境变量注入路径；用于解释本机残片 |
| [Benjamin-zlt/c3rb3r-baremetal-rescue，固定 commit 906e81293153341f162ee1f176722d93ba1d8358](https://github.com/Benjamin-zlt/c3rb3r-baremetal-rescue/tree/906e81293153341f162ee1f176722d93ba1d8358) | 物理机上保留存活加密进程并提取会话材料的案例；5 项自测与本机 24,120 文件尾交叉验证分别记录 |
| [Linux v4.4.302：zsmalloc](https://github.com/gregkh/linux/blob/v4.4.302/mm/zsmalloc.c)、[zram 结构](https://github.com/gregkh/linux/blob/v4.4.302/drivers/block/zram/zram_drv.h) | 核对类字段、页链、句柄和交换设备元数据；结合本机数据验证 |
| [Linux v4.4.302：x86-64 页表](https://github.com/gregkh/linux/blob/v4.4.302/arch/x86/include/asm/pgtable_64.h) | 修正本机交换 PTE 编码；没有把原始 4.4 的表达式当作补丁版本的实现 |
| [Nashub：Synology C3RB3R 事件跟踪](https://nashub.vn/posts/synology-ransomware-c3rb3r-lock3d) | 10 月 29 日条目链接本仓库，列为第四个公开取证案例；只用于记录外部收录 |

本轮补充一手来源：

- [Ericality 在 Issue #6 的 ext4 补充](https://github.com/soimy/c3rb3r-rescue/issues/6#issuecomment-6495836088)：精确投递 URL、来源属性和清理行为的跨案例比对；本机结论来自独立副本分析。
- [Linux ext4 扩展属性](https://www.kernel.org/doc/html/latest/filesystems/ext4/attributes.html)与 [inode 文档](https://www.kernel.org/doc/html/latest/filesystems/ext4/inodes.html)：命名空间、外部属性块及 inode 解释。

本机事实来源为所有者私有取证记录，其脱敏定位见[证据索引](../evidence/evidence-index.json)。本仓库独立撰写，不复制参考项目的长段文字、源码或恢复密钥。仓库没有重新声明第三方材料的许可。
