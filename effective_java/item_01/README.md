## Static factory methods instead of Constructors
Traditionally we use a public constructor to allow the client to obtain an instance of ta object. Alternatively, we can provide a public static factory method.

```
// default constructor
public Car(String make, String model, String color) {
    return new Car(make, model, color);
}

// static factory method
public static Boolean buildTesla(String model, String color) {
    return new Car("Tesla", model, color);
}
```

Having a static factory method has the following benefits:

1. a static factory has names, which can make the usage much easier to comprehend.

2. unlike constructors, static factory methods does not require a new object each time they're invoked. Because they are static

3. static factory methods allows you to do instance-control of target classes. This is especially useful for singleton classes or noninstantiable classes. It can allow guarantee that no 2 instances are equal. 

4. in a static factory, the class of the returned object need not exist when the class containing the method is written.