[//]: # (Source: https://www.jetbrains.com/help/idea/move-refactorings.html)
[//]: # (Downloaded: 2025-12-17 19:32:50)

## Instance method example

Let's move the `getName` instance method from the `Test` class to the `Car` class.

import java.lang.reflect.InvocationTargetException; public class Test { public static void main(String[] args) throws Exception { Car c= new Car(); System.out.println(new Test().getName(c)); } String getName(Car car){ System.out.print(toString()); return car.name; } } class Car { String name = "Default Car"; Car() throws InvocationTargetException, NoSuchMethodException, InstantiationException, IllegalAccessException { } } 

import java.lang.reflect.InvocationTargetException; public class Test { public static void main(String[] args) throws Exception { Car c= new Car(); System.out.println(c.getName(new Test())); } } class Car { String name = "Default Car"; Car() throws InvocationTargetException, NoSuchMethodException, InstantiationException, IllegalAccessException { } String getName(Test anotherObject){ System.out.print(anotherObject.toString()); return this.name; } } 
