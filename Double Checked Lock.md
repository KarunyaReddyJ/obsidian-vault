This is a concurrency design pattern specifically used in [[Singleton Pattern]] for making it thread safe as well ensuring we don't make thread wait in queue while a thread executing an if statement which will evaluate to false anyhow.

```java
if(instance==null){//fast non blocking check will evaluate to false once an instance is created 
  synchronized(Singleton.class){
  //safety check to ensure the concurrent instance checks won't happen which will cause the multiple object creation
      if(instance==null){
          instance = new Singleton()
      }
  }
}
``` 

The synchronized also solves the [[Visibility Problem]].