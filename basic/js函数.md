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

