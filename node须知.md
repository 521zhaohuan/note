## node内存溢出问题
表现为node服务经常崩溃，浏览器显示内存不足
### 解决方案是
1、
```"script": {
"pro": "node --max_old_space_size=9000 build/build.js" // package.json文件中
}
2、
``` "devDependencies": {
"increase-memory-limit": "^1.0.6"
}
"scripts": {
"fix-memory-limit": "cross-env LIMIT=4096 inscrease-memory-limit"
}
// npm run fix-memory-limit之后再重新启动
3、
安装最新版的node
