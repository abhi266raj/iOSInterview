*  Improve the code. 

```
class Manager {
    var isEditing = false
    enum EditingError:Error {
        case alreadyEditing
        case notFound
    }
    func deleteFile(path:String) throws{
        guard isEditing == true else{
            throw EditingError.alreadyEditing
        }
        isEditing = true
       
        guard FileManager.default.fileExists(atPath: path) else {
             isEditing = true
            throw EditingError.notFound
        }
        
        do  {
             try FileManager.default.removeItem(atPath: path)
        }catch let error {
            isEditing = false
            throw error
        }
       
        isEditing = false
    }
}
```

* 

