![logo](https://raw.githubusercontent.com/veedrin/biu/master/logo/logo.png)

<h2 align="center">BiuJS</h2>

<br>

> BiuJS是一个轻巧的mvvm框架<br>
> 它实现了数据的双向绑定<br>
> 并提供一些基本的指令帮助你提升效率，比如`$for`，`$model`，`$if`，`$click`，`$style`<br>
> 是的，如你所见，以`$`开头的指令是它的独特标识<br>
> 1000行左右的代码量，让应用的开发和加载biu的一瞬完成

## 启动

```javascript
const app = new Biu({
    mount: '#app',
    data: {
        me: 'BiuJS',
    },
    action: {
        change: function() {
            console.log('changed');
        },
    },
});
```

## 构建界面

```html
<div id="app">
    <div>{{name}} 的清单</div>
    <ol>
        <li $for="todo in todos">{{todo.text}}</li>
    </ol>
</div>
```

```javascript
const app = new Biu({
    mount: '#app',
    data: {
        name: 'biu',
        todos: [
            { text: '学习 HTML' },
            { text: '学习 CSS' },
            { text: '学习 JavaScript' },
        ],
    },
});
```

## 说明文档

1. [总体结构](https://github.com/veedrin/biu/issues/1)

2. [数据劫持](https://github.com/veedrin/biu/issues/2)

3. [文本编译](https://github.com/veedrin/biu/issues/3)

4. [$if 指令](https://github.com/veedrin/biu/issues/4)

5. [$for 指令](https://github.com/veedrin/biu/issues/5)

## License

[MIT](https://github.com/veedrin/biu/blob/master/LICENSE)
