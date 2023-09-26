# Redeem-moving-Ball explaination

This HTML and JavaScript code creates a simple animation of bouncing balls within a container. Here's a step-by-step explanation of the code:

1. **HTML Structure**:
   - The HTML document is relatively straightforward, with a `<div>` element that serves as a container for the bouncing balls. It has an `id` of "container" and specified width, height, border, and background color properties to define its appearance.

2. **JavaScript Code**:
   - The JavaScript code begins by defining several arrays and variables to manage the properties of the bouncing balls.
     - `palet`: An array containing different colors that will be randomly assigned to the balls.
     - Arrays (`balls`, `x_pos`, `y_pos`, `x_vel`, `y_vel`) to store information about each ball's HTML element, position, and velocity in the x and y directions.
     - `gravity`: A variable representing the gravitational force applied to the balls (simulated by reversing their velocity when they hit the container's boundaries).

   - The `ballCount(n)` function is defined to create a specified number (`n`) of balls and add them to the container. Inside this function:
     - It iterates `n` times to create each ball.
     - Randomly selects a color from the `palet` array for each ball.
     - Creates a new `<div>` element (representing the ball) and sets its CSS properties such as size, shape, color, and position.
     - Appends the ball element to the "container" div.
     - Randomly assigns initial positions and velocities to the ball, storing this information in the respective arrays.

   - The `moveBall()` function is responsible for animating the balls' movement.
     - It iterates through the balls array and updates their positions based on their current velocities.
     - If a ball reaches the container's boundaries (left/right or top/bottom), its velocity is reversed to simulate bouncing.
     - The updated positions are then applied to the CSS of each ball.
     - The `moveBall()` function is called again using `setTimeout()` to create an animation loop with a 50ms delay, giving the appearance of continuous motion.

   - Finally, the `ballCount(3)` function is called to create and animate three balls inside the container.
