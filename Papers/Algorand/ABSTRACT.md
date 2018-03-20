# Algorand: Scaling Byzantine Agreements  for Cryptocurrencies

Yossi Gilad, Rotem Hemo, Silvio Micali, Georgios Vlachos, Nickolai Zeldovich

MIT CSAIL

## ABSTRACT

> Algorand is a new cryptocurrency that confirms transactions with latency on the order of a minute while scaling to many users.
 Algorand ensures that users never have divergent views of confirmed transactions, even if some of the users are malicious and the network is temporarily partitioned.
In contrast, existing cryptocurrencies allow for temporary forks and therefore require a long time, on the order of an hour, to confirm transactions with high confidence.
Algorand uses a new Byzantine Agreement (BA) protocol to reach consensus among users on the next set of trans-actions. 
To scale the consensus to many users, Algorand uses a novel mechanism based on Verifiable Random Functions that allows users to privately check whether they are selected to participate in the BA to agree on the next set of transactions, and to include a proof of their selection in
their network messages. 
In Algorand’s BA protocol, users do not keep any private state except for their private keys,
which allows Algorand to replace participants immediately after they send a message. 
This mitigates targeted attacks on chosen participants after their identity is revealed.
We implement Algorand and evaluate its performance on 1,000 EC2 virtual machines, simulating up to 500,000 users.
Experimental results show that Algorand confirms transactions in under a minute, achieves 125×Bitcoin’s throughput, and incurs almost no penalty for scaling to more users.