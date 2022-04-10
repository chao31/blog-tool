---
title: 低code
tags:
---
1.组件库
![](./1.png)
数据
```json
[{
  key: 0,
  type: 'banner',
  name: '横幅图片',
  cid: 0
}, {
  key: 2,
  type: 'popWin',
  name: '挂件',
  cid: 0

}, {
  key: 3,
  type: 'runLight',
  name: '老虎机',
  cid: 1
}]
```
将上面的数据塞入下面，渲染出compslist
```json
{
  showName: '通用组件',
  name: 'Common',
  key: 0
}, {
  showName: '游戏组件',
  name: 'Games',
  key: 1
}, {
  showName: '应用列表',
  name: 'Applist',
  key: 3
}, {
  showName: '奖品组件',
  name: 'Awards',
  key: 4
}, {
  showName: '相关页面组件',
  name: 'subpages',
  key: 5
}, {
  showName: '积分商城',
  name: 'IntegralComps',
  key: 6
}
  ```

1.[import语法](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Statements/import)
```js
import defaultExport from "module-name";
import * as name from "module-name";
import { export } from "module-name";
import { export as alias } from "module-name";
import { export1 , export2 } from "module-name";
import { foo , bar } from "module-name/path/to/specific/un-exported/file";
import { export1 , export2 as alias2 , [...] } from "module-name";
import defaultExport, { export [ , [...] ] } from "module-name";
import defaultExport, * as name from "module-name";
import "module-name";
var promise = import("module-name");//这是一个处于第三阶段的提案。
```

2. [webpack的cmd、amd、import的使用](https://webpack.docschina.org/api/module-methods/)

3. [手动打包一个应用程序](https://www.youtube.com/watch?v=UNMkLHzofQI)
[实时创建一个简单打包工具](https://www.youtube.com/watch?v=Gc9-7PBqOC8)
[一个简单打包工具的详细说明](https://github.com/ronami/minipack)
[可见](https://webpack.docschina.org/concepts/)

4. 为什么要提取vendor
将第三方库(library)（例如 lodash 或 react）提取到单独的 vendor chunk 文件中，是比较推荐的做法，这是因为，它们很少像本地的源代码那样频繁修改。因此通过实现以上步骤，利用 client 的长效缓存机制，命中缓存来消除请求，并减少向 server 获取资源，同时还能保证 client 代码和 server 代码版本一致。 


5.[name].[contenthash].js
[filename](https://webpack.docschina.org/configuration/output/#outputfilename)

6.[bundle分析](https://webpack.docschina.org/guides/code-splitting/)
[官方分析](https://github.com/webpack/analyse)

7.--env参数
[webpack CLI 文档](https://webpack.docschina.org/api/cli/#environment-options)