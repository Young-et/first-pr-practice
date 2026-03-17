# 维护者：如何开启 PR 自动合并

本仓库的「Validate PR」工作流会对每个 PR 做自动检查。通过后可由你选择**自动合并**，无需人工点 Merge。

## 步骤

1. **允许 Auto-merge**  
   仓库 **Settings → General → Pull Requests** → 勾选 **Allow auto-merge**。

2. **设置分支保护（main）**  
   **Settings → Branches → Add rule**：
   - Branch name: `main`
   - 勾选 **Require status checks to pass before merging**
   - 在列表里勾选 **Validate PR**（或 "validate" job 名称）
   - 可选：勾选 **Require branches to be up to date before merging**
   - 保存

3. **在具体 PR 上启用自动合并**  
   打开某个 PR → 若检查已通过，可点击 **Enable auto-merge** → 选择 **Merge when pipeline succeeds**。  
   之后该 PR 会在「Validate PR」通过后自动合并。

若希望**所有通过检查的 PR 都自动合并**，可额外使用 GitHub Action（如 `peter-evans/enable-pull-request-automerge-action`）在 CI 通过后自动为该 PR 启用 auto-merge（需自行添加 workflow）。
