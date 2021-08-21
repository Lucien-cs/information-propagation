Abstract
========

Many studies have attempted to employ online social networks to affect people’s attitudes and behaviors. Moreover, the wide adoption of social media has caused information overload and has increased the competition for limited human attention in online social networks. However, limited human attention is unconsidered in information propagation models in online social networks, and previous studies indicated that the independent cascade model and the linear threshold model cannot offer an adequate explanation for information spread. Therefore, this study investigates whether considering limited human attention would facilitate information propagation in online social networks.

Introduction
============

This study investigates whether considering limited human attention would facilitate information propagation in online social networks.

Many studies have attempted to employ online social networks to affect people’s attitudes and behaviors (Bond et al., 2012; Valente, 2012). Moreover, the wide adoption of social media has caused information overload and has increased the competition for limited human attention in online social networks (Weng, 2012). As Simon foresaw, “a wealth of information that creates a poverty of attention” (Simon, 1971)

There has been an increasing interest in understanding the relationship between limited attention and information propagation in online social media (Weng, 2012; Feng, 2015).

However, limited attention is not well-considered in information propagation models in online social networks. Moreover, previous studies indicated that the independent cascade model and the linear threshold model, two of the classic information propagation models, cannot offer sufficient explanation for information spread (Hodas & Lerman, 2014).

Therefore, we propose an information propagation model integrating the effect of limited attention and social persuasion.

The results reveal that limited human attention may affect information propagation in online social networks; the proposed model predicts the propagation behaviors in online social media better than the classic models.

METHODOLOGY
===========

Problem definition
------------------

Given a directed social graph G = (V, E) and an activity log L = [(user, action, timestamp)], V represents users, E presents social relationship among users, and L represents that each user performed an action at timestamp.

Method
------

Prior study indicated the influence probability is proportional to its fraction of activated neighbors under information overload condition (Feng, 2015). Besides, conformity in social persuasion is applied for information propagation (Leung, 2014; Tang, 2013). We proposed a method integrating the effect of limited attention and peer conformity in social persuasion.

The intuition is that users in online social network tend to pay limited attention to received information from users who have stronger social conformity under information overload condition.

### Models

The Independent Cascade model (IC) and the Weighted Cascade model (WC) (Kempe, Kleinberg, & Tardos, 2003) are used as the baseline model. We compare the performance among the proposed model, the Peer Conformity model and the baseline models.

The probability of each edge (u, v) is annotated as p(u, v). In IC model, p(u, v) is assigned to 0.001. The WC model is a special case of IC model and p(u, v) is assigned to 1/in-degree(v) of activating v (Kempe et al., 2003).

In the Peer Conformity model, the probability of each edge (u, v) is defined as the ratio between the numbers of actions that a user v conformed to a particular friend u over the total number of actions performed by user u.

EXPERIMENTS AND RESULTS
=======================

Dataset
-------

|Dataset|Nodes|Edges|
|-|-|-|
|[higgs-twitter](http://snap.stanford.edu/data/higgs-twitter.html)|456,631|14,855,875|

Results
-------

|Model|p(u, v)|AUC for Twitter dataset|
|-|-|-|
|Independent Cascade|0.001|0.5000(±0.0001)|
|Weighted Cascade|1/k(v)|0.8641(±0.0001)|
|SIR |1-(1-γ)<sup>τ</sup>|0.5000(±0.0001)|
|fSIR |1-(1-γ/k(v))<sup>τ</sup>|0.8665(±0.0001)|

Note:
1) p < 0.05
2) c = peer(u, v), k(v) = in-degree of node v, τ is assumed as 2, 𝛾 is assumed as 0.35




Bibliography
============

De Domenico, M., Lima, A., Mougel, P., & Musolesi, M. (2013). The Anatomy of a Scientific Rumor. Scientific reports, 3. doi: ARTN 2980

Feng, L., Hu, Y., Li, B., Stanley, H. E., Havlin, S., & Braunstein, L. A. (2015). Competing for attention in social media under information overload conditions. PLoS ONE, 10(7). doi: 10.1371/journal.pone.0126090

Hodas, N. O., & Lerman, K. (2014). The simple rules of social contagion. Scientific Reports, 4. doi: 10.1038/srep04343

Hogg, T., & Lerman, K. (2012). Social dynamics of Digg. EPJ Data Science, 1(1), 5. doi: 10.1140/epjds5

Kempe, D., Kleinberg, J., & Tardos, É. (2003). Maximizing the spread of influence through a social network. Paper presented at the 9th ACM SIGKDD International Conference on Knowledge Discovery and Data Mining, KDD '03, Washington, DC.

Leung, T., & Chung, F. L. (2014). Persuasion driven influence propagation in social networks. Paper presented at the ASONAM 2014 - Proceedings of the 2014 IEEE/ACM International Conference on Advances in Social Networks Analysis and Mining.
