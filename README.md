# 20.1.6-Focus-on-Parameters

In JavaScript, function parameters act as placeholders for values that will be passed to the function when called. They allow functions to accept input and perform actions based on that input. 
```
function greet(name) {
  console.log("Hello, " + name + "!");
}
```
Functions in JavaScript can have multiple parameters separated by commas: 
```
function add(a, b) {
  return a + b;
}

console.log(add(5, 3)); // Output: 8
```




```
//Ex3_Parameters.js

function setup() {
    createCanvas(800, 600);
    background(200,200,80);

    textSize(20);
    fill(0);
    noStroke();

    text("Press r to roll the dice", 50, 100);
    text("Press p to pipeline cost", 50, 140);

}//end setup

function draw() {
}//end draw



function keyPressed() {
    if( key==='r'){
        // roll2Dice();
        rollDice(8,20);
    }

    if (key ==='p'){
        pipeline();
    }
}//end keyPressed

function pipeline(){
    let diameter = 1 * window.prompt("What is the diameter of the pipeline in meters?");
    let length = 1 * window.prompt("What is the length in kilometers?");
    
    length *= 1000; //convert km to meters

    materialsCost(diameter, length);
    capacity(diameter, length);
}//end pipeline

function capacity(  d, len){
    let volume = 3.14 * (d/2) * (d/2) * len;
    print("Total capacity: " + volume + " cubic meters.");
}//end capacity

function materialsCost( d, len  ){
    let squareMeters  = 3.14 * d * len;
    print("Sheet metal costs $50 per square meter");
    print("Total metal needed: " + squareMeters);
    print ("Total Cost: $" + (squareMeters*50)  );
}//end materialsCost



function roll2Dice(){




}//end roll2Dice

function rollDice( numDice, numSides ){



}//end rollDice

```
