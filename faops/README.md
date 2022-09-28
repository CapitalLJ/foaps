faops版本及功能：

```bash
Usage:     faops <command> [options] <arguments>
Version:   0.8.21

Commands:
    help           print this message
    count          count base statistics in FA file(s) 
    #count 对每一个read进行碱基数量读取和长度读取
    size           count total bases in FA file(s)
    #size 统计每一个read的长度
    masked         masked (or gaps) regions in FA file(s)
    # masked  将每一个read中的串联重复或低复杂度的序列区域显示出来
    frag           sub-sequences from a FA file
    #frag	从序列中提取子序列	
    #命令行：faops frag ufasta.fa<输入文件> 22 57<起始 终止> out.fa<输出文件名称>
    #当一个fasta文件中有多个read时，只读取第一个。
    
    rc             reverse complement a FA file
    # 反向补码 faops rc ufasta.fa<输入文件>  out.fa<输出文件名称>
    #-r 将序列反向输出 -n 不改变标题的名称
    #-c 序列的补码输出 -f 只对fasta文件中list文件中的标题序列进行操作fa'o'p
    
    one            extract one fa record
    # 从序列中提取记录（read）
    # faops one ufasta.fa read0 out.fa
    
    some           extract some fa records
    #从序列中提取记录（reads）
    # faops some ufasta.fa list out.fa
    #-i Invert 反转，输出不在列表中的序列。
    
    order          extract some fa records by the given order
    #按给定的顺序从序列中提取记录（reads）
    #如果list 为read2 read1 ；order会按照2 1的顺序；但是some会拍成1 2 的顺序。
    #
    replace        replace headers from a FA file
    #更改序列标题的名称 （read0 》》 111）
    #faops replace ufasta.fa rep（read0  "tab"	111) out.fa 
    #faops order [options] <in.fa> <list.file> <out.fa>
    #list.file格式    original_name       replace_name 
    
    filter         filter fa records
    #按照条件对序列进行筛选，通常针对序列大小等，名称可以通过some命令
    #faops filter 查看命令选项介绍
    #  faops filter [options] <in.fa> <out.fa>
    #-a INT 筛选序列长度至少大于INT
    #-z INT 筛选序列长度不大于INT
    #-n INT 筛选序列的N碱基数小于INT
    #-u 删除重复的id，保留第一个
    #-b  pretend to be a blocked fasta file 实际操作生成的文件格式更规则
    #-N 把不确定的模糊碱基全换成N
    #-d  remove dashes '-'
    #-s 简化序列名称
    
    split-name     splitting by sequence names
    #根据序列名称分成一个目录，包含每个标题的序列
    # faops split-name [options] <in.fa> <outdir>
    
    split-about    splitting to chunks about specified size
    #根据序列所占的字节大小（大约）进行分类，但是在对于临界状态的判定似乎有点问题。
    # faops split-about [options] <in.fa> <approx_size> <outdir>
    #-e 一个文件中的序列一定是偶数
    #-m INT 最大的部分，当一个read的长度大于INT时，该read还是会完整读出
    
    n50            compute N50 and other statistics
    #faops n50 [options] <in.fa> [more_files.fa]  （可以放多个fasta文件。n50，反应序列的拼接效果。）
    #-H 不显示n50这个标题
    #-N INT 计算Nx的值，-N 90 表示计算N90的值
    #-S 计算得到N50时的所有条目的总和。（条目应该指参与计算n50的entries）
    #-A 计算所有条目的平均长度。
    #-E  compute the E-size (from GAGE)？？？？
    #-C 计算条目数
    #-g INT 认为输入基因组大小，而不是文件中的所有碱基读数
    
    
    
    dazz           rename records for dazz_db
    #faops dazz [options] <in.fa> <out.fa> 改变序列的标题为特定格式（>read/1/0_???）
    #此命令会删除重复的ID，默认保留第一个。
    #-p str 将read前缀改为输入的str
    #-s INT 起始索引改为INT，初始为1
    #-a 不要删除重复的ID
    
    
    interleave     interleave two PE files
    #faops interleave [options] <R1.fa> [R2.fa]
    # 交错展示两个R文件;一个文件也行，另一个展示的是'N'
    #-q  write FQ. The inputs must be FQs(FQ文件格式)
    #-p str 将read前缀改为输入的str
    #-s INT 起始索引改为INT，初始为0
    
    
    region         extract regions from a FA file
    #从fa文件中提取区域
    # faops region [options] <in.fa> <region.txt> <out.fa>
    #frag命令只能提取第一个read中的子序列，region可以提取指定read的序列
    #<region.txt>文件的格式：seq_name:begin-end[,begin-end]
    
    #-s 在标题read后面加了一个加号，read（+）
    

Options:
    There're no global options.
    Type "faops command-name" for detailed options of each command.
    Options *MUST* be placed just after command.
```



```c++

```

