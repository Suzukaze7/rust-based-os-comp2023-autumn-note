# 踩坑记录

此篇为了记录2023秋冬季OS训练营第二阶段中踩的坑

> 本篇没有配置环境相关内容，因为本人 wsl2 按照第零章的步骤顺序下来没出问题

1. 每一次 lab 的 `reports/` 都要带上之前所有 lab 的 report
2. 从 classroom 接收的任务仓库的`README`中说明了如何在本地进行 Grading，不要(像我一样)傻傻地反复 rerun 等着 GitHub 好几分钟才能出的结果，而且还没有报错信息。而这需要`clone` `ci-user/`与`ci-user/user/`。
3. 如果在本地 Grading 能通过而 GitHub 上出错，这通常是 GitHub 方面的问题，可以在 Actions 界面进行 rerun。
4. 为了区分两种运行方式，以下将在`user/`下运行称为`make run`，`ci-user/`下运行称为`make test`
5. 可以使用`debug!()`宏并在运行时加上`LOG=DEBUG`可以方便地通过输出来 debug
6. 有很多文档没有提及的而又很有用的函数，在实现某个功能时可以先去对应的模块里找一下是否有能拿来直接用的下层函数，通常都可以复用免去了造轮子的时间
7. 同样的，可以去找一下功能相近的函数，然后仿照去实现自己的函数
8. `ci-user/Makefile` 中第 50 行的`test: env randomize`中的`env`建议删掉，不然每次 `make test`都会删除一些工具又重新下载
9. `make test`会将所有输出都写入`ci-user/stdout-ch#`，可以查看以 debug
10. 也可以通过输出找到未通过的 test 对应的文件，通过样例找错误
11. `make test`运行后会改变`os/Makefile`里的内容以配合测试，`make test`的逻辑是先`make run`然后通过输出来寻找通过测试的提示，所以从 ch5 开始在不`make test`之前`make run`会正常运行有交互的内核，而之后就变成了只进行测试