# indoor_soccer_trainer
A computer vision application to train the next generation of soccer player   
   
# Application 1: count number of juggles   
Place the webcam in front of the player and start juggling. The "trainer" will automatically count the number of juggles and output it on the image.   
When juggling, the ball goes up and down. Up and down. Up and down. In physics, it is called an oscillation. The idea was to:   
- isolate the ball (with a color filter),   
- calculate the location of its center,   
- isolate its Y coordinate (in 2D space, Y is the indicator of “height”),   
- count the number of peaks.   
NB: we actually take the inverse of the Y coordinate because in CV, the origin is on the top left corner (vs bottom left).   
   
# Application 2: shadow training   
In racing video games, you often see your best lap as a shadow (in some specific mode). The idea is to give you an indication about how (well) you are doing, in real time, without having to look away. Let’s take that idea, and transfer it to our super trainer. The pro player is demonstrating a trick on video. Then it is your turn. To help you, you can see on the screen where the ball is supposed to be and check if you are doing it right.   
I:   
- recorded myself doing the trick,   
- processed the video to isolate the ball,   
- calculate the location of its center and store it in a variable,   
- to be used in the live feed to draw the shadow ball.   
   
# Application 3: augmented indoor soccer   
Juggling and touching the ball is great, but it is useless unless you score more goals than your opponent. And for that, you need training on passing and shooting! The app can transform any room into a soccer pitch with virtual goals or virtual teammates.   
I assumed the camera was steady and at the level of the ground:   
- added the image of a goal onto the live image,   
- isolated the ball (with a color filter),   
- calculated the location of its center,   
- and checked if the ball crossed the line.   
   
Blog post: https://medium.com/@Enooooooormous/how-to-become-the-next-c-ronaldo-using-computer-vision-266aec1e1720
