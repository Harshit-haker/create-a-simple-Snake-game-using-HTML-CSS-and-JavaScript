# create-a-simple-Snake-game-using-HTML-CSS-and-JavaScript
An example of how you can create a simple Snake game using HTML, CSS, and JavaScript
<html>
  <head>
    <title>My Snake Game</title>
    <style>
      canvas {
        border: 1px solid black;
      }
    </style>
  </head>
  <body>
    <canvas id="gameCanvas" width="400" height="400"></canvas>
    <script>
      // Get the canvas element
      const canvas = document.getElementById("gameCanvas");
      // Get the canvas context
      const ctx = canvas.getContext("2d");

      // Define the snake's position and size
      let snake = [{x: 150, y: 150}, {x: 140, y: 150}, {x: 130, y: 150}];
      const snakeSize = 10;

      // Define the direction of the snake's movement
      let dx = 10;
      let dy = 0;

      // Define the food's position and size
      let foodX;
      let foodY;
      const foodSize = 10;

      // Define the game's score
      let score = 0;

      function draw() {
        // Clear the canvas
        ctx.clearRect(0, 0, canvas.width, canvas.height);

        // Draw the snake
        ctx.fillStyle = "green";
        snake.forEach(se
