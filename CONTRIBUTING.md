# 如何贡献

## 第一次提 PR？按这个来

1. 点击本仓库右上角 **Fork**，复制到你的账号下。
2. 克隆**你的 fork**（不要克隆原仓库）：
   ```bash
   git clone https://github.com/你的用户名/first-pr-practice.git
   cd first-pr-practice
   ```
3. 新建分支（分支名建议 `add-你的用户名`）：
   ```bash
   git switch -c add-你的用户名
   ```
4. 用任意编辑器打开 `Contributors.md`，在**列表中间**（不要在最上面或最下面）加一行：
   ```markdown
   - [你的用户名](https://github.com/你的用户名)
   ```
5. 保存后提交并推送：
   ```bash
   git add Contributors.md
   git commit -m "Add 你的用户名 to contributors"
   git push -u origin add-你的用户名
   ```
6. 在 GitHub 上打开你的 fork，点击 **Compare & pull request**，填写 PR 标题（如 "Add 你的用户名 to contributors"），提交 PR。

## 自动检查说明

每个 PR 都会自动运行「Validate PR」工作流，检查：

- 是否只修改了 `Contributors.md`
- 是否只新增了一行
- 新增行是否符合 `- [用户名](https://github.com/用户名)` 的格式

检查通过后 PR 会显示绿色勾，维护者可以合并或启用自动合并。

## 遇到问题？

- 检查失败：确认只改了 `Contributors.md` 且只加了一行，格式正确。
- 冲突：从原仓库拉取最新 main 再 rebase 或 merge 后推送。
