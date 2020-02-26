# Some shell skills

### Conduct a command for several times
`for i in {1..10}; do echo "Hello, World $i"; done`

### 将文本文件里的文件路径对应的文件复制到另一个目录中去
`cat <list file> | xargs -i cp {} <dst dir>` 

### others
ln -s /usr/local/lib/libopencv_core.so /usr/local/lib/libopencv_core.so.3.1 //将libopencv_core.so.3.1指向libopencv_core.so

wget "url" //download from web site

wget --user=xxx --password=xxx http://xxx.xxx.xxx.xxx/cdh3/script/ntp-.sh //带用户名及密码的下载

git config --global http.sslVerify false//在Ubuntu下使用git clone等出错很可能都是这个的问题

sudo gedit ~/.bashrc //编辑本用户的目录

source ~/.bashrc //使用户目录生效

//解决windows文件换行符‘\r\n’的问题
vi M.txt
:set fileformat=unix
:wq

//提交后台运行的指令
nohup command & //command 为自己的命令，很多时候会在nohup前加sudo

//.sh 脚本执行指令
sudo sh file.sh 

ps -u username //显示当前username的所有进程

nvidia-smi//显示当前GPU使用情况（NVIDA 驱动正常工作的情况下）
watch -n 1 nvidia-smi

//移动当前文件下的所有.jpg文件到指定目录
sudo find . -name "*.jpg" -exec mv {} ../face_lib \

apt-get install feh

feh //命令行查看图片

//默认的Ubuntu shell 解释器是dash，而dash不支持c风格的一些操作，
//使用此命令可以将dash改为bash
//跳出来的框选择no即可
sudo dpkg-reconfigure dash  
du -h //查看文件的大小

cat file > newfile //cat 将file中的内容输出的标准输出，> 将标准输出重定向到了newfile中， >>追加, >覆盖

cat file | grep "hello"  //找到file中hello行

sudo nvidia-smi -pm 1

\>log 1>&2 //1，2都定向到log文件中

