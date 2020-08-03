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
