---
layout: post
title: Homework
permalink: /homework/
---

## This is all of the homework from the lessons being taught 

### Homework for Conditionals

```javascript

// Define a character class
class Character {
    constructor(name, health, attackPower) {
        this.name = name; // Character's name
        this.health = health; // Character's health points
        this.attackPower = attackPower; // Character's base attack power
    }

    // Method to attack an enemy
    attack(enemy) {
        if (this.health > 0) { // Check if the character is alive
            let randomAttackPower = Math.floor(Math.random() * this.attackPower) + 1; // Generate random attack power
            console.log(`${this.name} attacks ${enemy.name} for ${randomAttackPower} damage.`);
            enemy.health -= randomAttackPower; // Reduce enemy's health by random attack power
            if (enemy.health <= 0) { // Check if the enemy is defeated
                console.log(`${enemy.name} has been defeated!`);
            } else {
                console.log(`${enemy.name} has ${enemy.health} health remaining.`);
            }
        } else {
            console.log(`${this.name} cannot attack because they are defeated.`);
        }
    }
}

// Create characters
let hero = new Character('Hero', 100, 10); // Create a hero character
let monster = new Character('Monster', 50, 5); // Create a monster character

// Simulate a battle
hero.attack(monster); // Hero attacks monster
monster.attack(hero); // Monster attacks hero
hero.attack(monster); // Hero attacks monster again
monster.attack(hero); // Monster attacks hero again
hero.attack(monster); // Hero attacks monster again
```

### Homework for Mathematic Expressions 

```javascript

%%js

//Problem 1

let a = 60;
let b = 13;

    console.log("Sum:", a + b);          
    console.log("Difference:", a - b);   
    console.log("Product:", a * b);      
    console.log("Quotient:", a / b);

//        Output: Sum: 73
//        Difference: 47
//        Product: 780
//        Quotient: 4.615384615384615...

%%js 

//Problem 2

let num1 = 5;
let num2 = 200;

    console.log("Remainder:", num1 % num2);  // Output: 5


%%js

// Problem 3

let count = 10;
console.log("Initial Count:", count);  // Output: 10

// Increment using ++
count++;
console.log("After Increment using ++:", count);  // Output: 11

// Decrement using --
count--;
console.log("After Decrement using --:", count);  // Output: 10

// Increment using +=
count += 5;
console.log("After Increment using += 5:", count);  // Output: 15

// Decrement using -=
count -= 3;
console.log("After Decrement using -= 3:", count);  // Output: 12
```

### Homework for Nested Conditionals

```javascript
%%js 

// Generate a random grade between 0 and 12

let grade = Math.round(Math.random() * 12);
console.log(`You are in ${grade} grade.`);

// Determine the school level and if the student is in their final year
if (grade === 0) {
    console.log("You are in Kindergarten.");
} else if (grade >= 1 && grade <= 5) {
    console.log("You are in Elementary School.");
    if (grade === 5) {
        console.log("You will graduate this year from Elementary School.");
    }
} else if (grade >= 6 && grade <= 8) {
    console.log("You are in Middle School.");
    if (grade === 8) {
        console.log("You will graduate this year from Middle School.");
    }
} else if (grade >= 9 && grade <= 12) {
    console.log("You are in High School.");
    if (grade === 12) {
        console.log("You will graduate this year from High School.");
    }
}
```