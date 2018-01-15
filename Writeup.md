Effect of components:

	P makes the car move toward the center but doesn't adapt to the distance to the middle and this makes the car oscillated around the center.
	
	D removes the oscillating behavior but if the weels are aligned at an angle, by going straight the car would actually follow that angle and never reach the middle of the road.
	
	I is here to find that angle and correct the output to take it in account. After some time the bias angle is countered with the I component.

How did I find the P, I and D coefficients ?

	I just took what we can find in the lesson and tried to move them around. But if I had to start from nowere I would have used the Twiddle algorithm or an SGD (I think it would be faster and better) to find the right set of parameters.
