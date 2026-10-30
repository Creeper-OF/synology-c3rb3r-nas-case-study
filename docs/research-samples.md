# C3RB3R 研究样本附件

设备所有者于 2026-10-30 明确授权公开这批恶意样本，供防御研究和独立复核。附件在 [GitHub Release](https://github.com/Creeper-OF/synology-c3rb3r-nas-case-study/releases/tag/research-samples-20261030) 发布，Git 源码历史继续仅保存文档与结构化记录。

**附件包含真实勒索程序、下载器和投递脚本，执行可能加密或破坏数据。仅在隔离分析环境中使用合成数据，不挂载生产目录、NAS 或原始业务数据。** 本次整理、校验和上传均未执行样本。

## 下载和校验

- [研究样本 Release](https://github.com/Creeper-OF/synology-c3rb3r-nas-case-study/releases/tag/research-samples-20261030)
- 归档：`c3rb3r-research-samples-20261030.zip`，3,473,238 字节
- 格式：AES-256 加密 ZIP，需要支持 AES ZIP 的读取工具
- **公开密码：`infected`**。密码用于避免无意读取或运行，不提供保密性
- 归档 SHA-256：`61525d7ec4796cc2938a0e995daf566cdb7aa8ed0bac94ef52d899c0399691db`
- [逐样本清单](../evidence/research-sample-manifest-20261030.json)，Release 同时附有 `sample-manifest.json`、`SHA256SUMS.txt` 和 `README_RESEARCH.md`

先核对下载归档 SHA-256，再按清单核对内部文件。可以只读取解密后的字节进行哈希和静态分析，无需执行样本。每个样本文件名追加 `.sample`，Unix 权限为 `0400`；这些措施不能代替隔离环境。

## 精确发布范围

| 内容 | 数量 | 形式 |
| --- | ---: | --- |
| 原始架构载荷 | 8 | `packed/xdy5.*.sample` |
| 原始投递脚本 | 1 | `packed/xdy5.sh.sample` |
| 已验证的脱壳产物 | 2 | `unpacked/*.sample` |
| 归档内说明和清单 | 2 | `README_RESEARCH.md`、`MANIFEST.json` |

样本内容没有修改，原文件名、类型、字节数及 SHA-256 均记录在清单中。归档重读检查覆盖每个成员；无密码和错误密码均无法读取样本。

原始载荷取自所有者提供的投递节点留存件；本次打包没有连接该节点。已提供的脱壳产物按实际字节和摘要发布，不声称所有脱壳工具版本都能得到完全相同的布局。脚本、命令和字符串作为证据保存，不作为使用说明执行。

附件不包含受害者内存、swap、账号、凭据、会话密钥、认证日志、对话、业务文件或任何恢复数据。原始取证包和 NAS 保全目录继续私有。

这些文件用于恶意软件分析，不是解密器，也不提供受害者解密密钥。样本身份、服务器时间线和密码学勘误见[复核报告](payload-node-review-20261030.md)。研究或滥用相关联系方法见 [SECURITY.md](../SECURITY.md)。
