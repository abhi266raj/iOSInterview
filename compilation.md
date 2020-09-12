* There are three ways compilation are done in ios app. Arrange them with respect to compilation time. Explain the timing difference
	* We have build the app and then we change a line of code on program and build the app again. We care about second build timing
	* We clean build the app
	* We build the app from archive that is used for releasing to the app store.
	
* What is .dSYM. What is the full form. Why it is used?

* You are declaring a class and a protocol. What is better decision to implent the protocol and class in same file or create two file and implement in different file?  Explain with respect to compialtion and how does compilation affect them.

```
File Title.swift
protocol Title {
    var title:String?{get}
}


File Note.swift
struct Note: Title {
    var title:String?
    
}. 

```

* Does adding space extra line cause a file to recompile.

* There are two files. Answer these question with respect to files

```
File ViewController.swift
class ViewController: UIViewController {
    var note:Note = Note()
 }
 
File Note.swift
class Note {
var title
}
```

* Assume the following, compiling class ViewController takes 1 minute and compiling class Note take 1 second. We want that class ViewController should not be compiling unneccsary and no-one changes class ViewController but class note is changes often. You have compiled the code once and now working on incremental build
	*  Suppose you changed aligment in file Note. Which file will be compiled in incremetnal 
	* Suppose you added extra variable in class note which wont be used by classViewController. Which file will be compiled. Any better way to solve compilation time.


