# idshwk7

### 目录结构

|       文件名      |      文件内容     |
| :--------------: | :--------------: |
|    LSBSteg.py    | 信息隐藏、提取脚本  |
| requirements.txt |  运行脚本所需依赖  |
|   original.jpg   |      原始图像     |
|     test.txt     |     ID & 姓名    |
|     test.png     |  隐藏信息后的图像  |

### Setup

``` shell
pip3 install -r requirements.txt
```

### 隐藏信息
- 利用LSB隐写法，将图片的最低有效位替换为待隐藏信息的二进制编码。

#### 具体操作流程
``` shell
cd idshwk7
python3 LSBSteg.py encode -i original.jpg -o test.png -f test.txt
```

### 提取信息
- 提取图片的最低有效位，用来恢复信息。

#### 具体操作流程
``` shell
python3 LSBSteg.py decode -i test.png -o decode.txt
cat decode.txt
```
