# javascript ����淶

## js��ʽ
����js��ִ�д��붼��������������С�

    $(function(){

    });

## ����
* ��ȫ��д�ķ�ʽ������֮�����»��߸��������磺THIS_IS_CONST

## ����
* ÿ��������������Ҫ���� var �ؼ��֣������ָ���ؼ��� var, �ñ����ͻᱩ¶��ȫ��������(window)�У� ��ܿ��ܻḲ��ȫ���������е�ͬ������
* ȫ�ֵı�������Сдǰ׺g, ���磺 gImageUrl
* ������Ϊjquery�����ʱ����$������Ϊ��ͷ�����磺$name = $('#name'); ��jquery����Ҫ��$����ͷ��
* js�ڲ�ʹ�ñ�������ʹ���շ���ʽ�����磺 imageUrl, userFilialeId
* ����ajax�����ı�����������Ҫ���ݵĲ���������һ��
* ���飨array���Ͷ���object���������ǰ׺������ǰ׺�ͻ�֪���ñ�����������߱��������磺

        var aList = [], // ����
            oParams = {}; // ����

* ��������Ҫ���󣬼���ʶ�⡣����ѭ�����߼�������ʹ�õ���ĸ��i, j, k, v..�������������磺

        var len = aList.length;
        for (var i = 0; i < len, i++) {
            // TODO 
        }

## �ַ���
* �ַ���һ��ʹ�õ����ţ�js�кܶ�ʱ���д��htmlԪ�أ���htmlԪ�ص����Ծ���ʹ��˫���Ű��������磺 

        sBtn = '<button class="btn btn-default">***</button>';

* �����ַ���ʹ�� + ƴ����ʽ��

## ����
### ����
* �Է�����ȡֵ����ǰ׺Ϊ"fetch/saveFuncName..."���磬fetchUserListById: function(){...};
* �Ա���ȡֵ��ǰ׺"get/setFuncName...", �磬getParams��function(){...};  setParams��function(oParam){...};
* �ж��Ƿǵĺ���ǰ׺Ϊ"isFuncName...",  �磺 function isFuncName() {}

## ע��
ע�Ͷ������˶��죬��Ȼ�����Ĵ��벻дע��Ҳ���Կ�������ͨ�÷�������д��ע�ͣ����������ʹ�á�

## ������
    var a = 0;
    $('#id').click(function() {

    }); // ��Ҫ���Ƿֺ�
    var obj = {
        'a': 1,
        'b': 2 // �˴���Ҫ��Ӷ��ţ� IE�ᱨ��
    };
## �ո�
�ʵ���ӿո���ǿ����Ŀɶ��ԡ�
* ��ֵ����>, <, = �ȵȣ�������ӿո�
* �����ж�����������ǰ�������ź���ӿո񣬱��� if-else, while, for ������

        for (var i = 0; i < 100, i++) {
            if (i > 0) {
                i = 1;
            }
        }
        while (i < 10) {
            i++;
        }

## ����

* �ַ����ĺϲ�, ����ַ����ϲ����� '+' �ķ�ʽЧ�ʵͣ��Ƽ����·�ʽ

    ����1��

        var arr = [];
        arr[0] = "hello";
        arr[1] = "world";
        var str = arr.join("");

    ����2��

        // ����������
        function StringBuffer () {
            this._strings_ = [];
        }
        StringBuffer.prototype.append = function(str) {
            this._strings_.push(str);
        };
        StringBuffer.prototype.toString = function() {
            return this._strings_.join("");
        };
        // ʹ�ã�
        var buffer = new StringBuffer ();
        buffer.append("hello ");
        buffer.append("world");
        var result = buffer.toString();

* jquery���󣬶ദ��ʹ��ĳһjquery����ʱ��������ǰ���ö��󸳸�һ����������ֹ�ظ�����Ԫ�ء�

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

## ����
* ��ʽ��飺JSLint (http://www.jslint.com/)
     �ο��� http://www.jslint.com/

* ��Ԫ���ԣ�jsunit
     �ο�: http://llying.iteye.com/blog/258605

## ����
* ѹ��  ��С���룬���Ϳɶ��ԣ�JSMIN

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