
# An Improvement of Controlling Quality of Large Scale Data in Thailand

Nuttapon Pattanavijit (1), Peerapon Vateekul (1), Kanoksri Sarinnapakorn (2)

(1) Department of Computer Engineering, Faculty of Engineering, Chulalongkorn University, Phayathai Road, Pathumwan, Bangkok, Thailand 10330

nuttapon.p@student.chula.ac.th, peerapon.v@chula.ac.th

(2) Hydro and Agro Informatics Institute, mInistry of Science and Technology, Thailand, 10400

kanoksri@haii.or.th

## 1. Abstract

Extremely change in precipitation level such as water level can cause severe damage. In order to acknowledge changes in water level among Thailand, Hydro and Agro Informatics Institute has installed automated telemetry system (ATS) in all places. However, to use its data in researching, incorrect data must be filtered. In previous work, we successfully detect various problems in water level data accurately. However, missing pattern algorithm and outliers algorithm proposed in previous work have run-time complexity up to O(n^2), which is not suitable for large-scale data. In this paper, we aim to improve these algorithms from our previous work, mainly focus on run-time complexity. As a result,  we can speed up outlier algorithm to O(n) and missing pattern to  O(n lg n). Furthermore, compared with the previous work, we measure run-time of our algorithms and found that our algorithms significantly reduce the running time.

