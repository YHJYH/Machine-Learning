### binary classification <br>
比方说有一个64\*64的图片，这幅图片的<b>input feature vector</b> x = \[r1,r2...r(64\*64),g1,g2...g(64\*64),b1,b2...b(64\*64)]^T, rgb分别表示red，green，blue；<br>
x的<b>dimension</b>是n_x = 64\*64\*3 = 12288
#### notation<br>
(x,y) x属于R^nx, y属于{0，1}<br>
有m个training examples：<b>training set</b> = {（x^(1),y^(1)）,(x^(2),y^(2)),...(x^(m),y^(m))}<br>
m = m_train, m_test = #test example<br>
X: m columes, each colume is x^(1), x^(2),...x^(m)<br>
so X is a R_nx\*m dimensional matrix.<br>
X.shape = (nx,m)<br>
Y = \[y^(1) y^(2) ... y^(m)]<br>
so Y is a R_1\*m dimensional matrix<br>
Y.shape = (1,m)<br>
### Logistic regression
given x, want y-hat (estimated y), y-hat = P(y=1|x)<br>
<b>linear regression</b>: y-hat = w^T \* x + b<br>
w属于R^nx dimension, b属于R<br>
<b>logistic regression</b>: sigmoid(linear regression): 确保值在\[0,1]<br>


