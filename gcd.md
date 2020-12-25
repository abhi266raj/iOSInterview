### GCD Question Bank

Answer all these in 
	- Will this code compile  
	- Will the code have deadlock  
	- Will this code have race condtion
	- Will the answer change on change qos parameters  (if applicable)

1. Race condition  

	```
	DispatchQueue.main.async {
		print ("A")
		DispatchQueue.global(qos: .userInteractive).async {
		    print ("B")
		}
		print("C")
		print("D")
	}
	```

2.

```
DispatchQueue.main.async {
	print ("A")
	DispatchQueue.main.sync {
		print ("B")
	}
	print("C")
}
```
		
```
DispatchQueue.main.async {
	print ("A")
	DispatchQueue.main.async {
		print ("B")
	}
	print("C")
}
```

3. Write a thread safe linked list read and delete function. Condition: Multiple read can go on linked list but but multiple write cannot. When read in going on write cannot go on and when write is going on read cannot.


4. Write the output of following code

```
func printData() {
    print("A");
    DispatchQueue.main.async { print("C");
        DispatchQueue.main.async { print("D") };
    DispatchQueue.global().sync {
        print("E")
        DispatchQueue.main.sync {
            print("G")
            
        }
        print("H")
        
    }
        print("F")
    
 }
    print("B")
 }
```

5. 