[Initial Scope Result](./spring_damper_example_1.png)

해당 프로젝트는 차량의 승차감을 결정하는 suspension system을 Simulink로 모델링하고 최적의 파라미터를 도출하는 과정을 담고 있습니다.

(m1)    body mass                                2500 kg
(m2)    suspension mass                          320 kg
(k1)    spring constant of suspension system     80,000 N/m
(k2)    spring constant of wheel and tire        500,000 N/m
(b1)    damping constant of suspension system    350 N.s/m
(b2)    damping constant of wheel and tire       15,020 N.s/m
(u)     control force = force from the controller we are going to design

사람은 1Hz 미만에서 멀미를 4~8Hz에서 피로감을 느낌. 이에 따라서 차체의 고유 진동수의 초기값을 wn=1.2Hz로 설정
damping ratio = 0.3으로 가정
http://www.nsv.co.kr/n2_engineering/theory_view.asp?idx=717&page=1&pagekey=352&search=&n=61

목표는 settling time 5초

wn = 1.2Hz = 7.54Hz
K1 = m1 * wn^2 = 142,125N/m
b1 = $b = 2\zeta \sqrt{m_1 K} = 11,310\text{ Ns/m}$ (Target $\zeta = 0.3$)



