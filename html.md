# html ����淶

## ��Դ����
��֤��ǩ����˳��ͳһ

* �ⲿ���ʹ��ʱ������ʹ�ã������޸ģ��������ʱ�Լ��޸ĵĶ���������©��
* css ����ʱ������˳��Ϊ�����css, /public/css/, վ���Լ���css 
* js�ļ������þ������󣬼��ٽ�����ֵ��ӳ�. ���ַ��ͳһ

        <!--�Ƽ�-->
        <link type="text/css" rel="stylesheet" href="/public/libs/layer/layer.css"/>
        <link type="text/css" rel="stylesheet" href="/public/css/base.css"/>
        <link type="text/css" rel="stylesheet" href="css/user.css"/>
        <script type="text/javascript" src="/public/js/jquery-1.8.3.min.js"></script>
        <script type="text/javascript" src="/public/js/jquery-1.8.3.min.js"></script>

        <!--���Ƽ�-->
        <link type="text/css" href="/public/css/base.css" rel="stylesheet"/>
        <link type="text/css" rel="stylesheet" href="css/base.css"/>
        <link rel="stylesheet" type="text/css" href="/public/libs/layer/layer.css"/>
        <script type="text/javascript" src="/public/js/jquery-1.8.3.min.js"></script>
        <script language="javascript" src="/public/js/jquery-1.8.3.min.js"></script>

* ��ʹ��������ʽ

        // ���Ƽ�
        <style>.no-good {}</style>

## Ԫ��
* ����Ԫ�ر��������ʱ�ĳ�ʼ������ʹ����������ȷ����� h Ԫ����������⣬pԪ�����������ֶ��䣬aԪ������������ê�㣬�ȵȡ�
* Ԫ�ض�Ҫ��ʼ���գ������Ապϱ�ǩ����Ҫ�ɶԳ��֡�
* Ԫ�ص����ԣ�ʹ��˫���Ű���
* Ԫ��Ƕ�׷����ȴ��С��ԭ�򣬲�ʹ������Ԫ�ذ����鼶Ԫ�أ���IE7�������£�����ʹ�ûᵼ��DOM�ж���Ⱦ����
* img �����ͼƬ��ַΪ�գ��Ͳ�Ҫдsrc���ԣ�������ĳЩ������ϻ���ǰҳ�淢�������
* ����Ԫ����ʹ�� style ���ԣ�<hr style="border-top: 5px solid black">��

## ����
* class class����ʹ�� "Сд��ĸ+�л���"��class="btn-default class-name"���� class ������ҳ��ͬѧ��ɣ�����cssѡ������
* name ���Ϊ��Ԫ�أ�����Ҫ�ͺ�̨�������ݽ�����nameֵ����Ҫ���ݸ���̨������������һ�¡�
* id id Ϊһ��Ԫ�ص�Ψһ��ǣ�ͬһ��ҳ�汣֤id��Ψһ�� 
* �Զ������ԣ�ʹ��Сд��ʽ���������֮�����л��߸�������ǩ���Զ�������ͨ����jsͬѧ��ӣ���js��ʹ�á����磺

        <input custom-type="">

* jsͬѧҲ��������Լ��� class ���� id, ������js�в���Ԫ�ذ��¼��ȵȣ����ʱ��ͳһ����������: id="J_ActivityName" ���� class="J_PrizeSelect"������ҳ��ͬѧ�޸�ҳ���ʱ��Ҳ��֪���Ǹ�class���������ġ�

## ��
* ��Ԫ������õ���ǣ�ʹ��label��ǩ��������������ǩ���档
* ǣ�浽�ύʱ��ʹ��form��������ť type="submit", ��ֱ֤�Ӱ� enter �������ֻ��ϵ���ɼ������ύ��

    Demo

        <form>
            <label>�û���</label>
            <input type="text" name="username">
            <br>
            <label>����</label>
            <input type="password" name="password">
            <br>
            <input type="submit" value="�ύ">
        </form>