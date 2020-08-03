### Memory managment Question Bank

1. Write the output of 
	
	```
	protocol InputHandlingProtocol {
	    func didRecivedInput(_ string:String)
	}
	
	class InputPrinter: InputHandlingProtocol {
	    func didRecivedInput(_ string: String) {
	        print(string)
	    }
	}
	
	class Reciever {
	    weak var delegate:InputPrinter?
	    
	    func revieveInput(_ string:String){
	        delegate?.didRecivedInput(string)
	    }
	}
	
	var reciver = Reciever()
	reciver.delegate = InputPrinter()
	reciver.revieveInput("Hello")
	
	
	var printer:InputPrinter? = InputPrinter()
	reciver.delegate = printer
	reciver.revieveInput("Printing")
	printer = nil
	reciver.revieveInput("Dellocated")
	```
2. Expain the result of the following. What happens when unowned is changed to weak. 
 
	```
	class Child {
	    func display() {
	       print("Hello") 
	    }
	}

	class Parent {
	    unowned var child:Child?
	}
	
	
	var parent = Parent()
	var m:Child = Child()
	parent.child = m
	parent.child?.display()
	m = nil
	parent.child?.display()
	```