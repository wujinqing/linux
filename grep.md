## grep 笔记

[官方文档](https://www.gnu.org/software/grep/manual/grep.html)

### 格式
> grep options pattern input_file_names

### options
|参数|说明|
|---|---|
|-i|忽略大小写|
|-w|匹配单词|
|-C|限定打印匹配行的前后行的行数，除了会输出匹配行还会输出匹配行的前后行|
|--color|用红色标记匹配字符串|

### 示例

#### 匹配文件hello.txt中所有包含字符串'zh'的行(-i表示忽略大小写)
> grep -i 'zh' hello.txt

#### 匹配所有以.txt结尾且内容包含字符串'java'的文件
> grep -l 'java' *.txt

#### 匹配所有包含完整单词'zhangsan'的行
> grep -w 'zhangsan' hello.txt

#### 输出匹配行及匹配行的前后2行
> grep -C 2 'mazi' hello.txt

#### 输出既包含字符串'zh'也包含字符串'liu'的行
> grep 'zh' hello.txt | grep 'liu'

#### 匹配空行
> grep '^$' hello.txt




















