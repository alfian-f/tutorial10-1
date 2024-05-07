# Reflections

### [1.2]
![1.2 image](assets/1.2.png)
The reason "Alfian's Computer: hey hey!" is printed first is that it is outside the asynchronous task and executes immediately, while the asynchronous task runs concurrently in the background.

### [1.3] Multiple Spawner
![multiple spawner output](<assets/1.3-multiple spawner.png>)
When there are many spawners, the results from their tasks might not come in order because they run at the same time and might mix together.

### [1.3] Removed drop(spawner)
![without drop output](<assets/1.3-removed drop.png>)
If we removed `drop(spawner)` from the code, the executor will never know when to stop executing tasks. It will continue to wait for new tasks to be spawned, even after the main thread has finished executing.