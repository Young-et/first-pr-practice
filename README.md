# 第一次 PR 练习

一个**专为新手**准备的仓库：只改一行、提一个 PR，由 **机器人自动检查**，通过即可合并（可配置自动合并）。

## 你要做的事（3 步）

1. **Fork** 本仓库  
2. 在你的 fork 里编辑 **`Contributors.md`**，在列表中间**加一行**你的信息（不要加在文件最开头或最末尾）  
3. 提 **Pull Request**

格式（把 `你的GitHub用户名` 换成你的）：

```markdown
- [你的GitHub用户名](https://github.com/你的GitHub用户名)
```

## 规则（自动检查会校验）

- ✅ **只允许改** `Contributors.md` 这一个文件  
- ✅ **只能新增一行**，且格式为：`- [用户名](https://github.com/用户名)`  
- ✅ 用户名只能包含字母、数字、连字符 `-`  
- ❌ 不能删改别人的行，不能改其他文件  

通过检查后，PR 会显示绿色 ✓；维护者可配置**自动合并**，无需人工 review。

## 本地操作示例

```bash
# 克隆你自己的 fork（把 YOUR_USERNAME 换成你的 GitHub 用户名）
git clone https://github.com/YOUR_USERNAME/first-pr-practice.git
cd first-pr-practice

# 新建分支
git switch -c add-YOUR_USERNAME

# 编辑 Contributors.md，在中间加一行你的信息后保存

# 提交并推送
git add Contributors.md
git commit -m "Add YOUR_USERNAME to contributors"
git push -u origin add-YOUR_USERNAME
```

然后在 GitHub 上打开你的 fork，点 **Compare & pull request** 创建 PR。

## 维护者：如何开启自动合并

1. **Settings → General → Pull Requests**：勾选 **Allow auto-merge**  
2. 在 **Settings → Branches** 添加 Branch protection rule（main）：  
   - 勾选 **Require status checks to pass**，选择 workflow「Validate PR」  
   - 可选：勾选 **Require branches to be up to date**  
3. 合并时在 PR 页选择 **Enable auto-merge** → 「Merge when pipeline succeeds」  

这样符合条件的 PR 会在检查通过后自动合并。

## License

MIT
