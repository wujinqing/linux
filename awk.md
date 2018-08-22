## awk 笔记
功能：匹配文件的每一行，并且可以对每一行进行处理(如：切割)

### options
|参数|说明|
|---|---|
|-F|分隔符|


#### 匹配并打印hello.txt文件中所有包含字符串'zh'的行
> awk '/zh/ { print $0 }' hello.txt

#### 匹配并打印hello.txt文件中所有字符长度大于6的行
> awk 'length($0) > 6' hello.txt

#### 匹配并打印hello.txt文件中所有非空行(只包含多个空格也不行)
> awk 'NF > 0' hello.txt

#### 指定分隔符,分隔每一行里面的字符串
> echo a,b,c,d | awk -F, '{print $2}'