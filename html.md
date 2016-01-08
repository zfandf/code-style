# html 编码规范

## 资源引用
保证标签属性顺序统一

* 外部类库使用时，仅作使用，不做修改（更新类库时自己修改的东西容易遗漏）
* css 引入时，引入顺序为，类库css, /public/css/, 站点自己的css 
* js文件的引用尽量靠后，减少界面出现的延迟. 保持风格统一

        <!--推荐-->
        <link type="text/css" rel="stylesheet" href="/public/libs/layer/layer.css"/>
        <link type="text/css" rel="stylesheet" href="/public/css/base.css"/>
        <link type="text/css" rel="stylesheet" href="css/user.css"/>
        <script type="text/javascript" src="/public/js/jquery-1.8.3.min.js"></script>
        <script type="text/javascript" src="/public/js/jquery-1.8.3.min.js"></script>

        <!--不推荐-->
        <link type="text/css" href="/public/css/base.css" rel="stylesheet"/>
        <link type="text/css" rel="stylesheet" href="css/base.css"/>
        <link rel="stylesheet" type="text/css" href="/public/libs/layer/layer.css"/>
        <script type="text/javascript" src="/public/js/jquery-1.8.3.min.js"></script>
        <script language="javascript" src="/public/js/jquery-1.8.3.min.js"></script>

* 不使用行内样式

        // 不推荐
        <style>.no-good {}</style>

## 元素
* 根据元素被创造出来时的初始意义来使用它。打个比方，用 h 元素来定义标题，p元素来定义文字段落，a元素来定义链接锚点，等等。
* 元素都要有始有终，除了自闭合标签，都要成对出现。
* 元素的属性，使用双引号包裹
* 元素嵌套奉行先大后小的原则，不使用行内元素包裹块级元素（在IE7及其以下，逆向使用会导致DOM中断渲染）。
* img ，如果图片地址为空，就不要写src属性，否则在某些浏览器上会向当前页面发起空请求。
* 不在元素上使用 style 属性（<hr style="border-top: 5px solid black">）

## 命名
* class class命名使用 "小写字母+中划线"（class="btn-default class-name"）， class 命名由页面同学完成，用做css选择器。
* name 如果为表单元素，并且要和后台进行数据交互，name值与需要传递给后台的数据名保持一致。
* id id 为一个元素的唯一标记，同一个页面保证id的唯一性 
* 自定义属性，使用小写形式，多个单词之间用中划线隔开，标签的自定义属性通常由js同学添加，在js中使用。例如：

        <input custom-type="">

* js同学也可以添加自己的 class 或者 id, 用于在js中操作元素绑定事件等等，这个时候统一命名，比如: id="J_ActivityName" 或者 class="J_PrizeSelect"。这样页面同学修改页面的时候也会知道那个class是属于他的。

## 表单
* 表单元素如果用到标记，使用label标签，而不是其它标签代替。
* 牵涉到提交时，使用form包裹，按钮 type="submit", 保证直接按 enter 键或者手机上的完成键可以提交。

    Demo

        <form>
            <label>用户名</label>
            <input type="text" name="username">
            <br>
            <label>密码</label>
            <input type="password" name="password">
            <br>
            <input type="submit" value="提交">
        </form>