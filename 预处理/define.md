�궨��
=======
�����÷������ǲ��ᡣ  
## #
һ������`#`���ַ���������˼����ν�ַ����������ǽ�����ת��Ϊ�ַ�����  
���磺
```c
#include <stdio.h>

#define PRINT(x) printf(#x" ��ֵ�� %s\n",x)
#define PRINT2(x) printf("x ��ֵ�� %s\n",x)
int main()
{
	char * var = "hello world";
	PRINT(var); //��ӡvar��ֵ�� hello world
	PRINT2(var);//��ӡx��ֵ�� hello world
}
```
>����������в��ܽ�#xд������֮�У���*printf(#x" ��ֵ�� %s\n",x)*�����򽫴�ӡ#x ��ֵ�� hello world��  
Ҳ���ܽ�x��ֵд���������棬��printf(x" ��ֵ�� %s\n",x)�������ᱣ����Ϊprinf�ĵ�һ�������������ַ����� 

## ##
��������`##`�������궨���У���**���ӷ�**�����á�
�ǽ��������ߵ��ַ����ӵ�һ��ע����������֮�����ɵ���**����**���������ַ�����  
���磺
```c
#include <iostream>
#define TEST(c) test##c
int main()
{
	int test1=123;
	std::cout<<TEST(1)<<std::endl;
}
```
������ȷ��ӡ������test1��ֵ��
>��ν���ţ������ַ���������ָ�ı����������������������������ȵȡ�

����Ȥ�������ǣ�
```c
#include <iostream>
#define TEST(c) test[##c]
int main()
{
	int test[10];
	for(int i=0;i<10;i++)
		test[i]=i;
	for(int i=0;i<10;i++)
		std::cout<<TEST(i)<<std::endl;
}
```