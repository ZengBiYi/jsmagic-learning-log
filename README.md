
# [ZengBiYi](https://github.com/ZengBiYi)的学习日志

##开始Github的探索之配置学习日志和上传本地代码--2016.09.27
  由于本人学习的习惯是先理解后行动的，加上刚接触github不久，对配置学习日志的步骤不理解，现在完成后来回顾一下：
  首先贴出配置的步骤：


  1.fork 这个 repo

  2.用你的 github 账户登录 gitbook 网站

  3.创建一个新的 gitbook，创建时选择从 github 创建，并选择你在步骤 1 中 fork 的目录

  4.把 README.md 中的 [XXX](https://github.com/xxx) 换成你自己的 github id，并且删掉"配置你自己的学习日志" 这个部分

  5.这样你就完成了学习日志的创建。你可以通过 gitbook 自己的在线编辑器来写学习日志，或者通过更新 github repo 
  的方式来上传日志。

  6.你可以通过 https://{your-github-id}.gitbooks.io/{gitbook-name} 来访问你的学习日志
  
  对第1点，fork是复制的意思，看完第2,3点就知道是将复制的这个仓库放在自己github中去，其实很简单，但是不理解的话就是寸步难行。
  
  接下来通过Google学习了如何将本地文件上传到github。（前提是已经创建好了Github账户和安装好了Git Shell程序）
  1. 打开Git Shell，输入以下命令生成密钥来验证身份：ssh-keygen -C 'your@email.address' -t rsa
  2. 此时会在window的用户下的.ssh文件夹下生成pub文件，把文件夹下的id_rsa.pub文件内容全部复制。然后打开github账户设置，找到setting 里面的ssh keys，右上角点击add ssh key，然后在title随便输入，key栏粘贴刚才的密钥。
  3. 在Git Shell下输入命令：ssh -T git@github.com 测试刚才的公钥是否认证正确。
  4. clone刚才新建的repository 到本地，输入命令：git clone https://github.com/Flowerowl/stumansys.git
  5. 新建Text文件夹作为仓库根目录（文件夹名字随意命名）
  6. 将需要上传的代码文件加入到Text根目录
  7. 在根目录下建立仓库，输入下面命令：先进入到根目录下，再输入git init（初始化一个仓库）
  8. 将所有文件添加到仓库，输入下面命令：git add .
  9. 提交，输入下面命令：git commit -m “CommitInfo”
  10. 添加源到GitHub：git remote add origin git@github.com:YourName/YourRepositroy.git
  11. 上传源到GitHub：git push -u origin master
  至此，就可以在自己的Github中看到新增的文件了。

##Gitbook的成功创建以及如何在Github上更新Gitbook--2016.09.28
  继昨天创建完Gitbook后，出现了些许小问题，一打开自己的Gitbook地址无法显示出内容，而是显示Your content is almost ready.
  折腾了许久，原来只需要删除重建即可

  在Github上更新Gitbook
  1. 首先在自己的GIthub账户中找到与Gitbook相关联的那个repo,download zip，然后解压
  接下来的步骤就是上传本地文件到github，但是和昨天写的步骤有一点点区别，因为昨天那个是新建了一个repo，而今天是直接更新已有的文件。所以重写步骤如下：
  2. 将要更新的文件所在的文件夹即刚刚解压的文件夹作为根目录，在根目录下建立仓库：git init
  3. 将所有文件添加到仓库，输入下面命令：git add .
  4. 提交，输入下面命令：git commit -m “CommitInfo”
  5. 添加源到GitHub：git remote add origin git@github.com:YourName/YourRepositroy.git(注意，origin 后面的这一串要修改，修改的内容怎么找呢：打开Github与Gitbook相关联的文件夹，点clone or download按钮，Clone with SSH,复制框中的那一串)
  6. 上传源到GitHub：git push -u origin master
  
  我在上传过程中遇到一个问题，就是没有修改第5步的那一串，导致上传时找不到repo。
  查看源的命令：git remote -v, 发现并不是我要上传的那个仓库，
  删除当前这个origin：git remote rm origin
  添加origin：和上面第5步一样。



