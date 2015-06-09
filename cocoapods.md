cocoapods

 CocoaPods, the Objective-C library package manager.

1.RubyGems

RubyGems（简称 gems）是一个用于对 Ruby组件进行打包的 Ruby 打包系统。 它提供一个分发 Ruby 程序和库的标准格式，还提供一个管理程序包安装的工具。
RubyGems的功能类似于Linux下的apt-get。使用它可以方便第从远程服务器下载并安装Rails。
打开命令行窗口(cmd)，输入执行命令 gem install rails --remote 或　gem install rails--include-dependencies。


ruby+gem常用命令
 
ruby -e ''require"watir"; puts Watir::IE::VERSION''　#查看watir版本 
gem -v #gem版本 
gem update #更新所有包 
gem update --system #更新RubyGems软件 
gem install rake #安装rake,从本地或远程服务器 
gem install rake --remote #安装rake,从远程服务器 
gem install watir -v(或者--version) 1.6.2#指定安装版本的 
gem uninstall rake #卸载rake包 
gem list d #列出本地以d打头的包 
gem query -n ''[0-9]'' --local #查找本地含有数字的包 
gem search log --both #从本地和远程服务器上查找含有log字符串的包 
gem search log --remoter #只从远程服务器上查找含有log字符串的包 
gem search -r log #只从远程服务器上查找含有log字符串的包 
gem help #提醒式的帮助 
gem help install #列出install命令 帮助 
gem help examples #列出gem命令使用一些例子 
gem build rake.gemspec #把rake.gemspec编译成rake.gem 
gem check -v pkg/rake-0.4.0.gem #检测rake是否有效 
gem cleanup #清除所有包旧版本，保留最新版本 
gem contents rake #显示rake包中所包含的文件 
gem dependency rails -v 0.10.1 #列出与rails相互依赖的包 
gem environment #查看gem的环境

2. 安装cocoapods
sudo gem update --system
sudo gem  install cocoapods 
pod setup 

下载不动时，替换ruby 源为下面：
gem sources --remove https://rubygems.org/
gem sources -a http://ruby.taobao.org/
gem sources -l 

节省更新维护第三方开源库的时间；


3. 查找某个库：

pod search json

执行 配置一个podfile文件；放在工程根目录下执行 
pod install

pod install --no-repo-update //不更新配置中版本
---------------
配置文件内容
---------------
platform:ios
pod 'JSONKit' ,'~> 1.4'
--------------

所有的维护工程都在配置文件，比如删除某个库；

原理：

所有的依赖库都放倒pods工程中，让主项目依赖pods项目；





