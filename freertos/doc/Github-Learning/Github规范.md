## 提交
#### 1.提交注释规范
	格式：<类型>(<范围>): <主题>
	使用动词开头，如 Add login page、Fix bug in header
	不要写模糊描述如 “update”
	引用相关 Issue：Fixes #12

| 类型         | 说明       | 示例                                      |
| ---------- | -------- | --------------------------------------- |
| `feat`     | 新功能      | feat(auth): add OAuth login             |
| `fix`      | 修复 Bug   | fix(cart): fix price calculation        |
| `docs`     | 文档更新     | docs(readme): update installation guide |
| `style`    | 代码格式调整   | style(button): fix indentation          |
| `refactor` | 重构（非新功能） | refactor(api): simplify request handler |
| `test`     | 测试用例     | test(user): add login test cases        |
| `chore`    | 构建/工具更新  | chore(deps): upgrade lodash to v4       |

## 分支
#### 1.推送流程
以下为简化版流程

	创建功能分支 -> 合并feature/user-auth -> 合并release/v1.2.0 -> 合并到主分支
	main
	↑ 
	release/v1.2.0 
	↑ 
	feature/user-auth

#### 2.创建分支
	git checkout 分支名（切换到某分支）
	git checkout -b feature/登陆功能（创建并切换到一个名为 feature/登陆功能 的新分支）
输入你新分支的名字，需要遵循分支命名规范
![[image-8.png]]

#### 3.切换分支
切换分支之前，一定要把修改的东西先提交或者撤销，否则会切换不成功
![[image-9.png]]

#### 4.合并分支
打开git graph，可以看到仓库分支代码提交的作者、日期、分支创建、合并等等信息

| 主分支（长期存在）         |      |                   |
| ----------------- | ---- | ----------------- |
| 分支名               | 用途   | 说明                |
| `main` / `master` | 主分支  | 生产环境代码，必须稳定       |
| `develop`         | 开发分支 | 集成分支，功能完成的代码      |
| `release/*`       | 发布分支 | 准备发布的版本，只做 bug 修复 |
| **临时分支（完成即删除）**   |      |                   |
| `feature/*`       | 功能分支 | 开发新功能             |
| `hotfix/*`        | 修复分支 | 紧急修复生产环境 bug      |


[Git命名规范_git分支命名规范-CSDN博客](https://blog.csdn.net/iku_n/article/details/150393126?ops_request_misc=%257B%2522request%255Fid%2522%253A%25222124a8c6b780ba2778bbe724e6fad7e4%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=2124a8c6b780ba2778bbe724e6fad7e4&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduend~default-2-150393126-null-null.142^v102^pc_search_result_base1&utm_term=git%E5%91%BD%E5%90%8D%E8%A7%84%E8%8C%83&spm=1018.2226.3001.4187)
[如何在VsCode中使用git（免敲命令版本！保姆级！建议收藏！）_vscode git-CSDN博客](https://blog.csdn.net/lijiemeiyyds/article/details/148380409?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522adad2cf6b8f02bd541e688571a7fa604%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=adad2cf6b8f02bd541e688571a7fa604&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduend~default-1-148380409-null-null.142^v102^pc_search_result_base1&utm_term=vscode%E4%BD%BF%E7%94%A8git%E6%8F%92%E4%BB%B6&spm=1018.2226.3001.4187)



