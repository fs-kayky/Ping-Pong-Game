# Ping-Pong Game in JavaScript

Welcome to the Ping-Pong Game! This simple and fun game is implemented in JavaScript using HTML5 Canvas. Test your skills against the computer and see how many points you can score.

## Game Features

- **Responsive Design:** The game adapts to different screen sizes, providing an optimal gaming experience.
- **Smooth Animation:** Enjoy smooth and fluid animations, thanks to the use of `requestAnimationFrame`.
- **Dynamic Paddle Movement:** The left paddle follows your mouse movements, providing precise control.
- **Intelligent Computer Opponent:** The right paddle is controlled by a smart algorithm, making the game challenging.
- **Scoring System:** Keep track of your score against the computer with a clear and bold display.

## How to Play

- Move your mouse vertically to control the left paddle.
- The objective is to hit the ball past the computer's paddle to score a point.
- Be careful! If the ball passes your paddle, the computer scores a point.
- The game speeds up as you score more points, providing an increasingly challenging experience.

## Screenshots

![Gameplay Screenshot](img/Captura%20de%20tela%202024-01-15%20211506.png)

## Click Here to Play

[Click Here](https://fs-kayky.github.io/Ping-Pong-Game/) to open the game in another tab and start playing!

## Code Highlights

### 1. Field and Line Drawing

```javascript
// DRAW FIELD
canvasCtx.fillStyle = "#286047"
canvasCtx.fillRect(0, 0, this.w, this.h)

// DRAW CENTRAL LINE
canvasCtx.fillStyle = "#ffffff"
canvasCtx.fillRect((field.w / 2 - this.w / 2), 0, this.w, field.h)
