
# An Improvement of Controlling Quality of Large Scale Data in Thailand

Nuttapon Pattanavijit (1), Peerapon Vateekul (1), Kanoksri Sarinnapakorn (2)

(1) Department of Computer Engineering, Faculty of Engineering, Chulalongkorn University, Phayathai Road, Pathumwan, Bangkok, Thailand 10330

nuttapon.p@student.chula.ac.th, peerapon.v@chula.ac.th

(2) Hydro and Agro Informatics Institute, mInistry of Science and Technology, Thailand, 10400

kanoksri@haii.or.th

## Abstract

Extremely change in precipitation level such as water level can cause severe damage. In order to acknowledge changes, Hydro and Agro Informatics Institute has installed telemetry system across Thailand to collect and analyze precipitation level. However, to use its data in researching, incorrect data must be filtered. In previous work, we successfully detect various problems in water level data accurately. Still, missing pattern algorithm and outliers algorithm proposed in the previous work have run-time complexity up to `O(n^2)`, which are not quite suitable for large-scale data. In this paper, we aim to improve these algorithms, mainly focus on run-time complexity. As a result,  we can speed up the outlier algorithm to `O(n)` and the missing pattern to `O(n lg n)`. Moreover, compared with the previous work, we measure actual running time of our algorithms and found that they significantly help reduce the running time.

## Introduction

Thailand has faced many dreadful climate-related disaster including floods, droughts, and tropical cyclones. They have happened year after year and cause severe loss. For example, In 2011, seasonal flooding results in US$ 45.7 Billion damage to Thailand’s economy , which is 1.1% of the country’s GDP [1]. Also, the climate-related disaster bring difficulties to agriculture and industry, which are backbones of Thailand economy.

To handle these disaster, the government established many organization to cooperatively counteract with it. One of the organization is Hydro and Agro Informatics Institute (HAII). HAII’s main focus is to research and utilize knowledge in agricultural and water resource management to confront the climate disaster [2].

In order to conduct researches, they have collect precipitation data by installing telemetry systems across Thailand. The telemetry system is a device that is used to collect physical, chemical, and biological data from its various sensors [3]. For instance, river’s water level, rainfall level, humidity, and temperature can be measured. Today, HAII have already installed over 800 telemetry systems. The data collected from the telemetry systems is sent back to HAII’s server by using GPRS cellular network [4].

Sometimes, incorrect data is reported from the telemetry systems such as minus value of cumulative rainfall level, or river’s water level suddenly changed from one level to another, which are not possible. In addition, data loss can also be occurred due to poor cellular network in rural area. These inconsistent data is not suitable to be used in researches since it might lead to inaccurate results.

To filtered out incorrect data efficiently, our previous work called “Controlling Quality of Water-Level Data in Thailand” proposed algorithms to detect anomalies in water level data, which includes outliers, inhomogeneity, and missing pattern algorithm [5]. Example of anomaly data detected by these algorithms is illustrated in **Figure 1**, **Figure 2**, and **Figure 3**. However, when we implement this algorithm to use with real precipitation level data, a problem arise. Since HAII use `R` as a main programming languages for all data analytic tasks, implementing outliers and missing pattern algorithm may leads to `O(n^2)` in complexity. This inefficiency is originated from two main points. First, The bottleneck of both algorithms is occurred from clustering algorithm. The previous work use `DBSCAN` [6] as the clustering algorithm which have `O(n^2)` complexity if it is a naive implementation and `O(n lg n)` if it is implemented using special data structures that support fast region query such as `R*-Tree` or `k-d Tree` , which seem to be much more complex. Second, Our last work is implemented in HAII using `R` library called `”fpc”` which contains `DBSCAN` library that have `O(n^2)` complexity [7]. Thus, the overall algorithms’ complexity become `O(n^2)`.

This paper aim to propose an improvement in outliers and missing pattern algorithms for large-scale water level data. Our main goal is to refine both algorithm to be simple, yet expeditious, while bring out the same results as our previous work. We have reduce running time of outliers algorithm from `O(n^2)` or `O(n lg n)`, depends on data structures, `to O(n)`. Also, missing pattern is decresed from `O(n^2)` or `O(n lg^2 n)` to `O(n lg n)`. This can be  done by imitating the clustering result with more simple and fast approach which we will discuss later. The experimental result revealed that our approach significantly cut s down the overall running time in large-scale data.

The paper is organized as follows. Sections 2 describes how data was collected at HAII. Sections 3 recaps our previous work and points out problems. Our approach to refine the both algorithms are illustrated in Section 4. Experiment results are shown in Section 5. Last, Section 6 delivers a conclusion.

## Large-Scale Water Level Data

Currently, Hydro and Agro Informatics Institute (HAII) have already installed over 800 telemetry system across Thailand. Each system send data from its many sensors back to central database every 10 minutes via cellular network. From these figure, we can estimate that there are 3.45 million records of data added to database every month.

## Previous Data Quality Management

## Proposed Improved Algorithms 

## Experiments

## Conclusion

## References
- [1] http://www.worldbank.org/en/news/feature/2011/12/13/world-bank-supports-thailands-post-floods-recovery-effort
- [2] http://www.haii.or.th/haiiweb/index.php?option=com_content&task=view&id=94&Itemid=95&lang=en
- [3] http://www.thaiwater.net/web/index.php/aboutusen/524-telemeterringenen.html
- [4] http://www.thaiwater.net/web/index.php/aboutusen/525-tele-gprsen.html
- [5] Old Paper
- [6] http://citeseerx.ist.psu.edu/viewdoc/download;jsessionid=6549EE83A7F48705A9C3964F7A4D7C26?doi=10.1.1.71.1980&rep=rep1&type=pdf
- [7] http://cran.r-project.org/web/packages/fpc/fpc.pdf
