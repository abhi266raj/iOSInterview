* Design a cache to download video files. You will be given a videoUrl to download video. If video has not been downloaded you will download the video, save it in cache and give it to user. If video has been downloaded earlier you will return video from cache. The cache will delete the video older than let say 10 days. 
	* Create a protocol describing the cache
	* Implement the protocol
	* What are the requirement you think can change with  the implemnetaion with time. How will you handle them
	* What are the edges cases excpeted.
	* How this caching will be different from normal json cache or image cache.

* You are given five network task. Task 1 can work parallel with task 2. Task 3 will start only when both task 1 and 2 completes. Task 4 will start after task 3 finishes. Task 4 will return a flag. If flag shows false you will update a view from data of 4 else you will call 5 and update view with data of 5. Every task can fail and you should try 3 times for each task before marking the task as failed. In case of failure update view as failed.  
	* Try to complete using GCD
	* Try to complete using NSOperation
	* Make it generic so that any task can thrown and rule can be made easily.
	
* 