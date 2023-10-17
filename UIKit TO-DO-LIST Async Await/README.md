
# TO-DO UIKit 





## API Reference

#### Get all items

```http
  GET 
  https://gist.githubusercontent.com/rigovides/12708f4aed26f847a0fe34f0fef1dbd7/raw/bb5a9a21f599acb2a46d01f45709d0aeb669f965/items.json
```


## Optimizations

the most important here is how we did conversion from callback function to async/await function 

```
func fetchData<T: Codable>(_ completion: @escaping(Result<T, Error>) -> Void)
```

- withCheckedThrowingContinuation (Automatic Xcode Async wrapper)
```
func fetchToDoTasks() async throws -> [ToDoTask] 
```

- withCheckedThrowingContinuation (Manually using Generics)
```
func fetchData<T: Codable>() async throws -> T
```

- Manually
```
func fetchToDoTasksGeneric<T: Codable>() async throws -> T 
```






