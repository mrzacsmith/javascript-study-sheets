## Understanding JavaScript Classes

In JavaScript, classes are blueprints for creating objects. They provide a way to define object properties and methods that can be shared across multiple instances. Although classes themselves are not objects, they serve as templates to generate objects with similar properties and behaviors. Let's look at how we can create a class with generic placeholders in a food-related context:

```javascript
class FoodItem { // syntax: (1) class keyword (2) class name, typically capitalized
  name = 'Generic Food' // adding a default property
  calories = 0 // adding another default property
  updateCalories(cal) { // adding a method to update calories
    this.calories += cal
    return `Calories updated: ${this.calories}`
  }
}
```

Now that we've defined the `FoodItem` class, we can create instances of this class to represent different food items:

```javascript
const apple = new FoodItem() // this creates a new object (or instance) based on the FoodItem class
```

Let's test our new object:

```javascript
apple.updateCalories(95)
console.log(apple.calories) // prints 95
console.log(apple.name) // prints "Generic Food"
```

As you can see, our created object `apple` has inherited the `updateCalories` method and both the `name` and `calories` properties from the `FoodItem` class. We can create as many instances of `FoodItem` as we want, and they will all have the same properties and methods, making classes a powerful tool for object creation.

### How to Build It: Practice Walkthrough

Now, let's create a class for a specific type of food item, such as a `Fruit`, with a few basic properties and one method:

```javascript
class Fruit {
  name = 'unknown fruit' // each property has a default value set
  sweetness = 5
  isRipe = false
  toggleRipeness() { // method to change ripeness state
    this.isRipe = !this.isRipe
  }
}
```

Let's use this class to create a new fruit object and see how it inherits the properties and methods:

```javascript
const banana = new Fruit() // creating a new instance of the Fruit class
console.log(banana.name) // prints "unknown fruit"
console.log(banana.sweetness) // prints 5
console.log(banana.isRipe) // prints false

banana.toggleRipeness() // calling the method to change ripeness state
console.log(banana.isRipe) // now prints true
```

Our new `banana` object has inherited the properties and method of the `Fruit` class as specified in the class template. We can now update the `banana` object's properties:

```javascript
banana.name = "Banana" // updates the name property value from "unknown fruit" to "Banana"
banana.sweetness = 7 // updates the sweetness property value from 5 to 7

console.log(banana.name) // prints "Banana"
console.log(banana.sweetness) // prints 7
```

Using classes to create templates for objects is useful when you need multiple object instances with shared properties and methods. However, if you need to create objects with customized initial values, you can use the `constructor` method, which we'll discuss next.

---

### Checklist for Creating and Using a JavaScript Class

1. **Define the Class**:
   - Use the `class` keyword followed by the class name.
   - Example: `class FoodItem {}`

2. **Add Properties**:
   - Define default properties within the class.
   - Example: `name = 'Generic Food'`

3. **Add Methods**:
   - Add methods to the class for behaviors you want instances to have.
   - Example: `updateCalories(cal) { this.calories += cal }`

4. **Create Instances**:
   - Use the `new` keyword to create instances of the class.
   - Example: `const apple = new FoodItem()`

5. **Test and Update Instances**:
   - Test the properties and methods, and update properties as needed.
   - Example: `apple.updateCalories(95)`

