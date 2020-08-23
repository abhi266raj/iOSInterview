- A class monster is created in game. There is a rule that only 20 monster can be created in game at max anytime. How will you this. Discuss all approach. Write code for this 

- Differnce between class and static property
class. 

```
class Test {
    static var staticValue:Int? {
        get {
            return 7
        }
    }
    class var classValue:Int?{
        get {
            return 6
        }
    }
}
```

- How do you init a class from literal value/primitve value. How such thing can be done in swift

```
class Temperature {
var value:Int
}

let temperature: Temperature = 37
```

- Answer the following question with respect to following code

```
class TestView: UIView {
    
    
    init() {
        super.init(frame:.zero)
    }
    
    required init?(coder: NSCoder) {
        fatalError("init(coder:) has not been implemented")
    }
}

```
 	
 	1. When we try to create init method and ap



