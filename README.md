#jdlingyuImageCollector  
程序使用方法很简单，隔一段时间打开JdlingyuImageCollector.exe就可以了，它会自动检查jdlingyu上的更新，然后下载更新的内容，顺便收集百度盘链接。如果没有更新的话也会显示“下载完成”。  
嫌日志烦的话可以删掉，并且把options.ini里的logToFile=True改为logToFile=False，但是不要删除catalog.txt和downloaded.txt。  
应该是必须要有.NET Framework组件才能正常运行的（我没有试过没有会怎么样），不过大部分电脑应该都有吧。  
文件夹命名规范：序号_标题_分类_标签。  

可能存在的bug：  
最常见的bug就是，加载页面或者下载图片的时候会卡在那里，出现这种问题多半是因为网络不稳定，重新打开程序即可。  
还可能因为一些奇怪的原因，导致无法正常下载，如果出现这种情况，可以手动把出错的这条url中的数字添加到downloaded.txt里即可跳过此页面。
如果遇到其他无法解决的问题……根据错误信息自己探索一下吧23333 

各个文件介绍：  
* baidupan.txt：存放百度盘链接。可删除。  
* catalog.txt：目录列表，运行程序的话会自动更新。删除的话会导致程序重新检查全部目录列表。  
* catalogLog.txt：更新目录时的日志。可删除。  
* downloaded.txt：已下载的页面列表，当下载完一个页面上所有图片时就会在这里记录下它的url中的数字，以后不再下载。当然你要是想重新下载某一个或者某些页面的图片的话可以在这个文件里删除相应url。如果删除这个文件的话会导致所有文件重新下载。 
* errorlist.txt：下载出错的图片的地址会保存在这里，有些图片，重新打开它的链接、或者多刷新几次就能加载出来，有些则是不可能再找回来了。可删除。  
* log.txt：程序主要日志。可删除。  
* options.ini：存放程序设置的地方，详细的设置说明在\jdlingyuImageCollector\Resources\options.ini里

以上文件都会保存在程序根目录。
