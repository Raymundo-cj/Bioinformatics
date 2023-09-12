### 序列处理工具|seqkit

seqkit是一款专门处理fasta/q序列文件的软件，自己使用感觉速度很快，不用额外写python代码

### 1.安装方法

通过conda安装

```
conda install -c bioconda seqkit
```
参数截图：

![image](https://github.com/Raymundo-cj/Bioinformatics/assets/64938817/aad66c4a-27d2-4b67-9450-58ed191f51b9)

目前用到的命令总结：

1.Seq

```
seqkit seq name_fasta_file.fasta #查看 fa文件
seqkit seq name_fasta_file.fqsta #查看fq文件
seqkit seq name_fasta_file.fasta -n #打印序列全名
seqkit seq name_fasta_file.fasta -n -i #打印序列名的唯一标识
seqkit seq name_fasta_file.fasta -n -i --id-regexp "^[^\s]+\s([^\s]+)\s" #打印ID中的第二个字段
seqkit seq name_fasta_file.fasta -s -w 0 #只打印序列（-w定义输出行宽，0不换行，默认为60）
seqkit seq name_fasta_file.fasta -r -p #反向互补（-r 序列反向；-p序列互补）
```

2.replace 使用正则表达式替换name以及sequence

参数描述：
name：描述行；sequence：序列行；seqid:name 第一个空格前的ID号；descriptions:name 第以空格后的部分。
-p: --pattern string 正则表达式 ； -r： --replacement string 替换

2.1 name前面或者后面添加字符

seqkit replace -p ^ -r prefix_ test.fasta > 



