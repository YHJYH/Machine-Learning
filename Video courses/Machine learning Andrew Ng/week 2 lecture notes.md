multiple features<br>
gradient descent on multiple variables<br>
<br>
<b>features scaling</b>: make sure features are on a smiliar scale<br>
method: x_n = (x_n - miu_n)/s_n <b>mean normalization</b>: make features have approximately zero mean<br>
miu_n = average , s_n = standardized error<br>
<br>
test the gradient descent: <b>min<i>J</i> converges</b><br>
plot cost function <i>J</i> against number of iterations (a converging curve)<br>
if learning rate is <b>too small</b>: slow convergence<br>
if learning rate is <b>too large</b>: no convergence<br>
<br>
polynomial regression<br>
can transfer to linear regression<br>
e.g. x_2 = x^2, x_3 = x^3<br>
need feature scaling<br>
<br>
<b>normal equation</b>: solve for theta in J(theta) analytically.<br>
1D: differentiation<br>
n-D: partial differentiation<br>
alternatively: using matrix<br>
theta = (X^T X)^-1 X^T y<br>
where, X is the <b>feature matix</b> represents all features of all examples, y is a <b>label vector</b> contains the labels/outputs of each example<br>
<br>
advantages and disadvantages of gradient descent and normal equation<br>
Gradient descent:<br>
1. need to choose learning rate alpha (NE doesn't);<br>
2. needs many iterations (NE doesn't);<br>
3. works well when n is large (NE is slow if n is large, needs to compute the matrix operation);<br>
<br>
Q: what does it mean when there is no inverse?<br>
non-invertible matrix: <b>singular/degenerate matrix</b><br>
1. two features are related (<b>linearly dependent</b>), e.g. x_1 = area in m^2, x_2 = area in feet^2;<br>
2. too many features (m <= n, # of samples <= # of features): then delete some features or use <b>regularization</b> (later topic)<br>
<br>
Octave tutorial is skipped<br>


