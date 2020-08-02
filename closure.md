### Closure Question Bank

1. Capturing vs non capturing
 		
	```
		var value = 5
		let closure = { [value] in
		    print(value)
		}
		value = 6
		closure()
	```
		
	```
		var value = 5
		let closure = {
		    print(value)
		}
		value = 6
		closure()
	
	```
2. Struct vs class capturing vs non capturing
	
	```
	struct Test {
	    var value = 0
	}
	
	var object = Test()
	let closure = { [object] in
	    print(object.value)
	}
	object.value = 6
	closure()
	```
	
	```
	class Test {
	    var value = 0
	}
	
	var object = Test()
	let closure = { [object] in
	    print(object.value)
	}
	object.value = 6
	closure()
	```
	
	```
	struct Test {
	    var value = 0
	}
	
	var object = Test()
	let closure = { 
	    print(object.value)
	}
	object.value = 6
	closure()
	```
	
	```
	class Test {
	    var value = 0
	}
	
	var object = Test()
	let closure = { 
	    print(object.value)
	}
	object.value = 6
	closure()
	```
	

2.  


