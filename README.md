# commitlint-husky
### 安装commitlint
``
yarn add @commitlint/{config-conventional,cli} --dev  
``  
创建配置文件commitlint.config.js,如果使用的ts语言，后缀换成.ts
```
module.exports = {
    extends: ['@commitlint/config-conventional']
}
```

### 安装husky
``
yarn add husky --dev
``  
激活hooks,会产生一个.husky目录，存放git钩子要执行的命令  
``
yarn husky install
``  
添加commit-msg钩子,.husky目录下会多一个commit-msg文件  
``
yarn husky add .husky/commit-msg
``  
修改.husky/commit-msg文件，加入校验commit message内容的命令  
``
npx --no -- commitlint --edit $1 或者
yarn commitlint --edit $1
``