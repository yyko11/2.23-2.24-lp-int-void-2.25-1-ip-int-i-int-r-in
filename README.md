2.23

不可以


2.24

因为lp的类型不是int，而void定义了一个空指针，可以接受任意类型的对象。


2.25

1:ip是一个int类指针型的，i是一个int型的变量，r是一个int型的引用。

2;i是一个int型的变量，ip是一个空指针。

3：ip是一个int类型的指针，ip2是一个int类型的变量。


2.35

第一个auto  j  类型为int

第二个auto  &k 类型为const int &

第三个auto *p类型为const int *

第四个auto j2类型为const int

第五个auto &k2 类型为const int&3.4

字符串比较：
#include <iostream>
#include <string>
using namespace std;
void main()
{	
	string mystring1 , mystring2;
	cin>>mystring1>>mystring2;
	if (mystring1 != mystring2)
	{
		cout<<(mystring1 >= mystring2 ? mystring1 : mystring2)<<endl;
	}
	
}

测试：


字符串长度比较：
#include <iostream>
#include <string>
using namespace std;
void main()
{	
	string mystring1 , mystring2;
	cin>>mystring1>>mystring2;
	if (mystring1.size() != mystring2.size())
	{
		cout<<(mystring1.size() >= mystring2.size() ? mystring1 : mystring2)<<endl;
	}
	else
	{
		cout<<"The length of these strings are the same!"<<endl;
	}	
}

测试结果：


3.5

#include <iostream>
#include <string>
using namespace std;
void main()
{	
	string mystring;
	string sumstring;
	while (getline(cin ,mystring))
	{
		sumstring += mystring;
		cout<<sumstring<<endl;
	}
}	


#include <iostream>
#include <string>
using namespace std;
void main()
{	
	string mystring;
	string sumstring;
	while (getline(cin ,mystring))
	{
		sumstring = sumstring+mystring+" ";
		cout<<sumstring<<endl;
	}
}
3.20
#include <iostream>
#include <string>
#include <vector>
using namespace std;
void main()
{	
	vector<int> My_vector;
	int a[10];
	for (int i = 0;i<10;i++)
	{
		cin>>a[i];
	}
	for (int j = 0;j<10;j++)
	{
		My_vector.push_back(a[j]);
	}
	int sum[10];
	for (int k = 0;k<10;k++)
	{
		sum[k] = My_vector[k] + My_vector[k+1];
		cout<<sum[k]<<endl;
		k++;
	}
} 
3.23

#include <iostream>
#include <string>
#include <vector>
using namespace std;
void main()
{	
	vector<int> text(10,5);
	for (auto it = text.begin(); it != text.end();it++) 
	{
		*it = *it * 2;
		cout<<*it<<endl;	
	}
} 

3.10
#include <iostream>
#include <string>
#include <vector>
using namespace std;
 
int exchange(int &val1, int &val2)
{
	int a;
	a = val1;
	val1 = val2;
	val2 = a;
	return 0;
}
void main()
{	
	cout<<"请输入需要交换的两整数:";
	int val1,val2;
	cin>>val1>>val2;
	cout<<"交换之前的两数："<<val1<<" "<<val2<<endl;
	exchange(val1,val2);
	cout<<"交换之后的两数："<<val1<<" "<<val2<<endl;
}

6.19：

(a)：函数只有一个参数，传入两个不合法

(b)：合法

(c)：合法

(d)：合法

6.30
30：返回值的类型必须与函数类型相同(void对应无返回值)

Non-void function 'str_subrange' should return a value. // error #1
Control may reach end of non-void function. // error #2

7.16
知识点1：需要控制的类的相关操作—类成员的初始化、拷贝、赋值、销毁对象

知识点2：private隐藏类的相关实现细节，实现封装。

7.24
Screen() = default; // 1
Screen(pos ht, pos wd) : height(ht), width(wd), contents(ht * wd, ' ') {} // 2
Screen(pos ht, pos wd, char c) : height(ht), width(wd), contents(ht * wd, c)
{
} // 3

7.27
27：知识点：返回引用的函数为左值，返回*this的函数，返回本函数修改后的对象本身而非对象的副本。这样的话就会出现函数的重复使用，如下：

myScreen.move(4, 0).set('#').display(std::cout);

7.49
(a)合法 
(b)不合法，Salesdata&类型与Salesdata类型之间不可转换 
(c)不合法，const不对，因为combine本身是需要改变传入参数的

