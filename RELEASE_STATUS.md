# 发布状态 2026-10-09

已公开发布。总仓库通过 `components.json` 和 Git 子模块固定三个配套源码版本；总入口与三个子项目的 `publication-v1` 标签标识本次源码归档。

- [总入口](https://github.com/101Laboratory/stardis-research)：递归克隆获得 stardis-oxs3d、stardis-editor、thesis 三个主目录。
- [研究数据 Release](https://github.com/101Laboratory/stardis-oxs3d/releases/tag/research-archive-2026-10-09)：15 个压缩分卷，共 5,258,585,586 字节（约 4.90 GiB），GitHub 端大小和 SHA-256 全部与本地一致；2,981 个归档成员已在本地逐文件解压校验。
- 公开下载验证：使用全新克隆内的下载脚本，不提供账号凭据，下载并恢复 optimization 数据集，26 个文件全部通过哈希校验。
- 全新公开递归克隆验证：811 份 Git 研究资料的 SHA-256 全部通过，文档目录无失效文件链接，论文未混入整篇生成 PDF、中间文件或环境。见 [克隆报告](validation/fresh-clone.json) 和 [附件清单](validation/data-assets.json)。
- 编辑器：86 项任务执行相关测试通过。
- 论文：隔离 LaTeX 源工程编译成功，保留原有重复页面目标警告；整篇 PDF、编译中间文件和环境未发布。
- CPU/GPU 新构建：当前机器缺少可用 MSVC C++ 工具链，CMake 配置未通过，未做求解器运行验证。
- 历史缺口：CPU 旧嵌套模块的 27 个不同提交对象未在父库中找到，现存源码和父仓库历史已保留。归属和缺口见核心仓库的出版说明。
- 凭据检查：常见模式扫描未发现匹配，非穷尽式审计。

原始 Stardis 属于法国 Meso-Star 团队；Windows/CMake 迁移、cus3d 探索、OptiX s3d 后端、混合 Wavefront 求解器和编辑器工作按各仓库说明区分归属。

本次为研究档案发布，保留成功、失败与未完成实验，不宣称所有历史分支或结果已重新验证。大型数据通过脚本按需恢复，数据 Release 的早期标签用于固定附件；最终配套源码以 `components.json` 中的 `publication-v1` 提交为准。
