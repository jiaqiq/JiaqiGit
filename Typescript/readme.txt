1.΢������javascript�ĳ�������ѭES6
2.ES�ǿͻ��˽ű����ԵĹ淶��javascriptʵ����ES5�淶��Typescriptʵ����ES6�淶��
3.Typescript�����ơ�
��1��֧��es6�淶��2015������δ��һ��ʱ�佫�ǿͻ��˽ű����Ե�������
��2��ǿ���IDE֧�֣����ͼ�飬�﷨��ʾ���ع��ĺô���ߴ���������������߿���Ч�ʡ�
��3��Angular2�Ŀ������ԣ��ܸ��õİ���ѧϰangular2.
�typescript����������
��Ҫcompiler ��es6ת��es5.
npm install -g typescript

typescript���﷨������

�ַ���������
1.�����ַ�����˫��1����ߵ��Ǹ��㡣
2.�ַ���ģ�棬�ڶ����ַ������������� �� ������
3.�Զ�����ַ�����

����������

1.�������� var name: string = 'aaaaa'; 
2.�����ƶϻ��ƣ�var alias =  'haha'; alias = 13����ǰ�渳ֵΪ�ַ�����ts���Զ��ƶ������͡�
3.����Ϊany �������κ����ͣ�
����number,boolean,void(����Ҫ����ֵ)
4.�Զ�������  ����ͬ��class  interface������
����Ĭ��ֵ�� �ŵ�����棻
��ѡ���� �����ã�����  ��ѡ�������������ڱ�ѡ�������棻

����������
A.
Rest and  Spread��������
�����������������ķ�������
������ǣ�...��
1.
function fun1(...args){
	args.forEach(function (arg)){
	console.log(arg);
   }
}
fun1(1,2,3);
fun1(7,8,9,10,11);

2. ������
function fun1(a,b,c){
console.log(a);
console.log(b);
console.log(c);

}

var args = [1,2];

fun1(...args);

var args = [7,8,9,10,11];

fun1(...args2);

B.
generator������
���ƺ�����ִ�й��̣��ֹ���ͣ�ͻָ�����ִ��
function* doSomething(){
	console.log('start');
	yield; //�൱�ڶϵ㣬ִ�е��˻�ͣס��
	console.log('finish');
}�������generator,ͨ���Ǻţ�

var fun1 = dosomething();

fun1.next();

fun1.next();

�������ʽ 
�Ӷ����в����
1.function getStock(){
	return {
	code: "IBM",
	price: 100
   }
}

var {code, price} = getStock();
console.log(code);
console.log(price);

2.function getStock(){
	return {
	
	code: 'IBM',
	price: {
	 price1: 200,
	 price2: 400
	}
     }
}

var {code: codex, price: {price2}}=getStock();
console.log(codex);
console.log(price2);

�������в����
var array1 =  [1,2,3,4];

var [number1, number2] = array1;//�ó�1,2
var [number1, , ,number2] = array1;//�ó�1,4
var [, ,number1, number2] = array1;//�ó�3,4
var [number1, number2, ...others] = array1;
function doSomething([number1, number2, ...others]){
console.log(number1);
console.log(number2);
console.log(others);	
}
doSomething(array1);

��ͷ���ʽ
������������������������ͳ����������thisָ�����⣻
var sum = (arg1, arg2) => arg1 + arg2;//һ��
var sum = (arg1, arg2) => {
   return arg1 + arg2; 
}//������Ҫ�����ź�return
var sum = () => {
    
}//�޲���
var sum = arg1 => {
    console.log(arg1);
}//һ������

var myArray = [1, 2, 3, 4, 5];

console.log(myArray.filter(value => value%2 == 0));

for of ѭ��

���Ե�����desc,������break;
var myArray = [1, 2, 3, 4];
myArray.desc = 'four number';

myArray.forEach(value => console.log(value));

for (var n in myArray) {
    console.log(n);//����±�key: 0,1,2,3 desc
    console.log(myArray[n]);//���ֵ
}

var myArray = [1, 2, 3, 4];
myArray.desc = 'four number';

for (var n of myArray) {
    if (n > 2) break;//����break;
    console.log(n);//���ֵ1,2,3,4
}
for (var n of "four number") {
    console.log(n);
}

�����������

�ࣨclass��
class Person {

	constructor(public name: string) {
	//��new��ʱ��ֻ�ܵ�һ��,���봫��name,��������������ʿ��Ʒ�
	}

}
var p1 = new Person();
var p2 = new Person();
���ʿ��Ʒ��� public�����У� private��˽�У�   protected���ܱ����ģ�����������ڲ���������౻���ʣ����ⲿ�����ԣ�

��ļ̳�
extends
class Employeee extends Person {
//�̳�Person Ҳ���������µ����Ժͷ���

    constructor(name: string, code: string) {
     	super(name);//���๹�캯��������ø��๹�캯��
	this.code = code;
      }
}

���ͣ�generic��<Person>
�����������ͣ� һ���������Ƽ��ϵ�����
var workers: Array<Person> = [];
workers[0] = new Person("zhang san");

�ӿ� interface
��������ĳ�ִ���Լ����ʹ�������������ڵ���ĳ�������򴴽��µ���ʱ������ѭ�ӿ�������Ĵ���Լ��

interface IPerson {
    name: string;
    age: number;

}

class Person {
    constructor(public config: IPerson) {
        
    }
}

var p1 = new Person({
    name:"zhang san",
    age: 18
});

interface Animal {
    eat();
}//��������ʵ������ӿڵ����࣬����ʵ������ӿڵķ���

class Sheep implements Animal {
    //���������ʵ��Animal����ӿ�
    eat() {
        console.log("i eat grass");
    }
}

class Tiger implements Animal {
    eat() {
        console.log("i eat meat");
    }
}

module ģ��
export import

�����������
���Ͷ����ļ���*.d.ts��

���Ͷ����ļ���������������zai Typescript��ʹ�����е�javascript�Ĺ��߰�  �磺JQuery

����https://github.com/DefinitelyTyped/DefinitelyTyped

typings
https://www.npmjs.com/package/typings 















