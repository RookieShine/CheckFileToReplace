1`客户端实现版本升级时，避免需要从服务器下载所有文件代码。  
2`在本地客户端上已经存在一个所有文件的check文件,将每一个文件存在DIC中,key为文件名,value由文件内容生成的MD5文件.  
3`升级时只需要将最新的check文件与本地做差分,key相同而value不同的文件就是我们需要从服务器下载更新的文件.包括下载新增的文件,替换原本存在而内容改变的文件,删除多余的文件,最后删除掉原来的old文件即可.  
4`下载时最新的check也将被保存,用于下次更新时做差分  
5`接口仅用于下载文件,此处不做描述  
