��js�У�����Ҳ��һ������

1 argumentsֻ���ں����ڲ�ʹ�ã���ָ������������Ĳ�����������Array����������Array.����Ҫ����;������д��ѡ�����ĺ���������
function abs(a,b,c){
	if(arguments.length==2){
		c=b;
		b=null;
	}
}
ͨ���˷����ɽ��м�Ĳ���b�����Ե���

2 rest����
����ES6�����ı�׼��һ�����飬���Ի�ȡ����Ĳ���
function abs(a,b,...rest){
	console.info(rest);
}

3 let�鼶������ const �������峣����������ES6�������ı�׼

4 ��������һ�������а󶨺������ͽ����������󶨵������ϵķ�������ͨ�ĺ���û��ʲô���𣬵��������ڲ�ʹ����һ��this�ؼ��֡�����ں����ڲ�ʹ��this�ؼ��֣�����ָ�������أ����������������
var xiaoming={
	name:"xiaoming",
	birthdy:1995,
	age=function(){
		var y=new Data().getFullYear();
		return y-this.birthdy;
	}
}
xiaoming.age; //function xiaoming.age()
xiaoming.age(); //�õ�ʵ�ʵ�����
������������У�thisָ����xiaoming������������������ڴ��������
var getAge=function(){
	var y=new Data().getFullYear();
	return y-this.birthdy;
}

var xiaoming = {
    name: 'С��',
    birth: 1990,
    age: getAge
};

xiaoming.age(); //ʵ������
xiaoming.age;  //[function:getAge]
getAge();  //error
����������У��ڵ�������getAge()ʱ��thisָ����ȫ�ֱ���,��window.
�ܽ᣺����Զ������ʽ����this,��ָ��ǰ�������Ķ��󣬵�������ʱ���ָ��ȫ�ֶ������ϸ�ģʽ�£�this��ʱҲ��ָ��undefine.
����Ա�����Լ�����this��ָ�򣬷�������ʹ�ú����Դ���apply����call����������
getAge.apply(xiaoming,[]);  //apply��������������һ����this��Ҫ��thisָ��Ķ��󣬵ڶ����Ǻ����Լ��Ĳ������������������
call������apply�������ƣ�Ψһ������apply�Ѳ��������Array���룬call��˳���롣

5 �հ�
����˵���Ǻ����ķ��ؽ������һ���������հ��и���ǿ��Ĺ��ܣ��ڱ�������У�����ʹ��private������һ���ڲ���������js��û��class���ƣ�ֻ�к���������޷�ʹ��private,�����ǿ���ʹ�ñհ�ʵ�ִ˹��ܡ����⻹���԰Ѷ�������ĺ�����Ϊһ��������

��ͷ����

generator(������) ����������һ�����Է��ض�εĺ���
function* foo(x){
	yield x+1;
	yield x+2;
	return x+3;
}