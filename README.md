# Program Function:

- Transfer files between devices under the local area network. support single file and the whole folder transfer.  
  For expamle, we can transfer files between computers or between smart phones which connect in a same wifi, also  
  between smart phone and computer is ok.(we can also turn on our Data hotspot on our smart phones or computers,  
  and other devices connect to the hotspot, it can also transfer files in between). The server is responsible for  
  sending data, and the client is converse.

> Tip: We have to download Termux and gcc to compile and run the program if want to transfer files between devices  
> that contain android smart phone, it's more convenient to input to use Hacker's Keyboard, so we can download and  
> install this app in our app store

# Usage:

- compile:

  - _\$ gcc server.c -o server_
  - _\$ gcc client.c -o client_

- run:
  - server side run firstly：_\$ ./server_
  - client side run secondary：_\$ ./client hostname_

> Tip：hostname is ip address of server,we can find it by running the command line 'ifconfig' in our terminal.  
> Just like：172.26.5.77(after inet)

# Example:

> The following takes the example of server ip being 172.26.5.77:

- server side(run in one terminal window): _\$ ./server_

- client side(run in another terminal window): _\$ ./client 172.26.5.77_

- Then the server side will receive the client side connection request. After the connection, it needs to input the  
  absolute path of the file to be transmitted on the server side. After the input is completed, the client side will  
  first receive the file name sent by the server side, and then detect the file name. See if there is a file with the  
  same name under the current folder will be overwritten, if so, we can choose to exit, overwrite, or rename (Just  
  follow the prompts to finish all things is ok :)

> Tip: if you want to test the program by local computer please repalce the 'hostname' with 127.0.0.1

<br>
<br>
<br>

# 程序功能:

- 在局域网中的设备间进行文件传输，支持单个文件和和整个文件夹的传输，比如连接同一个 wifi 的电脑和电脑，手  
  机和手机之间，电脑和手机之间。(也可以电脑或手机开 wifi 热点，另一台设备连接之后也是局域网，可以相互传输  
  文件)。其中 server 端用于发送文件，client 端负责接收文件

> 注：Android 手机要运行此程序的话，需要下载 Termux，并安装 gcc 用于编译程序，然后运行即可，为了输入方便，可以再安装 Hacker's Keyboard

# 用法：

- 编译：

  - _\$ gcc server.c -o server_
  - _\$ gcc client.c -o client_

- 运行:
  - server 端先运行：_\$ ./server_
  - client 端后运行：_\$ ./client hostname_

> 注：hostname 填写 server 端的 ip 地址,可以通过 ifconfig 命令查找,inet 后面的那个点分十进制就是,形如：172.26.5.77 即为 ip 地址

# 实例

下面以 server 端 ip 为 172.26.5.77 的为例

- server 端(在其中一个终端界面上运行): _\$ ./server_

- client 端(在另一个终端界面上运行): _\$ ./client 172.26.5.77_

- 接着 server 端会接收到 client 端的连接请求,连接后需要在 server 端输入需要传  
  输的文件的绝对路径,输入完成后 client 端会首先收到 server 端发送过来的文件名,  
  然后进行文件名的检测，看当前文件夹下是否有同名文件会被覆盖，若有可以选择  
  退出，覆盖，或重命名(运行时直接跟随提示操作即可)

> 注：本机测试的话将 hostname 改成 127.0.0.1 即可
