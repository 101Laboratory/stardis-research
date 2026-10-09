# Stardis 毕业研究成果工作区

蒲昱岐（EricPu / EricSolshkov）的毕业研究归档，发布于 **101Laboratory**。原始 Stardis 是法国 **Meso-Star 团队**的工作；本成果在此基础上完成 Windows/CMake 迁移、早期 cus3d 探索、OptiX s3d 后端、混合 Wavefront 求解器及 GUI 编辑器。

## 一次获取完整工作区

```bash
git clone --recurse-submodules https://github.com/101Laboratory/stardis-research.git
```

```text
stardis-research/
├── stardis-oxs3d/    # CPU/GPU 实现、研究分支、文档、场景、实验与数据索引
├── stardis-editor/   # 场景编辑器及测试
└── thesis/           # 完整 LaTeX 源工程及必要插图
```

普通 clone 不会填充子模块；已克隆时执行 `git submodule update --init --recursive`。本仓库通过三个固定提交锁定互相配套的版本，不自动追踪各子项目最新分支。更新时先 pull 总仓库，再执行同一子模块命令。

## 阅读顺序

1. [发布方案与归属](PUBLICATION_PLAN.md)：项目边界、历史与数据策略。
2. [论文](thesis/README.md)：方法、实验和总结。
3. [CPU/OptiX 求解器](stardis-oxs3d/README.md)：构建入口、研究文档与数据。
4. [场景编辑器](stardis-editor/README.md)：交互式场景与任务工作流。
5. [发布状态](RELEASE_STATUS.md)：已经验证的内容与尚存限制。

大型原始数据位于 stardis-oxs3d 的版本化 Release，不随初次 clone 下载；其下载脚本按哈希验证并恢复原路径。论文只发布源工程，不发布整篇 PDF、编译中间文件或本地环境。

## 历史和版本

CPU Windows 迁移历史与全部 GPU 研究分支统一在 stardis-oxs3d 内；worktree 不另建项目。编辑器保留已有历史，论文使用干净源码发布历史，模板源码连同局部修改直接提供。各组件的原作者、上游许可和素材来源保持不变。

本标签是研究档案，不代表所有实验分支和历史结论都已重新验证。特别是 CPU 早期嵌套仓库的部分历史对象仍缺失，求解器当前机器构建也有环境限制，详见发布状态。
