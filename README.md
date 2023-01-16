# CryptoFinance

## Selfish Mining Attack

`SelfishMiningAttack.ipynb`

We want to simulate a Selfish Mining Attack strategy against an honest mining strategy in order to determine which one is the most profitable.

### Here is the process of the attack:

The attacker will first premine X block ahead of the main chain before starting his attack. If the attacker is behind the main chain during the premining phase, he will abandon his blocks and restart mining from the last block of the main chain.

Once the premining phase is over, the attacker will launch his attack. This will end either if the attacker is Y blocks behind the main chain, or if he is ahead of the main chain at least Z blocks after the start of his attack.

X, Y, and Z are to be defined depending on the simulations you want to perform.

#### When we simulate this attack with arguments X = 3, Y = 3 and Z = 6, we get this graph:

<img src="SelfishMiningScreen.png"/>

We can see that this strategy needs about 50% or more of the total hashrate to be better than the honest mining strategy.

## 1+2 Strategy

`1+2Strategy.ipynb`

We want to simulate a 1+2 Strategy against an honest mining strategy in order to determine which one is the most profitable.

### Here is the process of the strategy:

In this strategy, as soon as the attacker mines a block on the main chain before the honest miners, he will wait two more blocks before potentially making his blocks public.

If in the next two blocks the attacker mines at least one more, he will then publish them and overwrite the main chain because his will be longer. In the opposite case, he will simply abandon his blocks and start mining again from the main chain.

We want to know from how much hashrate this strategy becomes more profitable than honest mining with our simulation.

#### When we simulate this strategy with 10.000 cycles, we get this graph:

<img src="1+2StrategyScreen.png"/>

We can see that this strategy needs about 40% (42% in theory) of the total hashrate to be better than the honest mining strategy.

## Mining Game

`MiningGame.ipynb`

We want to simulate a mining game in order to determine if and when the honest mining strategy is not the best one.

### Here is the process of the game:

In this simulation, the attacker will have A tokens, the bank H tokens and actions with some cost can be perform.

We will have only 3 possible actions : CoinFlip, Override or Abandon.

CoinFlip will either gives a token to the attacker or gives a token to the bank 
with a cost C. Override will cause the bank to lose all its tokens and the attacker to lose H + 1 tokens, but the attacker will gain H + 1 - C €. Finally, Abandon will cause both players to lose all their tokens without any cost.

#### When we simulate this strategy with A = 0, H = 0, N = 5 and C = Q / 10 we get this graph:

<img src="MiningGameScreen.png"/>

We can see that the threshold value from which the honest mining strategy is no longer the best one starts at 35%.
