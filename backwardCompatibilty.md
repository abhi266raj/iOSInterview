* Suppose in v1 of app the code is written as

```
enum UploadStatus:Int{
    case notStarted
    case uploading
    case uploaded
    case failed
}

@objc class UploadModel:NSObject, NSCoding {
    func encode(with coder: NSCoder) {
        coder.encode(status.rawValue, forKey: "status")
        coder.encode(path, forKey: "path")
    }
    
    required init?(coder: NSCoder) {
        self.path  = coder.decodeObject(forKey: "path") as? String
        let value = coder.decodeInteger(forKey: "status")
        if let status = UploadStatus.init(rawValue: value) {
            self.status = status
        }else{
            return nil
        }
    }
    
    var status:UploadStatus
    var path:String?
    
}

```


In v2 you need to add the status of deletion. So the enum is changed to

```
enum UploadStatus:Int{
    case notStarted
    case deleted
    case uploading
    case uploaded
    case failed
}
```

The class is using following Codable protocol. Which means you can save the state of model between launches. So if you have to review the code what are the mistake in these code.  Assume the code for saving, loading, uploading is wokring fine and is written by someone else.