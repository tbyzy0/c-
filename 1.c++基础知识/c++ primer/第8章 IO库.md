### **IO类**
I 向程序输入，即从控制台、文件读取
O 从程序读出，即写入文件、控制台
**iostream** 读写流
istream ostream iostream
**fstream** 读写文件
ifstream ofstream fstream
**sstream** 读写string
istringstream ostringstream stringstream
ps:IO对象无拷贝和赋值

### **缓存刷新**
* 程序正常结束
* 缓存区满
* endl刷新
* 读写被关联的流时，关联到流的缓冲区会被刷新（如cin和cout）

### **文件操作**
```c
fstream f;//定义一个文件流对象
fstream f(s);//定义一个文件流对象，并打开名为s的文件
fstream f(s，mode);//定义一个文件流对象，并按指定mode打开名为s的文件
f.open(s);//打开名为s的文件
f.close();//关闭文件
f.is_open()；//文件是否打开
```

### **模式操作**
in 以读方式打开
out 以写方式打开 默认截断文件 文件原有内容会被丢弃
app 追加 定位到文件末尾 文件不会截断
trunc 截断文件
binary 以二进制的方式打开

### **string流**
```c
sstream s;//定义一个stringstream流对象
sstream s(s1);//定义一个stringstream流对象,保存string s1的一个拷贝
s.str();//返回s中保存的string拷贝
s.str(s1);//将string s1拷贝到s中，返回void

```

### **istringstream**
很神奇
```c
string line,word;
while(getline(cin,line)){//输入一行
	istringstream record(line);
	while(record>>word){//处理一行中的每个单词
	}
}
```



