# vnote-git
使用 私有仓库 + VNote 实现笔记备份
将VNote 根目录  /root/文档/vnote_notebooks 初始化私有仓库：

#~/文档/vnote_notebooks# git init	                        ###初始化。  

#~/文档/vnote_notebooks# git add .	                    ###（注意点！）把该目录下的所有文件加入到本地暂存区中。执行成功后不会有任何提示。  

#~/文档/vnote_notebooks#	git status  

#~/文档/vnote_notebooks#	git commit -m "zoro"	  

#~/文档/vnote_notebooks#	git remote add origin https://github.com/your/Repositories  

#~/文档/vnote_notebooks#	git push -u origin master  


此时初始化后的仓库已经push到你的私有仓，接下来执行下面2行，将此私有仓设置为免密push pull 方便脚本执行。  

在仓库下执行一下命令，实现免密push，pull。  


#~/文档/vnote_notebooks#	git config --global credential.helper store  

#~/文档/vnote_notebooks#	git pull /git push’        ###输入一次用户名和密码，设置完成。  

执行脚本即可同步本地VNote根目录至你的私有仓库。可配合计划任务实现定时自动同步。
