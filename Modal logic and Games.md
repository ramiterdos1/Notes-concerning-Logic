17-01-2023  14:01

*Status* : #incomplete 

*Tags* : [[gametheory]] [[Modal Logic]]

# Modal logic and Games

---

## My thesis work depends on this literature

### Four views of Game Theory [[gametheory]]

1. ==_Descriptive_ ==: illustration of the behaviour of _rational_ individuals who recognize each other's _rationality_ and _reasoning abilities_.
2. ==Prescriptive== : That is, Internally consistent _recommendation_ to individuals on how to act in interactive situations, like advice to players. -- Eg. Arrow's impossibility, etc
3. ==Experimental Game Theory== : Aim to describe the actual behaviour of individuals.
4. ==Evolutionary Game Theory== : Outcomes are explained in terms of dynamic processes of natural selection.

My take : Bonanno says basically that for both these aspects of game theory the mathematical tool required would be ==[[Modal Logic]]==. 

> [!Question ]
>  Why Modal Logic?
>  A : The literature uses `epistemic logic`  - the logic of knowledge and belief and try to determine the assumptions on the beliefs and reasoning of the players ( in the solution concepts).

Description point 1. is at a meta level of behaviour understanding and point 2. of recommendation is at a level at the game play.

In the context of my ==work==. 
1. My first work on the use of FO(lfp) is ==novel== because it tries to do away from the use of Modal Logic as a description and prescription of [[normal form games]] and it's certain instantiations What was the significance? (??)
2. For the second and third work, we stick to the status quo of [[Modal Logic]], work on some variants of it and use it's powers to go about a formal description and prescription of a class of games called, social network games and large games.
3. The most unique aspect is that i am doing away with the extensive form that the logicians used.
4. Jam is confusing with the **reasoning** word, we are more prescriptive than reasoning!

### Interactive Situations

Situations where several individuals take actions that affect each other.

### Formal language of Game Theory
1. Detailed Description - Extensive Form Game form
2. Compact Description - [[normal form games]]


#### Useful in the following fields
1. Economics
2. Political Science
3. Military Science
4. Evolutionary Biology
5. Computer Science
6. Mathematical Logic
7. Experimental Psychology
8. Sociology
9. Social Philosophy


### Solution Concepts of Game Theory
Each solution concept associates with every game in a given class as outcome or set of outcomes.

==The debate in game theory has been in trying to justify a solution concept, the rational for it and the interpretation we associate with it. The main issue has been the relationship between the notion of common belief in rationality and non cooperative solution concepts such as rationalisability and Nash Equilibirum.== 

----
## Results that connect Modal Logic and Game Theory

1. Backwards induction in Perfect information games - characterised by Modal Logic
---
## Job Description of a Modal Logician

Mainly concerned with proving : 
1. Soundness
2. Completeness

---
## Use of Modal Operators
1. $\Box_i \alpha$ : Player $i$ believes $\alpha$
2.  $\Box_* \alpha$ : It is the common belief $\alpha$
----

## Properties of common belief 

1. $\Box_* ~\alpha \to \Box_i  ~\alpha$
2. $\Box_* ~\alpha \to \Box_i \Box_* ~\alpha$
3. $\left( \Box_* ~\alpha \to (\bigwedge\limits_{i\in [n]}~ \Box_i~\alpha)\right) \to (\bigwedge\limits_{i \in [n]} \Box_i ~\alpha \to \Box_* ~\alpha)$
----

## Mixed Strategy setting and Modal Logic

> [!Definitions]
> 1. Strategy : $S_i$
> 2. Mixed Strategy : $\Delta(S_i)$ : The set of all probability distributions over $S_i$
> 3. Let $v_i \in \Delta(S_i)$  be a distribution.
> 4. $v_i(s_i)$ is the probability assigned to $s_i$ by $v_i$.


---

## Strictly Dominated

A pure strategy $s_i \in S_i$ is strictly dominated by $v_i \in \Delta(S_i)$ , if 
- for all $s_{-i} \in S_{-i}$ : $\sum\limits_{x \in S_i} ~v_i(x) \times \pi_i(x,s_{-i}) > \pi_i(s_i,s_{-i})$
Given a game $\mathbb{G}$ , let $G^0=\mathbb{G}$ , let $G^k$ be the game obtained by deleting all the pure strategies of all the players that are strictly dominated in $G^{k-1}$. Let $G^{\infty} = \bigcap\limits_{k=1}^{\infty} G^k$ be the game obtained by applying this iterative procedure of elimination. Let $S^{\infty}$ be the set of strategy profiles in $G^{\infty}$ 

-----

## Game Language

### Atomic Propositions

Symbol | Intended Interpretation
--|--
$r_i$ | player $i$ is rational
$s^{\infty}$ | a strategy profile from $S^{\infty}$


### Formulas

 1. All players are rational : $$ r = r_1 \wedge r_2 \wedge \ldots \wedge r_n$$
----

## Semantics of Mixed Strategy Games

### Probabilistic Frame

$$\langle S, R_1,R_2,\ldots , R_n, (\pi_i)_{i \in [n]}\rangle$$

1.  $S$ is the same strategy set for all players.
2.  Each relation $R_i$ is serial, transitive, euclidean and $R_*$ is the transitive closure of $R_1 \cup R_2 \cup \ldots \cup R_n$.
3. $\pi_i$ is a full suport probability distribution on $S$, by which we mean : $\forall s \in S : \pi_i(s)>0$

---


## Belief at each state $\alpha$

Player $i$'s belief at each stage $\alpha$ is obtained by conditioning $\pi_i$ on $R_i(\alpha) = \{ ~\beta ~\mid~ \alpha ~R_i~ \beta \}$

Let $p_{i,\alpha}$ denote this function.

$$p_{i,\alpha}(\beta)= \begin{cases} \frac{\pi_i(\beta)}{\sum\limits_{\zeta \in R_i(\alpha)} \pi_i(\zeta)} \text{ if } \beta \in R_i(\alpha)\\ 0 \text{ if } \beta \not\in R_i(\alpha) \end{cases} $$ 
So this gives us a fuzzy knowledge set ( the normalisation keeps it probabilistic ) for player $i$ in strategy profile $\alpha$. Think of it as the probability player $i$ will make a transition to state $\beta$ from $\alpha$ , that is the probability of $\alpha \to_i \beta$ : this is computed as, if there exists no $\to_i$ edge to $\beta$ , then we assign $0$. Else, whatever probability is assigned to $\beta$ by the distribution associated by $\pi_i$ we condition it to the total probaility of all the $\to_i$ outgoing edges.

-----
## Results

> [! Propostion 1.]
>  Let $\mathbb{G}$ be a finite strategic form game. Then the following formula is valid in every model of $G$. $$\Box_* ~r \to s^{\infty}$$

---

## Solutions as consistent recommendations

1. $\alpha R_i \beta$ : meaning changed from `state beta is epistemically accessible from alpha for player i` to `player i can unilaterally deviate to state beta from state alpha`. 
2. That is in place of `reasoning` we are capturing the notion of what we are `able to do` ( computationally ).
3. It should be thought of as expressing the theory's recommendation to the players.

>[!note]
> The Formal Language changes as follows
> 1. $p_i,q_i \in \mathbb{Q}$ where $Q$ is the set of rational numbers.

Symbol | Intended Interpretation
  --|--
 $u_i=p_i$ |  Player $i$'s utlity is $p_i$
$q\leq p$ | the rational number $q$ is less than $p$
Nash| The pure strategy profile is a Nash Eq


----
## Benefits of using Modal Logic

1.  Formalised the notions of `common belief` in rationality which was earlier vaguely stated.
2.  Established the relationship to the iterative deletion of strictly dominated strategies.
3.  New solution concepts - `Strong Rationalisability` - i. it is common belief that no player has incorrect beliefs; ii. collectively players are  correct in their beliefs.

----

## Modelling 

> [!note]
> This portion is taken from [2]

To understand a social network phenomenon, $P$, we start by abstracting it out into a copy or _model_ $M$ of $P$ to try and analyse it .

```mermaid
graph LR

id1(Economic activity)
id2(Human Game)
id3(Formal Game)

id1 --players,rules,payoffs--> id2
id2 --remove intentions--> id3
```


---
### References
1. [bonanno]Modal logic and game theory two alternative approaches.pdf
2. [hodges]Four paradigms for Logical Games.pdf
3.  [bonanno,degremont]Logic and Game theory.pdf -- `haven't read yet`
4. 