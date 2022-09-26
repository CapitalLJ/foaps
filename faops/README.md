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
    
    rc             reverse complement a FA file
    # 反向补码 faops rc ufasta.fa<输入文件>  out.fa<输出文件名称>
    one            extract one fa record
    # 从序列中提取记录（read）
    # faops one ufasta.fa read0 out.fa
    
    some           extract some fa records
    #从序列中提取记录（reads）
    # faops some ufasta.fa list faops out.fa
    
    order          extract some fa records by the given order
    #按给定的顺序从序列中提取记录（reads）
    #如果list 为read2 read1 ；order会按照2 1的顺序；但是some会拍成1 2 的顺序。
    replace        replace headers from a FA file
    #更改序列标题的名称 （read0 》》 111）
    #faops replace ufasta.fa rep（read0  "tab"	111) out.fa 
    
    filter         filter fa records
    split-name     splitting by sequence names
    split-about    splitting to chunks about specified size
    n50            compute N50 and other statistics
    dazz           rename records for dazz_db
    interleave     interleave two PE files
    region         extract regions from a FA file

Options:
    There're no global options.
    Type "faops command-name" for detailed options of each command.
    Options *MUST* be placed just after command.
```



```c++

```

