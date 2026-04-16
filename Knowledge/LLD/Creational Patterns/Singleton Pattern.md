Singleton Pattern is one of the [[Creational Design Pattern]] which is used to create only one instance of a class and use it globally.

We restrict the other classes from calling the Constructor the class directly by making it private and providing those classes an interface(not interface of java but in general ) which controls the creation of object.

For making the Singleton class Thread-Safe we use:
- [[Double Checked Lock]]
- refrain [[CPU Instruction Reordering]] by explicitly using volatile keyword in Java
