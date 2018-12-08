# img2webp

一个将 PNG、JPG、JPEG、BMP 等格式的图像文件批量 (递归) 转换为 webp 格式的 Python 脚本

可以设定转换程度 (0 ~ 100)，数字越大品质越好。支持无损压缩。

可以在 GNU/Linux 上运行，Mac OS 估计也可以 (没测试过)，Windows 上可能要修改一下才能用 (主要是目录地址中 `/` 与 `\` 的区别)

> 想了想将项目名称改成了 `img2webp`，这样就可以少打两个字了 \_(:з」∠)\_

## 依赖

- Python3

- webp


## 使用方法

```shell
python3 picture2webp.py [options] [value]
```
## 参数 (options)

支持以下参数：

| 参数 | 默认值 | 描述 |
|:---:|:-----:|:-----|
| -q |80|与 `cwebp` 中相同。表示压缩的程度 (0 ~ 100)，数字越大品质越好。|
| -lossless |-|与 `cwebp` 中相同。无损压缩。|
| -i |当前目录|需要转换的文件所在的目录，会递归进行转换。|
| -o |[输入目录]/output|`*.webp` 文件的输出目录。<br>输出目录结构与输入目录保持一致。<br>如果输出不存则会按照给定的路径新建文件夹。<br>如果缺省，则会在指定的输入目录中新建并输出到目录 `output`|

## TODO

- 并发转换
- 支持 Windows
- 支持更多的参数

