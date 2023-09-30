# Spirograph
Generate spirograph curve into arrays `x` and `y` such that the i^th point
 * in 2D is represented by `(x[i],y[i])`. The generating function is given by:
 * \f{eqnarray*}{
 * x &=& R\left[ (1-k) \cos (t) + l\cdot k\cdot\cos \left(\frac{1-k}{k}t\right)
 * \right]\\
 * y &=& R\left[ (1-k) \sin (t) - l\cdot k\cdot\sin \left(\frac{1-k}{k}t\right)
 * \right] \f}
 * where
 * * \f$R\f$ is the scaling parameter that we will consider \f$=1\f$
 * * \f$l=\frac{\rho}{r}\f$ is the relative distance of marker from the centre
 * of inner circle and \f$0\le l\le1\f$
 * * \f$\rho\f$ is physical distance of marker from centre of inner circle
 * * \f$r\f$ is the radius of inner circle
 * * \f$k=\frac{r}{R}\f$ is the ratio of radius of inner circle to outer circle
 * and \f$0<k<1\f$
 * * \f$R\f$ is the radius of outer circle
 * * \f$t\f$ is the angle of rotation of the point i.e., represents the time
 * parameter
 *
 * Since we are considering ratios, the actual values of \f$r\f$ and
 * \f$R\f$ are immaterial.
 *
 * @param [out] x output array containing absicca of points (must be
 * pre-allocated)
 * @param [out] y output array containing ordinates of points (must be
 * pre-allocated)
 * @param l the relative distance of marker from the centre of
 * inner circle and \f$0\le l\le1\f$
 * @param k the ratio of radius of inner circle to outer circle and
 * \f$0<k<1\f$
 * @param N number of sample points along the trajectory (higher = better
 * resolution but consumes more time and memory)
 * @param num_rot the number of rotations to perform (can be fractional value)
 */
