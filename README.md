# C--
这里有个疑问为什么我用中文名命名repository一直显示already exists in this account?
我懂了因为汉语字符居然在命名后显示为空。。。坑啊。。
#include<stdio.h>
int main(){
	char ac[5]={0,1,2,3,4};
	int ai[5]={0,1,2,3,4,};
	char *p=ac;
	int *q=ai;
	printf("p-q=%d",p-q);
	return 0;
} 
运行结果是报错[Error] invalid operands of types 'char*' and 'int*' to binary 'operator-'

下面再附上指向不同数组但类型相同的指针的测试结果


#include<stdio.h>
int main(){
	int ac[5]={0,1,2,3,4};
	int ai[5]={0,1,2,3,4,};
	int *p=ac;
	int *q=ai;
	printf("%p\n",ac);
	printf("%p\n",ai);
	printf("p-q=%d",p-q);
	return 0;
} 

这个代码不会报错，两指针相减会有一个结果，在我的电脑上全定义char开头输出结果16，全定义int输出8
