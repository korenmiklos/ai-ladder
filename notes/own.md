Problems are drawn at random from $Z \in U(0,1)$. A person of skill level $z$ can solve problems up to $Z<z$. There are two skill levels, $z_0$ and $z_1$.

Working on a problem requires time, committed before knowing the difficulty of the problem. One problem takes one unit of time to work on. (This is a normalization of units.) If a person is working alone on a problem, they can solve it with probability $z_i$, so their expected output per unit of time is $z_i$. 

When someone comes to a senior with a problem, it takes $h<1$ units of time to work on it. (Again, not knowing if it will be solved in the end.)

> This makes seniors very productive in teams, even if juniors are not really helpful in solving problems. 

Suppose $n_0$ juniors (with skill $z_0$) work in a team with a senior (with skill $z_1$). Juniors can solve $z_0$ fraction of the problems. The rest they take up to the senior, who then has to work on (communicate, think about) $n_0 (1-z_0)$ problems. Each problem takes $h$ time, so the time constraint of the senior pins down the team size, 
$$
n_0 = \frac {1} { h (1-z_0)}.
$$
Problems solved by juniors:
$$
n_0 z_0 = \frac {z_0}{h(1-z_0)}
$$
Problems solved by the senior:
$$
 n_0 (1-z_0) \frac{z_1-z_0}{1-z_0} = 
\frac {z_1-z_0}{h(1-z_0)}
$$
Team output per senior:
$$
\frac {z_1}{h(1-z_0)}
$$
The marginal returns to senior skill is greater in team than in solo work
$$
\frac{\partial q_1}{\partial z_1} = \frac{1}{h(1-z_0)} > 1.
$$

## Static equilibrium
There is a fixed supply of juniors $L_0$ and seniors $L_1$.

### Case 1: Too many juniors
Suppose $L_0 > n_0 L1 = L_1/[ h (1-z_0)]$. Then even if every senior builds a team, some juniors cannot joint, they will be working solo. The equilibrium is characterized by
$$
w_0 =  z_0
$$
(as pinned down by solo work) and
$$
w_1 = \frac {z_1} {h(1-z_0)} - w_0n_0 = 
\frac {z_1 - z_0} {h(1-z_0)}.
$$
The relative wage is
$$
\frac {w_1} {w_0} = 
\frac {z_1 - z_0} { h z_0(1-z_0)}.
$$
GDP:
$$
L_1 \frac {z_1 - z_0}{h(1-z_0)} + L_0 z_0
$$

#### Participation constraint
$$
w_1 \ge z_1
$$
$$
z_1 \ge  \frac{z_0}{1-h (1-z_0)}
$$
This ensures that team output is greater than the sum of individual outputs. We assume that parameters are such that PC holds.
### Case 2: Too many seniors
If the opposite inequality holds, then some seniors will work on their own, making
$$
w_1 =  z_1.
$$
Juniors are in scarce supply, so they capture all the rent from teamwork,
$$
w_0 = \frac{z_1}{h(1-z_0)n_0} - \frac{w_1}{n_0}
=  z_1[1 -  h (1-z_0)]
$$
Relative wage
$$
\frac {w_1}{w_0} = 
\frac 1{1-h(1-z_0)}
$$

## Technology and inequality
If ICT reduces $h$, its effect on inequality is ambiguous:
1. under Case 1, seniors capture all the surplus, inequality goes up
2. under Case 2, juniors defray the cost of paying the senior their outside option, inequality goes down

As long as the PC holds, $z_1$ does not matter for Case 2. In Case 1, inequality increases with $z_1$.

Wrt $z_0$, inequality decreases both in Case 1 and Case 2. 

# With AI
AI is like a junior, but is free, and can solve problems up to $z_A$. Communication cost is $h_A$.

For some configurations of $z_A$ and $h_A$, the senior will only hire AI, no juniors. Under Case 1, if juniors cannot use AI, the senior will use AI iff
$$
\frac {z_1 - z_0} {h(1-z_0)} < 
\frac {z_1} {h_A(1-z_A)}
$$
or
$$
\frac {h(1-z_0)} {h_A(1-z_A)} > 1-\frac{z_0}{z_1}
$$
Even if AI has the same $h$ and $z$ parameters as juniors, senior will only use AI, because they don't have to pay the outside option. In this case, all juniors will work alone.

## GDP
$$
L_1\frac {z_1} {h_A(1-z_A)} + L_0z_0 > Y_{\text{no AI}}
$$

> What if juniors can also use AI?

> Dynamic losses? Learning means that team member juniors become seniors with probability $\lambda$. 

# Dynamics
Continuous time. At any given point in time, $\delta L$ people are born. A fraction $\phi$ of them get senior skills $z_1$, $1-\phi$ get $z_0$. They each die with a Poisson arrival $\delta$, independent of skill. This implies that $L_0 = (1-\phi)L$ and $L_1=\phi L$ are the steady state, which holds in each instant.

## Learning by mentoring
A junior working in a team attains skill level $z_1$ with Poisson arrival rate $\lambda$. This may be a function of $z_0$ and $z_1$. 

This is a dynamic externality. Does not affect output immediate, but may change wage if people anticipate learning and internalize it. Irrespective of wages, supply of seniors is inelastic, so the amount of learning is "exogenous."

Steady state for skill levels:
$$
\delta L_1 = \delta L \phi + \lambda L_1/[ h (1-z_0)]
$$
Solve for $L_1$,
$$
\frac{L_1}L=  \frac\phi{1 - \frac{\lambda}{\delta h(1-z_0)}} > \phi
$$
Assume this is still small enough so that seniors are scarce and juniors are in "oversupply".
$L > L_1(1+1/[ h (1-z_0)])$, or
$$
\frac1{1+\frac1{h(1-z_0)}}>\frac{L_1}{L}=\frac\phi{1 - \frac{\lambda}{\delta h(1-z_0)}}
$$
or
$$
\frac{\lambda}{\delta}< (1 -\phi)h(1-z_0) - \phi. 
$$
Learning has to be slow relative to the death rate. 

Steady-state GDP per capita
$$
\frac{L_1}L \frac {z_1 - z_0}{h(1-z_0)} + \frac{L_0}L z_0 = 
\frac\phi{1 - \frac{\lambda}{\delta h(1-z_0)}}
\frac {z_1 - z_0}{h(1-z_0)} + \left[1-\frac\phi{1 - \frac{\lambda}{\delta h(1-z_0)}}\right]z_0
$$
$$
= z_0+\phi\frac{z_1-z_0[1+   h (1-z_0)] }{h(1-z_0) - \lambda/\delta}
$$
This is increasing in $\lambda/\delta$. 

## Steady-state GDP with AI
With AI, there is no learning because no teams are formed. Static GDP is the same as steady-state GDP, with $L_1 = \phi L$. 
$$
\frac{Y_{\text{AI}}}{L} = 
\phi\frac {z_1} {h_A(1-z_A)} + (1-\phi)z_0 =
z_0 + \phi \frac{z_1 - z_0 h_A(1-z_A)} {h_A(1-z_A)}
$$
Compare to steady-state GDP with no AI and learning. AI reduces steady-state GDP iff
$$
\frac{z_1 } {h_A(1-z_A)} - z_0 < \frac{z_1-z_0}{h(1-z_0) - \lambda/\delta} - \frac{z_0 }{1 - \lambda/[\delta h(1-z_0)]}.
$$
We know that AI is being used,
$$\tag{6}
\frac {z_1 - z_0} {h(1-z_0)} < 
\frac {z_1} {h_A(1-z_A)}
$$
When $\lambda =0$ and seniors have optimally chosen to use AI, steady-state GDP is bigger with AI than without.

> The RHS is strictly increasing in $\lambda/\delta$. There will be large enough $\lambda$ such that the inequality holds and AI reduces long-run GDP.

### Edge case: minimal benefit of AI
Suppose seniors are almost indifferent, but still use AI
$$
\frac {z_1 - z_0} {h(1-z_0)} \approx 
\frac {z_1} {h_A(1-z_A)}
$$

## Juniors internalizing learning
What if juniors accept lower wages in team, expecting that they will learn and become senior? The Bellman equation of the value of a junior job on a team, $J$, in the steady state:
$$
\delta J = w_{0,\text{team}} + \lambda[w_1/\delta - J]
$$
For juniors to be indifferent between team and solo, $J = z_0/\delta$. 
$$
z_0 = w_{0,\text{team}} + (w_1-z_0)\lambda/\delta 
$$
or
$$
w_{0,\text{team}} = z_0 -  (w_1-z_0)\lambda/\delta 
$$
In equilibrium, $w_1$ is the team output minus team junior wage, but team junior wage depends on $w_1$. 

> Check how this works in a competitive environment where firms compete for workers.

> There is a rent seeking behavior: seniors extract all the learning rent from juniors, including the rent that juniors expect to extract themselves after becoming seniors. This feels inefficient. This may imply that the senior does *not* adopt AI even when it would be static or dynamic GDP maximizing, to maintain his rents. (cf. Paco Buera)

$$
w_1 = \frac {z_1} {h(1-z_0)} - w_{0,\text{team}}n_0 =
\frac {\frac{z_1-z_0}{h(1-z_0)} + z_0\frac\lambda{\delta h(1-z_0)}}
	{1+\frac\lambda{\delta h(1-z_0)}}
$$
To use AI when learning is internalized,
$$
\tag{7}
\frac {\frac{z_1-z_0}{h(1-z_0)} + z_0\frac{\Lambda}{ h(1-z_0)}}
	{1+\frac\Lambda{ h(1-z_0)}} < \frac {z_1}{h_A(1-z_A)}
$$
AI increase steady-state GDP iff
$$\tag{8}
\frac{z_1 } {h_A(1-z_A)} - z_0 > \frac{z_1-z_0}{h(1-z_0) - \Lambda} - \frac{z_0 }{1 - \Lambda/[h(1-z_0)]}.
$$

