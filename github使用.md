---


---

<blockquote>
<p>详细的使用教程http://www.runoob.com/git/git-tutorial.html</p>
</blockquote>
<h1 id="安装配置">安装配置</h1>
<h2 id="linux-平台上安装">Linux 平台上安装</h2>
<p>Git 的工作需要调用 curl，zlib，openssl，expat，libiconv 等库的代码，所以需要先安装这些依赖工具。</p>
<p>在有 yum 的系统上（比如 Fedora）或者有 apt-get 的系统上（比如 Debian 体系），可以用下面的命令安装：</p>
<p>各 Linux 系统可以很简单多使用其安装包管理工具进行安装：</p>
<h3 id="debianubuntu">Debian/Ubuntu</h3>
<p>Debian/Ubuntu Git 安装命令为：</p>
<pre><code>apt-get install git
# git版本
git --version
</code></pre>
<hr>
<h2 id="windows-平台上安装">Windows 平台上安装</h2>
<p>在 Windows 平台上安装 Git 同样轻松，有个叫做 msysGit 的项目提供了安装包，可以到 GitHub 的页面上下载 exe 安装文件并运行：</p>
<p>安装包下载地址：<a href="http://msysgit.github.io/">http://msysgit.github.io/</a></p>
<p>完成安装之后，就可以使用命令行的 git 工具（已经自带了 ssh 客户端）了，另外还有一个图形界面的 Git 项目管理工具。</p>
<p>在开始菜单里找到"Git"-&gt;“Git Bash”，会弹出 Git 命令窗口，你可以在该窗口进行 Git 操作。</p>
<h2 id="配置个人信息">配置个人信息</h2>
<p>配置个人的用户名称和电子邮件地址：</p>
<pre><code>$ git config --global user.name "runoob" 
$ git config --global user.email test@runoob.com
</code></pre>
<h1 id="git-工作流程">Git 工作流程</h1>
<p>一般工作流程如下：</p>
<ul>
<li>git clone 克隆 Git 资源作为工作目录。</li>
<li>git add 在克隆的资源上添加或修改文件。</li>
<li>git merge如果其他人修改了，你可以更新资源。</li>
<li>git status 在提交前查看修改。</li>
<li>git commit 提交修改。</li>
<li>reset HEAD在修改完成后，如果发现错误，可以撤回提交并再次修改并提交。</li>
</ul>
<p>下图展示了 Git 的工作流程：</p>
<p><img src="http://www.runoob.com/wp-content/uploads/2015/02/git-process.png" alt=""></p>
<h1 id="git基本命令">git基本命令</h1>
<p>详情看http://www.runoob.com/git/git-basic-operations.html</p>
<h1 id="github使用">github使用</h1>
<h3 id="创建一个git仓库">创建一个git仓库</h3>
<pre><code>cd weifengcloud
echo "# weifengcloud" &gt;&gt; README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/cacacai/weifengcloud.git
git push -u origin master
</code></pre>
<h3 id="上传一个已经存在的git仓库">上传一个已经存在的git仓库</h3>
<pre><code>git remote add origin https://github.com/cacacai/weifengcloud
git git push -u origin master
</code></pre>
<p><strong>注意</strong>  如果需要更改尽量自己创建一个分支然后修改再提交。</p>
```
合并两个没有共同分支历史的仓库
git pull origin master --allow-unrelated-histories 
```
