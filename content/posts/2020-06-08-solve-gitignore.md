---
title: "解决.gitignore无法生效的问题"
date: 2020-06-08T21:32:07+08:00
draft: false
---

使用git的过程中, 为了避免垃圾文的上传,我们可以手动配置`.gitignore`排除一些文件或文件夹.

## 配置`.gitignore`

- 排除文件`.DS_Store`, 排除文件夹`node_modules/`

```undefined
.DS_Store
dist/
node_modules/
```

## 使用git



```csharp
# 第一步: git初始化
git init
# 第二步: 将除了.gitignore之外的文件添加到git缓存区
git add .
# 第三步: 将git缓存区的文件添加到仓库
```

------

> 这时, 有了新的需求, 我们需要排除dist文件夹的内容, 你也许会说,这还不简单, 在`.gitignore`里面新增`dist/`不就可以了?

------

> 其实当项目进行到一半的时候, 直接修改`.gitignore`是不会立刻生效的, 我们需要先把缓存区清空, git才会重新读取`.gitignore`的新规则, `.gitignore`才会真正生效, 而清空缓存的命令也很简单...

```bash
#清空缓存(注意最后有个点)
git rm -rf --cached .
```

- 清空缓存之后, 我们只需重新进行`git add .`, 将待管理的文件添加到缓存区即可!
- 运行`git add.`后, 我们可以通过`git status`验证排除效果



> 作者：zhaoolee
> 链接：https://www.jianshu.com/p/ddd248164a5d
> 来源：简书