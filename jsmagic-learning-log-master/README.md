
# [ZengBiYi](https://github.com/ZengBiYi)的学习日志

##开始Github的探索之配置学习日志和上传本地代码-2016.09.27
  由于本人学习的习惯是先理解后行动的，加上刚接触github不久，对配置学习日志的步骤不理解，现在完成后来回顾一下：
  首先贴出配置的步骤：
  1. fork 这个 repo

  2. 用你的 github 账户登录 gitbook 网站


  1. fork 这个 repo

  2. 用你的 github 账户登录 gitbook 网站

  3. 创建一个新的 gitbook，创建时选择从 github 创建，并选择你在步骤 1 中 fork 的目录

  4. 把 README.md 中的 [XXX](https://github.com/xxx) 换成你自己的 github id，并且删掉"配置你自己的学习日志" 这个部分

  5. 这样你就完成了学习日志的创建。你可以通过 gitbook 自己的在线编辑器来写学习日志，或者通过更新 github repo 
  的方式来上传日志。

  6. 你可以通过 https://{your-github-id}.gitbooks.io/{gitbook-name} 来访问你的学习日志

  对第1点，fork是复制的意思，看完第2,3点就知道是将复制的这个仓库放在自己github中去，其实很简单，但是不理解的话就是寸步难行。
  
  接下来通过Google学习了如何将本地文件上传到github。（前提是已经创建好了Github账户和安装好了Git Shell程序）
  1.打开Git Shell，输入以下命令生成密钥来验证身份：ssh-keygen -C 'your@email.address' -t rsa
  2.此时会在window的用户下的.ssh文件夹下生成pub文件，把文件夹下的id_rsa.pub文件内容全部复制。然后打开github账户设置，找到setting 里面的ssh keys，右上角点击add ssh key，然后在title随便输入，key栏粘贴刚才的密钥。
  3.在Git Shell下输入命令：ssh -T git@github.com 测试刚才的公钥是否认证正确。
  4.clone刚才新建的repository 到本地，输入命令：git clone https://github.com/Flowerowl/stumansys.git
  5.新建Text文件夹作为仓库根目录（文件夹名字随意命名）
  6.将需要上传的代码文件加入到Text根目录
  7.在根目录下建立仓库，输入下面命令：先进入到Text根目录下，再输入git init（初始化一个仓库）
  8.将所有文件添加到仓库，输入下面命令：git add .
  9.提交，输入下面命令：git commit -m “CommitInfo”
  10.添加源到GitHub：git remote add origin git@github.com:YourName/YourRepositroy.git
  11.上传源到GitHub：git push -u origin master
  至此，就可以在自己的Github中看到新增的文件了。




