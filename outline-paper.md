
# An Improvement of Controlling Quality of Large Scale Data in Thailand

Nuttapon Pattanavijit (1), Peerapon Vateekul (1), Kanoksri Sarinnapakorn (2)

(1) Department of Computer Engineering, Faculty of Engineering, Chulalongkorn University, Phayathai Road, Pathumwan, Bangkok, Thailand 10330

nuttapon.p@student.chula.ac.th, peerapon.v@chula.ac.th

(2) Hydro and Agro Informatics Institute, mInistry of Science and Technology, Thailand, 10400

kanoksri@haii.or.th

## Abstract

Extremely change in precipitation level such as water level can cause severe damage. In order to acknowledge changes, Hydro and Agro Informatics Institute has installed telemetry system across Thailand to collect and analyze precipitation level. However, to use its data in researching, incorrect data must be filtered. In previous work, we successfully detect various problems in water level data accurately. Still, missing pattern algorithm and outliers algorithm proposed in the previous work have run-time complexity up to O(n^2), which are not quite suitable for large-scale data. In this paper, we aim to improve these algorithms, mainly focus on run-time complexity. As a result,  we can speed up the outlier algorithm to O(n) and the missing pattern to O(n lg n). Moreover, compared with the previous work, we measure actual running time of our algorithms and found that they significantly help reduce the running time.

## Introduction

	Thailand has faced many dreadful climate-related disaster including floods, droughts, and tropical cyclones. They have happened year after year and cause severe loss. For example, In 2011, seasonal flooding results in US$ 45.7 Billion damage to Thailand’s economy , which is 1.1% of the country’s GDP[\[1\]](http://www.worldbank.org/en/news/feature/2011/12/13/world-bank-supports-thailands-post-floods-recovery-effort). Also, the climate-related disaster bring difficulties to agriculture and industry, which are backbones of Thailand economy.

	To handle these disaster, the government established many organization to cooperatively counteract with it. One of the organization is Hydro and Agro Informatics Institute (HAII). HAII’s main focus is to research and utilize knowledge in agricultural and water resource management to confront the climate disaster[\[2\]](http://www.haii.or.th/haiiweb/index.php?option=com_content&task=view&id=94&Itemid=95&lang=en).

	In order to conduct researches, They have collect precipitation data by installing telemetry systems across Thailand. The telemetry system is a device that is used to collect physical, chemical, and biological data from its various sensors [\[3\]](http://www.thaiwater.net/web/index.php/aboutusen/524-telemeterringenen.html). For instance, river’s water level, rainfall level, humidity, and temperature can be measured. Today, HAII have already installed over 800 telemetry systems. The data collected from the telemetry systems are sent back to HAII’s server by using GPRS cellular network[\[4\]](http://www.thaiwater.net/web/index.php/aboutusen/525-tele-gprsen.html).

	Sometimes, incorrect data is reported from the telemetry systems such as minus value of cumulative rainfall level, or river’s water level suddenly changed from one level to another, which is not possible. In addition, data loss can be occurred due to poor cellular network in rural area. These inconsistent value is not suitable to be used in researches since it might lead to inaccurate results.

	To filtered out incorrect data efficiently, …



## Large-Scale Water Level Data

## Previous Data Quality Management

## Proposed Improved Algorithms 

## Experiments

## Conclusion

## References
