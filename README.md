# Lombok Task - Car Model

Implementation of the Car model using Project Lombok annotations to eliminate boilerplate code.

## Code

`CarWithLombok.java` contains the model class and the demo class.

```java
import lombok.AllArgsConstructor;
import lombok.EqualsAndHashCode;
import lombok.Getter;
import lombok.Setter;
import lombok.ToString;

@Getter @Setter @AllArgsConstructor
@ToString(exclude = "quantity")
@EqualsAndHashCode(of = "brand")
public class CarWithLombok {
    private String model;
    private String brand;
    private int year;
    private int price;
    private String color;
    private int quantity;
}
```

## Console Output

```text
CarWithLombok(model=GLE, brand=Mercedes, year=2020, price=350000, color=white)
CarWithLombok(model=GLC, brand=Mercedes, year=2023, price=200000, color=silver)
white
Are these objects equal? true
The HashCode of this object is: -440739023
The HashCode of this object is: -440739023
```
