# Credit Constraints and Endogenous Technology Choice in Production Networks

## Motivation

Firms are embedded in a connected production network in a closed economy. Their
technology choices determine which suppliers they rely on, how exposed they are to
sectoral shocks, and how shocks propagate through the economy. When production must
be financed in advance, these technology choices also depend on sectoral credit
conditions. A tightening of credit in one sector can therefore change not only that
sector's production scale, but also the pattern of input-output linkages chosen by firms
throughout the network.

This project studies the interaction between credit conditions, firms' endogenous
technology choices, and aggregate network fragility. The starting point is the endogenous
production-network framework of \citep{kopytovEndogenousProductionNetworks2024},
where firms choose technologies and input shares in response to supply-chain risk. I
extend this logic by introducing sector-specific credit limits that constrain firms'
ability to finance labor and intermediate-input payments before idiosyncratic
productivity shocks are realized. The credit mechanism is motivated by
\citep{wangCreditMarketImperfections}, who shows that credit-market imperfections
create an additional channel of interconnection in production networks beyond the usual
input-output cost channel. The quantitative and policy parts of the project are anchored
in the network statistics emphasized by \citep{herskovicNetworksProductionAsset2018},
who shows that network concentration and sparsity are economically meaningful objects
for aggregate risk. In this project, these statistics become policy targets: if credit
shocks induce firms to rechoose technologies in ways that create excessive concentration
or sparsity, sectoral taxes and subsidies can be used to lean against the resulting
network fragility.

The central research question is:

> How do sectoral credit conditions shape firms' technology choices and the structure of
> the production network, and how should the government respond when firms'
> technology reallocation after credit shocks creates aggregate fragility?

The proposal has three goals. First, the static model characterizes how sectoral credit
conditions affect technology choice through comparative statics which describe how firms change their reliance on suppliers when their own or their
suppliers' credit conditions change. Second, the dynamic model studies how persistent
credit shocks reshape network concentration, network sparsity, and aggregate output
when technology adjustment is costly. Third, the policy analysis asks whether sectoral
taxes and subsidies can reduce inefficient overconcentration and make the network less
vulnerable to bad shocks.

## Static Environment

There are \(N\) sectors indexed by \(i \in \{1,\ldots,N\}\). Sector \(i\) produces a
differentiated good \(Q_i\), which can be consumed by households or used as an
intermediate input by other firms. The economy is closed.

Goods market clearing requires

$$
Q_i
=
c_i
+
\sum_{k=1}^N X_{ki},
$$

where \(c_i\) is household final consumption of good \(i\), and \(X_{ki}\) is the use
of good \(i\) as an intermediate input by sector \(k\).

Each firm chooses a technology vector

$$
\alpha_i = (\alpha_{i1},\ldots,\alpha_{iN}),
$$

where \(\alpha_{ij}\) governs the intensity with which sector \(i\) uses goods from
sector \(j\). Following \citep{kopytovEndogenousProductionNetworks2024}, production
combines a stochastic productivity shock, technology-specific productivity, a
normalizing term useful for marginal-cost calculations, labor, and intermediate inputs:

$$
Y_i
=
e^{\epsilon_i}
A_i(\alpha_i)
\zeta_i(\alpha_i)
L_i^{\gamma_i}
\prod_{j=1}^N X_{ij}^{\alpha_{ij}}.
$$

The intended specification is decreasing returns to scale in measured production
inputs. Therefore, the exponents satisfy

$$
\gamma_i + \sum_{j=1}^N \alpha_{ij} < 1.
$$

The feasible technology set is therefore

$$
\mathcal{A}_i
=
\left\{
\alpha_i \in \mathbb{R}_+^N:
\gamma_i + \sum_{j=1}^N \alpha_{ij} < 1
\right\}.
$$

The shock \(\epsilon_i\) is not known at the beginning of the period. It is realized only
after firms have chosen their technology and committed borrowing needs. This timing
makes technology choice ex ante and exposes the firm to financing risk.

## Credit Constraint

Firms need working capital to pay labor and intermediate-input costs. Wages are
normalized to one. Sector \(i\)'s required borrowing is

$$
B_i
:=
L_i + \sum_{j=1}^N P_j X_{ij}.
$$

The firm faces a reduced-form sectoral credit constraint:

$$
B_i \leq \bar B_i
:=
\phi_i \mathbb{E}[P_i Q_i],
$$

where \(P_j\) is the price of input \(j\), \(P_i Q_i\) is sector \(i\)'s sales, and
\(\phi_i \in (0,1)\) captures the credit condition of sector \(i\). A higher \(\phi_i\)
means looser credit because a larger fraction of expected sales can be pledged.

Sectoral taxes or subsidies are also allowed. Let \(\tau_i\) denote a reduced-form
sectoral policy wedge, where \(\tau_i > 0\) is a tax and \(\tau_i < 0\) is a subsidy.
These wedges alter firms' private returns and provide the government with instruments
to correct network externalities.

## Timing and Firm Problems

The period has two stages.

### Stage 1: Ex Ante Technology and Borrowing Choice

Before \(\epsilon_i\) is realized, sector \(i\) chooses the technology vector
\(\alpha_i \in \mathcal{A}_i\) and planned borrowing \(B_i\). The firm maximizes
expected discounted profit subject to the credit constraint:

$$
\max_{\alpha_i,B_i}
\mathbb{E}
\left[
\Lambda
\Pi_i(\epsilon_i;\alpha_i,B_i)
\right]
$$

subject to

$$
B_i \leq \phi_i \mathbb{E}[P_i Q_i].
$$

Here \(\Lambda\) is the stochastic discount factor and \(\Pi_i\) is the profit realized
after \(\epsilon_i\) is known.

This stage captures the central tradeoff. A firm may choose a technology that is more
productive on average, but that technology may require a more input-intensive or more
credit-intensive production plan. Sectoral credit conditions therefore affect technology
choice directly.

### Stage 2: Ex Post Production and Repayment Feasibility

After \(\epsilon_i\) is realized, households observe the committed borrowing need
\(B_i\). They lend only to firms that can repay principal and interest. Let \(R_i\) denote
the interest rate faced by sector \(i\). A firm receives credit only if realized revenue can
cover repayment:

$$
(1-\tau_i) P_i Q_i(\epsilon_i)
\geq
(1+R_i) B_i.
$$

If this condition is satisfied, the firm borrows, pays labor and intermediate-input costs,
and produces. If the condition fails, households do not lend and the firm produces zero:

$$
Q_i(\epsilon_i)=0.
$$

Conditional on receiving credit, the firm solves a unit-cost minimization problem for
the chosen technology:

$$
K_i(P;\alpha_i,\epsilon_i)
=
\min_{\{L_i,\;X_{ij}\}_{j=1}^N}
L_i + \sum_{j=1}^N P_j X_{ij}
$$

subject to

$$
e^{\epsilon_i}
A_i(\alpha_i)
\zeta_i(\alpha_i)
L_i^{\gamma_i}
\prod_{j=1}^N X_{ij}^{\alpha_{ij}}
\geq 1,
$$

and the ex post working-capital limit

$$
L_i + \sum_{j=1}^N P_j X_{ij}
\leq
\bar B_i.
$$

In this second stage, \(\bar B_i\) is taken as fixed. This separates the ex ante choice of
technology and desired borrowing from the ex post feasibility of financing production.

## Households

Households consume a Cobb-Douglas final consumption aggregator:

$$
C
=
\prod_{i=1}^N c_i^{\omega_i},
\qquad
\sum_{i=1}^N \omega_i = 1.
$$

They supply labor and lend to firms. Preferences are

$$
\mathbb{E}_0
\sum_{t=0}^{\infty}
\beta^t
\left[
\log C_t
-
\chi \frac{N_t^{1+\varphi}}{1+\varphi}
\right],
$$

where \(N_t\) is aggregate labor supply, \(\beta\) is the discount factor, and
\(\varphi\) governs the curvature of labor disutility.

The household budget constraint includes wage income, consumption expenditure,
interest income from firm borrowing, firm profits, and rebates of taxes net of subsidy
costs. With the wage normalized to one, a period budget constraint can be written
schematically as

$$
\sum_{i=1}^N P_i c_i
+ A'
\leq
N
+ (1+R)A
+ \sum_{i=1}^N \Pi_i
+ T,
$$

where \(A\) denotes household financial assets, \(A'\) denotes next-period assets,
\(\sum_i \Pi_i\) denotes firm profits rebated to households, and \(T\) is net fiscal
rebates: tax revenues minus subsidy costs.

Households understand the committed borrowing amount \(B_i\). After \(\epsilon_i\)
is realized, they lend only to firms whose realized revenue is sufficient to repay. This
creates a discrete extensive margin of production: sufficiently bad productivity
realizations imply no borrowing and zero production. This idea follows the credit-market
screening logic in \citep{wangCreditMarketImperfections}.

## Analytical Targets

The static model is designed to study how credit conditions affect endogenous
technology choice. The first set of comparative statics is

$$
\frac{\partial \alpha_{ij}}{\partial \phi_i},
$$

which captures how sector \(i\)'s own credit condition changes its reliance on supplier
\(j\). If looser credit allows sector \(i\) to operate more input-intensive technologies,
then this derivative should reveal which supplier relationships expand when credit
constraints relax.

The second object is

$$
\frac{\partial \alpha_{ij}}{\partial \phi_j},
$$

which captures how supplier \(j\)'s credit condition affects sector \(i\)'s technology
choice. This derivative is central for understanding propagation through the supplier
side of the network: if sector \(j\)'s credit improves, its output may become cheaper or
more reliable, making it more attractive as an input.

The third object is the cross-credit derivative

$$
\frac{\partial^2 \alpha_{ij}}{\partial \phi_i \partial \phi_j}.
$$

This measures complementarity between buyer-side and supplier-side credit conditions.
A positive value would mean that sector \(i\)'s own credit relaxation makes it more
responsive to improvements in supplier \(j\)'s credit condition. A negative value would
indicate substitution: once sector \(i\)'s own financing improves, supplier \(j\)'s credit
condition matters less for \(i\)'s technology choice.

## Dynamic Extension

The next step is to introduce time-varying credit conditions. Keep the household side
simple, but let sectoral credit evolve according to

$$
\log \phi_{i,t}
=
\rho_i \log \phi_{i,t-1}
+
\mu_t
+
\nu_{i,t},
$$

where \(\mu_t\) is an aggregate credit shock common to all sectors and \(\nu_{i,t}\) is a
sector-specific credit shock. Because higher \(\phi_{i,t}\) relaxes the borrowing
constraint, an adverse credit shock is a negative innovation to \(\nu_{i,t}\).

Technology adjustment is costly. Define

$$
d_{i,t}
=
\left\|
\alpha_{i,t}
-
\alpha_{i,t-1}
\right\|_2,
$$

and let the adjustment cost be

$$
\kappa d_{i,t}^2.
$$

The dynamic firm problem then trades off the benefit of adapting input shares to current
credit and productivity conditions against the cost of changing the production
technology. This friction creates persistent network responses to temporary shocks.

## Quantitative Exercise

The quantitative model will study how productivity and credit shocks affect aggregate
output and the structure of the production network. Following
\citep{herskovicNetworksProductionAsset2018}, the analysis will focus on two network
statistics.

First, network concentration is measured by the negative entropy of the output-share
distribution:

$$
\mathcal{N}^C_t
=
\sum_{i=1}^N s_{i,t} \log s_{i,t},
$$

where \(s_{i,t}\) is sector \(i\)'s share of aggregate output. A higher value corresponds to
a more concentrated network.

Second, network sparsity is measured by the output-share-weighted negative entropy
of each sector's input-share distribution:

$$
\mathcal{N}^S_t
=
\sum_{i=1}^N
s_{i,t}
\left(
\sum_{j=1}^N
\alpha_{ij,t}
\log \alpha_{ij,t}
\right).
$$

This statistic is higher when sectors rely on fewer suppliers. It therefore captures how
specialized or sparse the input network is.

The main impulse-response exercises are:

1. An adverse productivity shock to a sector, modeled as a negative shock to
   \(\epsilon_i\) or to sectoral productivity \(A_i\).
2. An adverse credit shock to a sector, modeled as a negative shock to \(\nu_{i,t}\), which
   lowers \(\phi_{i,t}\) and tightens the borrowing constraint.

For each shock, the quantitative exercise will trace impulse responses of:

1. Aggregate output.
2. Network concentration \(\mathcal{C}_t\).
3. Network sparsity \(\mathcal{S}_t\).
4. Sectoral technology choices \(\alpha_{ij,t}\).
5. Sectoral prices and borrowing constraints.

## Externality and Industrial Policy

The model creates a natural externality. Individual firms choose technologies based on
private expected profits and private financing conditions. They internalize how input
choices affect their own production costs and repayment probability, but they do not
internalize how their technology choices affect the fragility of the aggregate production
network.

In particular, private technology choices may generate excessive concentration around
central suppliers. Such concentration can be privately efficient in normal times because
central suppliers may be productive or cheap. But it can make the whole network
vulnerable if the central sector is hit by an adverse productivity shock or a tightening of
credit conditions. The planner therefore faces a tradeoff between static production
efficiency and dynamic network resilience.

This opens the door to optimal industrial policy. Sectoral taxes and subsidies can be
used to discourage excessive dependence on fragile central sectors or to encourage
diversification toward suppliers that improve aggregate resilience. The policy problem is
therefore not simply to subsidize productive sectors, but to account for how sectoral
interventions reshape the endogenous network and the economy's exposure to bad
shocks.

The central policy question is:

> How should the government choose sectoral taxes and subsidies to reduce inefficient
> network overconcentration without sacrificing too much aggregate output?

The answer depends on the interaction between credit conditions, technology choice,
and network centrality. This interaction is precisely what the model is designed to make
transparent.
