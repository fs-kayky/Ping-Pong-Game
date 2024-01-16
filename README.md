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
 
	// DRAW FIELD
    
    canvasCtx.fillStyle =  "#286047"
    
    canvasCtx.fillRect(0, 0, this.w, this.h)
    
    // DRAW CENTRAL LINE
    
    canvasCtx.fillStyle =  "#ffffff"
    
    canvasCtx.fillRect((field.w /  2  -  this.w /  2), 0, this.w, field.h)


### 2. Ball Movement and Collision Detection

        _calcPosition: function () {
        // Ball and paddle collision logic
        // ...
    
        // Ball and field boundary collision logic
        // ...
    },
    
    _reverseY: function () {
        this.directionY *= -1
    },
    _reverseX: function () {
        this.directionX *= -1
    },
    
    _speedUp: function () {
        this.speed += 3
    },
    
    _pointUp: function () {
        this.x = field.w / 2
        this.y = field.h / 2
        this._speedUp()
        rightPaddle.speedUp()
    },
    
    _move: function () {
        this.x += this.directionX * this.speed
        this.y += this.directionY * this.speed
    }
### 3. Right Paddle Movement and Speed-Up

    _draw: function () {
        canvasCtx.fillRect(this.x, this.y, this.w, this.h)
        this._move()
    },
    
    _move: function () {
        if (this.y + this.h / 2 < ball.y + ball.r) {
            this.y += this.speed
        } else {
            this.y -= this.speed
        }
    },
    
    speedUp: function () {
        this.speed += 2
    }

## Enjoy the Game!

Feel free to explore and modify the code to enhance the game further. Have fun playing Ping-Pong!

