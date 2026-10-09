# Financial Distortions and Endogenous Technology Choice in Production Networks

## Motivation

Firms are embedded in a connected production network in a closed economy. Their
technology choices determine which suppliers they rely on, how exposed they are to
sectoral shocks, and how shocks propagate through the economy. When production must
be financed in advance, sectoral financial distortions affect firms through borrowing
costs. A financially distorted sector produces less than in the efficient allocation, its
price rises, and downstream firms respond by changing their technology and supplier
dependence.

This project studies how financial distortions shape technology choice and aggregate
network fragility. The starting point is the endogenous production-network framework of
\citep{kopytovEndogenousProductionNetworks2024}, where firms choose technologies and
input shares in response to supply-chain risk. I shift the focus from uncertainty-driven
technology choice to **finance-driven technology choice**: sectoral financial conditions
distort production prices, and these distorted prices make private technology choices
depart from the efficient network. The credit mechanism is motivated by
\citep{wangCreditMarketImperfections}, who shows that credit-market imperfections
create an additional channel of interconnection in production networks beyond the usual
input-output cost channel. The quantitative and policy parts of the project are anchored
in the network statistics emphasized by \citep{herskovicNetworksProductionAsset2018},
who shows that network concentration and sparsity are economically meaningful objects
for aggregate risk. In this project, these statistics become policy targets: if financial
shocks induce firms to rechoose technologies in ways that create excessive concentration
or sparsity, sectoral taxes and subsidies can be used to lean against the resulting
network fragility.

The central research question is:

> How do sectoral financial distortions shape firms' technology choices and the
> structure of the production network, and how should the government respond when
> firms' technology reallocation after financial shocks creates aggregate fragility?

The proposal has three goals. First, the static model characterizes how sectoral
borrowing rates affect technology choice through comparative statics that describe how
firms change their reliance on suppliers when their own or their suppliers' financial
conditions change. Second, the dynamic model studies how persistent financial shocks
reshape network concentration, network sparsity, and aggregate output when technology
adjustment is costly. Third, the policy analysis asks whether sectoral taxes and
subsidies can reduce inefficient overconcentration and make the network less vulnerable
to bad shocks.

## Static Environment

There are \(N\) sectors indexed by \(i \in \{1,\ldots,N\}\). Sector \(i\) produces a
differentiated good \(Y_i\), which can be consumed by households or used as an
intermediate input by firms in other sectors. The economy is closed.

Each sector contains a unit mass of firms \(f \in [0,1]\). Firm \(f\) in sector \(i\)
produces \(Y_{if}\). A competitive sectoral aggregator purchases firm output and
produces the sectoral good according to

$$
Y_i
=
\int_0^1
\left(
\frac{Y_{if}}{\theta_i}
\right)^{\theta_i}
df.
$$

The aggregator earns zero profit. This avoids the counterfactual implication that a bad
firm-level productivity realization shuts down an entire sector. Low-productivity firms
may produce zero while the sector continues to operate through other firms.

Goods market clearing requires

$$
Y_i
=
c_i
+
\sum_{k=1}^N \int^1_0 X_{kf, i} df,
$$

where \(c_i\) is household final consumption of good \(i\), and \(X_{ki}\) is the use
of good \(i\) as an intermediate input by sector \(k\).

Firm \(f\) in sector \(i\) chooses a technology vector

$$
\alpha_{if} = (\alpha_{if,1},\ldots,\alpha_{if,N}),
$$

where \(\alpha_{if,j}\) governs the intensity with which firm \(f\) in sector \(i\)
uses goods from sector \(j\). Following
\citep{kopytovEndogenousProductionNetworks2024}, production combines a stochastic
productivity shock, technology-specific productivity, a normalizing term useful for
marginal-cost calculations, labor, and intermediate inputs:

$$
Y_{if}
=
e^{\epsilon_{if}}
A_i(\alpha_{if})
\zeta_i(\alpha_{if})
L_{if}^{\gamma_i}
\prod_{j=1}^N X_{if,j}^{\alpha_{if,j}}.
$$

The intended specification is decreasing returns to scale in measured production
inputs. Therefore, the exponents satisfy

$$
\gamma_i + \sum_{j=1}^N \alpha_{if,j}
=
\psi
<
1.
$$

The feasible technology set is therefore

$$
\mathcal{A}_i
=
\left\{
\alpha_{if} \in \mathbb{R}_+^N:
\gamma_i + \sum_{j=1}^N \alpha_{if,j} = \psi < 1
\right\}.
$$

The firm-level productivity shock has a persistent sectoral component and an
idiosyncratic firm component:

$$
\epsilon_{if,t}
=
z_{i,t}
+
u_{if,t}.
$$

The sectoral component \(z_{i,t}\) affects sectoral output and prices. The firm-level
component \(u_{if,t}\) is idiosyncratic noise. With a unit mass of firms, this
idiosyncratic component shapes the distribution of active firms but does not by itself
generate aggregate sectoral risk.

## Financial Distortion

Firms need working capital to pay labor and intermediate-input costs before sales are
received. Wages are normalized to one. Firm \(f\) in sector \(i\)'s borrowing need is

$$
B_{if}
:=
L_{if} + \sum_{j=1}^N P_j X_{if,j}.
$$

All firms in sector \(i\) face the same sector-specific gross borrowing rate
\(R_i > R^f\), where \(R^f\) is the economy-wide safe gross rate. The spread
\(R_i - R^f\) is the reduced-form financial distortion in the model. It stands in for
intermediation costs that creditors incur when lending to sector \(i\): the cost of
verifying a firm's realized productivity before disbursing funds, and the cost of
keeping committed liquidity available for every firm in the sector even though only
some of them end up drawing it. These costs are not derived from a lender's problem;
the spread is taken as a sectoral primitive. A higher \(R_i\) means that working
capital is more expensive in sector \(i\), lowering production relative to the efficient
allocation and raising the sector's equilibrium price.

There is no separate reduced-form borrowing-capacity parameter \(\phi_i\). Financial
conditions enter through the price of working capital:

$$
R_i \uparrow
\quad\Rightarrow\quad
\text{effective production cost in sector }i \uparrow.
$$

Sectoral taxes or subsidies are also allowed. Let \(\tau_i\) denote a reduced-form
sectoral policy wedge, where \(\tau_i > 0\) is a tax and \(\tau_i < 0\) is a subsidy.
These wedges alter firms' private returns and provide the government with instruments
to correct network externalities.

## Timing and Firm Problems

The period has two stages.

### Stage 1: Ex Ante Borrowing Choice

Before \(\epsilon_{if}\) is realized, firm \(f\) in sector \(i\) commits to a
borrowing amount \(B_{if}\). It does not choose technology at this stage. The
commitment is one-sided: the firm cannot borrow more than \(B_{if}\), but the creditor
disburses the funds only after productivity is realized and only if the firm will be
able to repay. Let \(\mathbbm{1}_{if}\) denote the indicator that firm \(f\) is funded.
The firm maximizes SDF-discounted expected profit:

$$
\max_{B_{if} \geq 0}
\mathbb{E}
\left[
\Lambda\,
\mathbbm{1}_{if}
\left(
(1-\tau_i)P_iY_{if}
-
R_iB_{if}
\right)
\right],
$$

where \(\Lambda\) is the stochastic discount factor and \(R_i\) is taken as given.
Borrowing is committed before productivity is known because the firm must secure
liquidity before production takes place.

This stage captures the financial distortion. A higher \(R_i\) makes working capital
more expensive, reduces the optimal commitment, and affects the firm's subsequent
technology choice through the liquidity available for production.

### Stage 2: Ex Post Technology and Production Choice

After \(\epsilon_{if}\) is realized, the creditor observes it and disburses the
committed amount if and only if repayment is feasible:

$$
\mathbbm{1}_{if}
=
\mathbbm{1}
\left\{
(1-\tau_i)P_iY_{if}(\epsilon_{if};B_{if}) \geq R_iB_{if}
\right\}.
$$

Disbursement is all-or-nothing: a funded firm draws exactly \(B_{if}\), and an unfunded
firm draws nothing and produces nothing, \(Y_{if}=0\). Because the production function
is increasing in \(\epsilon_{if}\), this defines a sectoral cutoff \(\bar\epsilon_i\)
such that firms with \(\epsilon_{if} \geq \bar\epsilon_i\) are funded and the rest are
rationed. The creditor never lends to a firm that cannot repay, so no loan is ever
written off; low-productivity firms exit through rationing rather than default.

A funded firm then chooses its technology vector \(\alpha_{if} \in \mathcal{A}_i\),
labor \(L_{if}\), and intermediate inputs \(\{X_{if,j}\}_{j=1}^N\), spending the full
committed amount:

$$
L_{if} + \sum_{j=1}^N P_j X_{if,j}
=
B_{if}.
$$

It solves

$$
\max_{\alpha_{if},L_{if},\{X_{if,j}\}}
(1-\tau_i)P_iY_{if}
-
R_iB_{if}
$$

subject to the budget above and

$$
Y_{if}
=
e^{\epsilon_{if}}
A_i(\alpha_{if})
\zeta_i(\alpha_{if})
L_{if}^{\gamma_i}
\prod_{j=1}^N X_{if,j}^{\alpha_{if,j}}.
$$

Since \(R_iB_{if}\) is sunk at this stage, the funded firm's problem reduces to
maximizing output given the budget, so its technology choice depends on prices and
the committed scale but not directly on \(R_i\). The rate affects technology only
through the stage-1 commitment and through equilibrium prices.

Thus financial distortions affect technology choice through the price system. A sector
with a high \(R_i\) produces less and has a higher equilibrium price, making it less
attractive as a supplier. Other firms then re-optimize their technology vectors, changing
the production network.

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
\chi \frac{L_t^{1+\varphi}}{1+\varphi}
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
L
+ \sum_{i=1}^N \int_0^1 \mathbbm{1}_{if}\, R_i B_{if}\,df
+ \sum_{i=1}^N \Pi_i
+ T,
$$

where \(A'\) denotes next-period assets, \(\sum_i \Pi_i\) denotes firm profits rebated
to households, and \(T\) is net fiscal rebates: tax revenues minus subsidy costs. The
sectoral gross rate \(R_i\) summarizes the financial terms at which firms in sector \(i\)
obtain working capital.

The household side is intentionally kept simple. The key financial object for the firm is
the sector-specific rate \(R_i\), not a household screening rule. This follows the spirit of
\citep{wangCreditMarketImperfections} by letting financial conditions shape production
decisions, while keeping the reduced-form financial distortion on the price side.

## Network Statistics

The paper focuses on two summary statistics of the equilibrium network, following
\citep{herskovicNetworksProductionAsset2018}. Let
\(\omega^Y_i \equiv P_iY_i / \sum_{k=1}^N P_kY_k\) denote sector \(i\)'s share of
aggregate output, and let \(\alpha_{i,j} \equiv \int_0^1 \alpha_{if,j}\,df\) denote the
sector-average intensity with which sector \(i\) uses good \(j\).

Network concentration is the negative entropy of the output-share distribution:

$$
\mathcal{N}^C
=
\sum_{i=1}^N \omega^Y_i \log \omega^Y_i.
$$

A higher value means that output is concentrated in fewer sectors.

Sectoral sparsity is the negative entropy of sector \(i\)'s input-share distribution:

$$
\mathcal{N}^S_i
=
\sum_{j=1}^N \alpha_{i,j} \log \alpha_{i,j}.
$$

A higher \(\mathcal{N}^S_i\) means that sector \(i\) relies on fewer suppliers, so its
input structure is more specialized. Network sparsity is the output-share-weighted
average of sectoral sparsity:

$$
\mathcal{N}^S
=
\sum_{i=1}^N \omega^Y_i\, \mathcal{N}^S_i
=
\sum_{i=1}^N \omega^Y_i
\left(
\sum_{j=1}^N \alpha_{i,j} \log \alpha_{i,j}
\right).
$$

Both statistics are endogenous in this model: financial conditions \(\{R_i\}\) change
technology choices \(\alpha_{if,j}\), which change input shares, prices, output shares,
and hence \(\mathcal{N}^C\) and \(\mathcal{N}^S\).

## Analytical Targets

The static model is designed to study how financial distortions affect endogenous
technology choice through prices and working-capital costs, and how those choices
aggregate into the network statistics above. The comparative statics are organized
from the aggregate level to the firm level.

### Monetary Policy and Network Structure

Write the sectoral rate as \(R_i = R^f + s_i\), where \(s_i > 0\) is the sectoral
spread. Holding spreads fixed, a change in the safe rate shifts every sector's cost
of working capital at once. The first targets are

$$
\frac{\partial \mathcal{N}^C}{\partial R^f}
\qquad\text{and}\qquad
\frac{\partial \mathcal{N}^S}{\partial R^f}.
$$

These ask whether a uniform tightening of financial conditions, the monetary policy
side of the model, makes the network more concentrated and more sparse. The sign is not
obvious: a higher \(R^f\) raises costs in every sector, but sectors differ in
\(\gamma_i\), in their position in the network, and in their sensitivity to working-capital
costs, so output shares and input shares need not move proportionally.

### Sectoral Financial Shocks and Input Structure

The second target is the response of a sector's own input structure to its own
financial condition:

$$
\frac{\partial \mathcal{N}^S_i}{\partial R_i}.
$$

This captures how a sector reorganizes its input mix when it faces a sectoral financial
shock. A higher \(R_i\) raises the cost of every unit of working capital in sector \(i\),
which can push firms toward technologies that economize on purchased inputs or toward
a narrower set of suppliers.

### Propagation Through Technology Choice

The remaining targets are at the firm level and concern the input intensity
\(\alpha_{if,j}\) of firm \(f\) in sector \(i\) on good \(j\). Sector-average responses
follow by integrating over \(f\).

Downstream propagation:

$$
\frac{\partial \alpha_{if,j}}{\partial R_j}.
$$

This captures how supplier \(j\)'s financial condition affects the technology choice of
its customers. If \(R_j\) rises, sector \(j\)'s production cost and price rise, making
good \(j\) less attractive as an input, so the financial shock in \(j\) travels downstream
through the input choices of firms in \(i\).

Upstream propagation:

$$
\frac{\partial \alpha_{if,j}}{\partial R_i}.
$$

This captures how a buyer's own financial condition changes its reliance on supplier
\(j\). A higher \(R_i\) raises the cost of working capital for firms in sector \(i\),
lowers their optimal production scale, and changes which technologies are feasible or
profitable after shocks are realized. The resulting change in demand for good \(j\)
transmits the financial shock in \(i\) upstream to its suppliers.

Interaction between own and upstream financial conditions:

$$
\frac{\partial^2 \alpha_{if,j}}{\partial R_i \partial R_j}.
$$

This cross derivative asks whether a sector's own financing cost changes how sensitive
its technology choice is to supplier \(j\)'s financing cost. It therefore measures
whether a financial shock in sector \(i\) amplifies or dampens the propagation of
financial shocks arriving from upstream.

## Dynamic Extension

The next step is to introduce persistent sectoral financial conditions. The productivity
process is decomposed into a persistent sectoral component and iid firm-level noise:

$$
z_{i,t}
=
\rho_i^z z_{i,t-1}
+
\eta^z_{i,t},
$$

and

$$
u_{if,t}
\sim
F_i,
$$

where \(u_{if,t}\) is iid across firms and time. The firm-level component generates
cross-sectional dispersion in production outcomes, while the persistent sectoral
component generates aggregate sectoral productivity movements.

Financial conditions are summarized by a sectoral intermediation wedge \(s_{i,t}\),
the reduced-form counterpart of verification and committed-liquidity costs, which
follows

$$
s_{i,t}
=
\rho_i^s s_{i,t-1}
+
\eta^s_{i,t}.
$$

The sectoral gross borrowing rate is

$$
R_{i,t}
=
R_t^f
+
s_{i,t},
$$

where \(R_t^f\) is the economy-wide safe gross rate. An adverse financial shock is
\(\eta^s_{i,t}>0\), which raises \(s_{i,t}\) and therefore raises \(R_{i,t}\). Importantly,
\(R_{i,t}\) does not load directly on the productivity shock \(z_{i,t}\). Productivity
shocks and financial shocks are separate primitives in the decomposition.

Technology adjustment is costly. Define

$$
d_{if,t}
=
\left\|
\alpha_{if,t}
-
\alpha_{if,t-1}
\right\|_2,
$$

and let the adjustment cost be

$$
\kappa d_{if,t}^2.
$$

The dynamic firm problem then trades off the benefit of adapting input shares to current
financial and productivity conditions against the cost of changing production
technology. This friction creates persistent network responses to persistent financial
shocks.

## Quantitative Exercise

The quantitative model will study how productivity shocks and financial shocks affect
aggregate output and the structure of the production network. The network statistics
defined above are tracked period by period:

$$
\mathcal{N}^C_t
=
\sum_{i=1}^N \omega^Y_{i,t} \log \omega^Y_{i,t},
\qquad
\mathcal{N}^S_{i,t}
=
\sum_{j=1}^N \alpha_{i,j,t} \log \alpha_{i,j,t},
\qquad
\mathcal{N}^S_t
=
\sum_{i=1}^N \omega^Y_{i,t}\, \mathcal{N}^S_{i,t}.
$$

The main impulse-response exercises are:

1. An adverse productivity shock to a sector, modeled as a negative shock to
   \(\eta^z_{i,t}\), which lowers the persistent sectoral productivity component
   \(z_{i,t}\).
2. An adverse financial shock to a sector, modeled as a positive shock to
   \(\eta^s_{i,t}\), which raises the sectoral intermediation wedge \(s_{i,t}\) and
   therefore raises the gross borrowing rate \(R_{i,t}\).
3. A monetary tightening, modeled as a rise in the safe rate \(R^f_t\) with sectoral
   spreads \(s_{i,t}\) held fixed, which raises \(R_{i,t}\) in every sector at once.

For each shock, the quantitative exercise will trace impulse responses of:

1. Aggregate output.
2. Network concentration \(\mathcal{N}^C_t\).
3. Sectoral sparsity \(\mathcal{N}^S_{i,t}\) and network sparsity \(\mathcal{N}^S_t\).
4. Sectoral technology choices \(\alpha_{i,j,t}\).
5. Sectoral prices, borrowing, and financial spreads.

## Externality and Industrial Policy

The model creates a natural externality. Individual firms choose technologies based on
private expected profits, distorted sectoral prices, and sector-specific borrowing costs.
They internalize how input choices affect their own production costs, but they do not
internalize how their technology choices affect the fragility of the aggregate production
network.

In particular, private technology choices may generate excessive concentration around
central suppliers. Such concentration can be privately efficient in normal times because
central suppliers may be productive or cheap. But it can make the whole network
vulnerable if the central sector is hit by an adverse productivity shock or a worsening of
financial conditions. The planner therefore faces a tradeoff between static production
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

The answer depends on the interaction between financial distortions, technology choice,
and network centrality. This interaction is precisely what the model is designed to make
transparent.
