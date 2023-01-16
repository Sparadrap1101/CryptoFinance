# CryptoFinance

## Selfish Mining Attack

`SelfishMiningAttack.ipynb`

We want to simulate a Silfish Mining Attack strategy against an honest mining strategy in order to determine which one is the most profitable.

### Here is the process of the attack:

The attacker will first premine X block ahead of the main chain before starting his attack. If the attacker is behind the main chain during the premining phase, he will abandon his blocks and restart mining from the last block of the main chain.

Once the premining phase is over, the attacker will launch his attack. This will end either if the attacker is Y blocks behind the main chain, or if he is ahead of the main chain at least Z blocks after the start of his attack.

X, Y, and Z are to be defined depending on the simulations you want to perform.

When we plot the profitability as a function of the relative mining power we obtain this graph:
<img src="SelfishMiningScreen.png"/>

## 1+2 Strategy

`1+2Strategy.ipynb`

This script will simulate a "1 + 2" attack. This attack consists in discovering as many blocks as possible on a cycle of 3 blocks 
To simulate this attack we take as parameters :
* q, the relative mining power of the attacker
* n, the number of attack cycles


When we plot the profitability as a function of the relative mining power we obtain this graph:
<img src="Screen1_1.png"/>

If we use fewer cycles then we see that 42% is still the solution but that it is possible to be unprofitable always because of the spikes:
<img src="Screen1_3.png"/>
<img src="Screen1_2.png"/>

We see that the attack is profitable when you have 42% of the total bitcoin mining power

