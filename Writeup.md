Effect of components:

	P makes the car move toward the aimed position. The further it is, the more it steers.
	A larger P value make the car reach that postion faster but when the car is near the aimed position,
	the angle is not reduced enough and the vehicle overshoots and end up on the other side of the target line.
	And the same thing happens in the other direction, so the car oscillates around the targeted postion.
	With a higher P value, the frequence of the oscillation goes up as the car changes direction faster.
	
	D impacts the speed "vertical speed" at which the car reaches the desired position.
	A high D values will prevent the vehicle to move too quickly to the postion. A small value will have
	little impact on the oscillating behavior due to the steering angle and the P value. Here we try to find
	a value that let the car reach the desired line quickly enough without oscillating (removing the oscillations).
	
	I factor deals with environmental factors or mecanical problems. If for some reason our steering
	angle is 0 because we've reached our target, and the road is uneven or the car tends to go to the
	left or to the right when the steering angle is 0, we won't be able to take that into account with a PD model.
	We then have a offset value that depends on how far we are from the desired position over time.
	This bias lets us know on which side our bias is and using I, we can recover from it.
	A high value for I will make a big difference of a litlle change and may nullify the second term and
	make the car overshoot as soon as something happens, but a too small value will prevent the vehicle to recover from the change fast enough.

How did I find the P, I and D coefficients ?

	I just took what we can find in the lesson and tried to move them around.
	But if I had to start from nowere I would have used the Twiddle algorithm or an SGD
	(I think it would be faster and better) to find the right set of parameters.
