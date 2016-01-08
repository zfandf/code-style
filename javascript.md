# javascript 编码规范

## js格式
所有js的执行代码都包裹在下面代码中。

    $(function(){

    });

## 常量
* 用全大写的方式，单词之间用下划线隔开，例如：THIS_IS_CONST

## 变量
* 每个变量的声明都要加上 var 关键字，如果不指定关键字 var, 该变量就会暴露在全局作用域(window)中， 这很可能会覆盖全局作用域中的同名变量
* 全局的变量，加小写前缀g, 比如： gImageUrl
* 当变量为jquery对象的时候，以$符号作为开头，比如：$name = $('#name'); 非jquery对象不要以$符开头。
* js内部使用变量命名使用驼峰形式，比如： imageUrl, userFilialeId
* 进行ajax交互的变量命名与需要传递的参数名保持一致
* 数组（array）和对象（object）命名添加前缀，看到前缀就会知道该变量是数组或者变量，比如：

        var aList = [], // 数组
            oParams = {}; // 对象

* 变量命名要形象，见文识意。除了循环或者计数，不使用单字母（i, j, k, v..）变量名，比如：

        var len = aList.length;
        for (var i = 0; i < len, i++) {
            // TODO 
        }

## 字符串
* 字符串一律使用单引号，js中很多时候会写入html元素，而html元素的属性均是使用双引号包裹。例如： 

        sBtn = '<button class="btn btn-default">***</button>';

* 多行字符串使用 + 拼接形式。

## 函数
### 命名
* 对服务器取值函数前缀为"fetch/saveFuncName..."，如，fetchUserListById: function(){...};
* 对本地取值的前缀"get/setFuncName...", 如，getParams：function(){...};  setParams：function(oParam){...};
* 判断是非的函数前缀为"isFuncName...",  如： function isFuncName() {}

## 注释
注释多少因人而异，虽然简明的代码不写注释也可以看懂，但通用方法必须写明注释，方便调用者使用。

## 标点符号
    var a = 0;
    $('#id').click(function() {

    }); // 不要忘记分号
    var obj = {
        'a': 1,
        'b': 2 // 此处不要添加逗号， IE会报错
    };
## 空格
适当添加空格，增强代码的可读性。
* 赋值符（>, <, = 等等）两边添加空格。
* 条件判断语句的左括号前和右括号后添加空格，比如 if-else, while, for 。。。

        for (var i = 0; i < 100, i++) {
            if (i > 0) {
                i = 1;
            }
        }
        while (i < 10) {
            i++;
        }

## 性能

* 字符串的合并, 多个字符串合并，用 '+' 的方式效率低，推荐以下方式

    方法1：

        var arr = [];
        arr[0] = "hello";
        arr[1] = "world";
        var str = arr.join("");

    方法2：

        // 定义如下类
        function StringBuffer () {
            this._strings_ = [];
        }
        StringBuffer.prototype.append = function(str) {
            this._strings_.push(str);
        };
        StringBuffer.prototype.toString = function() {
            return this._strings_.join("");
        };
        // 使用：
        var buffer = new StringBuffer ();
        buffer.append("hello ");
        buffer.append("world");
        var result = buffer.toString();

* jquery对象，多处会使用某一jquery对象时，可以提前将该对象赋给一个变量，防止重复查找元素。

        var $name = $('name');
        $name.click(function() {
            // TODO
        });
        $.ajax({
            data: {
                name: $name.val()
            },
            success: function() {
                alert($name.val());
            }
        });

## 调试
* 格式检查：JSLint (http://www.jslint.com/)
     参考： http://www.jslint.com/

* 单元测试：jsunit
     参考: http://llying.iteye.com/blog/258605

## 发布
* 压缩  减小代码，降低可读性：JSMIN

## CODE DEMO

	var IMAGE_PREFIX = 'http://example.com/image/';
	var aSelectImages,
		oUploadFiles;

	$(function() {
		// 
	});

	var namespace = {
		initPage: function(){
			$('#xx').click(function() {

			});
		},
		foo2: function(){
			var oParam = {};
			oParam.action = 'xx';
			oParam.name = 'iamdemo';
			namespace.ajaxPost(oParam);
		}
	   ajaxPost: function(oParam){
		   $.ajax({
			   type: 'POST',
			   url: 'ajax/ajax_demo.php',
			   data: oParam
			   sucess: function(data){
				   if (oParam.action='xx') {
					   // 
				   } else if(oParam.action='yy') {

				   } 
			   }
	   });
	}