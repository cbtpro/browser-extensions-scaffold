# 新建一个package
lerna create 包名

# 将本地宝链接在一起,以节省空间,并安装剩余的依赖
lerna bootstrap

# 修改版本
lerna version

# 列出本地包
lerna list

# 列出子上次标记发布以来本地更改的包
lerna changed

# 比较自上次发布以来的所有包或单个包
lerna diff [包]

# 在每个包中执行任意命令
```shell
$ lerna exec -- <command> [..args] # runs the command in all packages
$ lerna exec -- rm -rf ./node_modules
$ lerna exec -- protractor conf.js
```

# 在包含该脚本的每个包中运行 npm 脚本
```shell
$ lerna run <script> -- [..args] # runs npm run my-script in all packages that have it
$ lerna run test
$ lerna run build

# watch all packages and transpile on change, streaming prefixed output
$ lerna run --parallel watch
```
