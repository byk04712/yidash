## yidash（易大师）一万个JavaScript实用方法库

`警告⚠️`：未发布 **v2.0.0** 之前，均为不稳定版本，慎用！！！

![logo](https://static.yicode.tech/logo/yidash-logo.png)

## 🏠 官网

[文档官网 https://yidash.dev](https://yidash.dev)

## 🛖 仓库

[github https://github.com/chenbimo/yidash](https://github.com/chenbimo/yidash)

## 🧊 安装

```bash
npm install yidash
# 或
pnpm add yidash
```

## 🍼 使用

`注意⚠️`：本项目暂时只提供 `ESM` 包。

```javascript
import { yd_tree_array2Tree, yd_regexp_trainNumber, yd_number_validNumber } from 'yidash';
console.dir(
    yd_tree_array2Tree([
        { id: 1, pid: 0 },
        { id: 2, pid: 1 },
        { id: 3, pid: 2 }
    ])
);
console.dir(yd_regexp_trainNumber);
const validNumber = yd_number_validNumber();
console.log(validNumber(1.111)); // 1.11
console.log(validNumber(1.571333)); // 1.57
console.log(validNumber('1..221333')); // 1.22
console.log(validNumber('1.2213.33')); // 1.22
console.log(validNumber('1.')); // 1.
console.log(validNumber('1.2')); // 1.20
console.log(validNumber('1.2.')); // 1.20
```

## 🎁 贡献和福利

### **贡献者交流群**

加笔者微信 `chensuiyime`，注明 `yidash` ，拉你进微信交流群。

群内将解答关于代码贡献相关的问题。

### **代码贡献步骤**

1. 访问本仓库。
2. fork本仓库。
3. 拉取fork后的仓库。
4. 修改代码。
5. push代码。
6. 发起pull request。
7. 等待笔者验证与合并。

**注意**：只提交lib中的函数到本仓库合并即可，其他文件不要提交。

### **不能这样做**

1. 不能引入很多包，需要导包的函数要与我沟通确认，尽量不依赖第三方包。
2. 不能写很复杂的函数，不能超过500行，要小而美。
3. 每个文件的作者，一经提交，其他人后续修改也不能改其原作者。

### **必须这么做**

1. 必须写 `JSDoc注释`，不然别人看不懂，不知道怎么用。
2. 必须写 `函数作者`，标签为 `@author`。
3. 必须写 `案例说明`，标签为 `@example`。
4. 必须写 `测试用例`，在 `test目录` 下，与 `lib目录` 中的结构一一对应。
5. 必须 `4格缩进`，不喜欢的请不要参与本项目。
6. 必须按 `git提交格式` 写清楚提交信息。
7. 必须 `一个函数一个文件`，不能多个导出函数写到一个文件中。
8. 函数名称必须清楚地表达函数作用。
9. 函数必须使用 `default` 默认导出，且导出的必须是一个 `箭头函数`。
10. 能用 `const` 定义的地方尽量用 `const`。
11. 不能使用 `var` 定义变量。
12. `不要炫技`，用尽量简单易懂的方式，宁愿多写几行，也不要增加理解难度。

### **没有这些玩意**

1. 没有 `TypeScript`。
2. 没有 `Eslint`。

### **函数开发规则**

`lib` 目录下，每一个目录是一个函数类型集合。

每个目录下，不能再创建目录，只能创建函数文件。

函数名称尽量简短且清楚地表达函数的作用。

对外导出的函数名称 = 前缀 + 目录 + 函数。

比如 `lib/is/array.js` 函数，则其对外导出的函数名称是 `yd_is_array`。

这个函数名称会自动生成，不要手动书写。

### **git提交格式**

`提交主题: 提交具体内容`

举例：

-   `完善功能: yd_is_number函数增加判断机制`
-   `代码重构: yd_number_thousands重新设计`
-   `新增函数: 增加yd_is_array函数`

### **贡献者福利**

1. 增加开源参与度。
2. 体会开源的乐趣。
3. 为自己的职业经历增加一个彩蛋。
4. 你的函数将会被每一个使用yidash的人看到。
5. 额外获得VSCode扩展fnMap永久注册码一枚。

**fnMap地址**：`https://marketplace.visualstudio.com/items?itemName=chensuiyi.fn-map`。

1. 每个注册用户可以免费领取一个永久注册码（登录自动领取）。
2. 每个贡献者可以额外领取一个（私聊我即可）。
