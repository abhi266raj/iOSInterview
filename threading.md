1. There is a class square. It has two stored variable. Area and side and a function detail. 

```
class Square {
 private (set) var area = 0
 var length = 0 {
 	didSet{
 		area = length * length
 		}
	}

func info() {
	print(" length = \(length), area = \(area)")
}
}
```

Now we are setting length to 5 and 6 in different parts of program only in different threads. But some where the logs are coming length = 5 and area = 36. Which means there are some error in code. Can you debug what might be the case. How can you fix that. 

2. Create async function of GCD
3. Create GCD
4. Create Dispatch group
