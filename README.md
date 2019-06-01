## WeChat-Markdown

###  微信公众号 Markdown 格式化工具

> 使用微信公众号编辑器有一个十分头疼的问题——粘贴出来的代码，格式错乱，而且特别丑。这块编辑器能够解决这个问题。

## 预览地址：[https://md.52lhd.com](https://md.52lhd.com/)

### Changelog

- 适配 Android
- 支持代码不转行，横向滚动条
- 支持页面主题样式配置

### 代码示例

```javascript
var OnlineMarkdown = {
  init: function() {
    var self = this;
    self.load().then(function() {
      self.start()
    }).fail(function(){
      self.start();
    });
  },
  start: function() {
    this.updateOutput();
  },
  load: function() {
    return $.ajax({
      type: 'GET',
      url: params.path || './demo.md',
      dateType: 'text',
      timeout: 2000
    }).then(function(data) {
      $('#input').val(data);
    });
  },
  updateOutput: function () {
    var val = this.converter.makeHtml($('#input').val());
    $('#output .wrapper').html(val);
    PR.prettyPrint();
  }
};

OnlineMarkdown.init();
```
---

上面是 `JavaScript`，下面是 `java`：

```java
echo 'hello,world'
```

### 表格示例

| 品类 | 个数 | 备注 |
|-----|-----|------|
| 苹果 | 1   | nice |
| 橘子 | 2   | job |



### 鸣谢

- 小胡子哥（插件原作者）：https://github.com/barretlee

### 关于我

![微信公众号](https://md.52lhd.com/imgs/qrcode.png)



