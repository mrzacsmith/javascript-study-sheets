## Using the Constructor Method in JavaScript Classes

In addition to defining properties directly within a class, JavaScript provides a special method called the `constructor` to initialize object properties with custom values when creating instances. This allows for more flexibility and customization when generating objects. Let's explore how to use the constructor method with our previous food-related example.

### Example Without Constructor

```javascript
class FoodItem {
  name = 'Generic Food'
  calories = 0
  updateCalories(cal) {
    this.calories += cal
    return `Calories updated: ${this.calories}`
  }
}

const apple = new FoodItem()
console.log(apple.name) // prints "Generic Food"
console.log(apple.calories) // prints 0
```

### Example With Constructor

By using the constructor method, we can set the initial values for `name` and `calories` when creating a new instance:

```javascript
class FoodItem {
  constructor(name, calories) { // defining the constructor method
    this.name = name
    this.calories = calories
  }

  updateCalories(cal) {
    this.calories += cal
    return `Calories updated: ${this.calories}`
  }
}

// Creating a new instance with custom initial values
const apple = new FoodItem('Apple', 95)
console.log(apple.name) // prints "Apple"
console.log(apple.calories) // prints 95
```

As you can see, the `constructor` method allows us to set initial values for the `name` and `calories` properties when we create a new `FoodItem` object.

### How to Build It: Practice Walkthrough

Now, let's create a `Fruit` class with a constructor method to initialize its properties:

```javascript
class Fruit {
  constructor(name, sweetness, isRipe) {
    this.name = name
    this.sweetness = sweetness
    this.isRipe = isRipe
  }

  toggleRipeness() {
    this.isRipe = !this.isRipe
  }
}

// Creating a new instance with custom initial values
const banana = new Fruit('Banana', 7, false)
console.log(banana.name) // prints "Banana"
console.log(banana.sweetness) // prints 7
console.log(banana.isRipe) // prints false

banana.toggleRipeness() // calling the method to change ripeness state
console.log(banana.isRipe) // now prints true
```

With the `constructor` method, you can create instances of `Fruit` with customized initial values, making your class more versatile and dynamic.

---

### Checklist for Creating and Using a JavaScript Class with Constructor

1. **Define the Class with Constructor**:
   - Use the `class` keyword and define the constructor method.
   - Example: `class FoodItem { constructor(name, calories) { this.name = name; this.calories = calories; } }`

2. **Initialize Properties in Constructor**:
   - Set the initial values for properties inside the constructor.
   - Example: `this.name = name;`

3. **Add Methods**:
   - Define methods within the class as usual.
   - Example: `updateCalories(cal) { this.calories += cal; }`

4. **Create Instances with Custom Values**:
   - Use the `new` keyword to create instances, passing values to the constructor.
   - Example: `const apple = new FoodItem('Apple', 95);`

5. **Test and Use Instances**:
   - Test the properties and methods, and utilize the instances as needed.
   - Example: `console.log(apple.name); // prints "Apple"`

---

Using the constructor method provides a powerful way to create more flexible and customizable object instances in JavaScript. Practice using constructors to become proficient in creating dynamic classes.

