# ALDownloadManager
A progressive download manager for Alamofire
 
 顺序下载 

 ![image](https://github.com/Yvent/ALDownloadManager/blob/master/Resource/2017-12-11%2011_49_36.gif)  
 
同时下载

 ![image](https://github.com/Yvent/ALDownloadManager/blob/master/Resource/2017-12-11%2011_50_44.gif)



Requirements
 ````
iOS 9.0+ 
Xcode 8.0+
Swift 3.0+
 ````
 
 单文件下载
 ````
    ALDownloadManager.shared.download(url:  self.testUrl)?.progressChangeBlock = { (progress) in
                    let completed: Float = Float(progress.completedUnitCount)
                    let total: Float = Float(progress.totalUnitCount)
                    self.progressView.progress = (completed/total)
                    self.progressLab.text = "\(completed/total)"
                }
````
 多文件同时下载
 ````
 ALDownloadManager.shared.changeDownloadState()
````
 多文件顺序下载
 ````
  ALDownloadManager.shared.changeWaitState(completeClose: nil)
````
