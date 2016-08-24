Hiding implementation is not just a matter of putting a layer of functions between the variables. Hiding implementation is about abstractions! A class does not simply push its variables out through getters and setters. Rather it exposes abstract interfaces that allow its users to manipulate the essence of the data, without having to know its implementations.

Listing 6-3 uses concrete terms to communicate the fuel level of a vehicle.
Listsing 6-4 use abstraction of percentage.

In the concrete case you can be pretty sure that these are just accessors of variables.
In the abstract case you have no clue at all about the form of the data.

In both cases, the Abstract option is preferable. We do not want to expose the details of our data. Rather we want to express our data in abstract terms. Serious thought needs to be put into the best way to represent the data that an object contains. The worst option is to blithely add getters and setters.


* Listing 6-3
Concrete Vehicle
```
public interface Vehicle {
    double getFuelTankCapacityInGallons();
    double getGallonsOfGasoline();
}
```
* Listing 6-4
Abstract Vehicle
```
public interface Vehicle {
    double getPercentFuelRemaining();
}
```
