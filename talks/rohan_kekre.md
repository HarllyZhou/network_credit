# Meeting Plan: Rohan Kekre

Use this meeting to get advice on the **finance block** of the project. Kekre's work is
closest to the macro-finance side: monetary transmission through financial markets,
risk premia, segmentation, and how asset prices discipline macro mechanisms. The goal
is to ask whether the credit constraint in the proposal should be treated as a
reduced-form borrowing capacity, an external finance premium, an intermediary
risk-bearing constraint, or something tied to asset prices and risk premia.

## 30-Minute Agenda

1. **0-3 minutes: short pitch.**
2. **3-8 minutes: explain the finance friction and where you are unsure.**
3. **8-18 minutes: ask how to model and discipline `\phi_i`.**
4. **18-25 minutes: ask about policy instruments.**
5. **25-30 minutes: ask for the cleanest next version of the model.**

## 1. Start With a 2-Minute Pitch

Say:

> I am building a production-network model where firms choose their input shares or
> technologies before productivity is realized. To operate, firms must finance labor and
> intermediate-input purchases in advance. The reduced-form constraint is
> \(B_i \leq \phi_i E[P_iQ_i]\), where \(\phi_i\) captures sectoral credit conditions.
> A credit shock changes not only sector \(i\)'s scale, but also its technology choice and
> supplier dependence. I want to understand which financial variables should discipline
> \(\phi_i\), and whether private technology reallocation after credit shocks creates a
> network externality that policy should correct.

Then give the mechanism:

$$
\phi_i \downarrow
\quad\Rightarrow\quad
\text{borrowing capacity tightens}
\quad\Rightarrow\quad
\alpha_{ij}\ \text{changes}
\quad\Rightarrow\quad
\text{network concentration / sparsity changes}
\quad\Rightarrow\quad
\text{aggregate fragility}.
$$

Keep the pitch concrete. Do not start with all details of the household side.

## 2. Why His Research Is Relevant

Frame the connection like this:

> Your work on monetary policy, redistribution, and risk premia makes me think the
> finance side should not just be a reduced-form borrowing limit. The credit condition
> may be tied to risk premia, asset values, or the identity of the marginal risk bearer.
> I want your advice on how structural the finance block needs to be.

The useful connection is not production networks per se. It is:

$$
\text{monetary/financial shock}
\Rightarrow
\text{risk premia or debt capacity}
\Rightarrow
\text{real allocation}.
$$

Your model adds:

$$
\text{real allocation}
\Rightarrow
\text{endogenous network structure}.
$$

So the meeting should focus on how to map financial-market objects into the network
constraint.

## 3. Main Question: What Is `\phi_i`?

Ask this early:

> In my current draft, \(\phi_i\) is a reduced-form sectoral credit condition. If I want the
> finance side to be credible, should \(\phi_i\) be interpreted as a borrowing-capacity
> parameter, an external finance premium, an intermediary risk-bearing constraint, or a
> reduced-form object backed out from asset prices and spreads?

Then give him the options:

### Option A: Borrowing Capacity

$$
B_i \leq \phi_i E[P_iQ_i].
$$

Interpretation: \(\phi_i\) is pledgeability or collateral capacity. This is tractable and
close to working-capital constraints.

Ask:

> Is this too reduced-form, or is it acceptable if I map \(\phi_i\) to leverage, loan
> quantities, collateral values, or sectoral credit spreads?

### Option B: External Finance Premium

Instead of a hard borrowing limit, firms pay an interest rate

$$
R_i = R + \chi_i,
$$

where \(\chi_i\) is a sectoral external finance premium.

Ask:

> Would a price wedge be more natural than a quantity constraint? If the model is about
> technology choice, is it more useful to make financing expensive at the margin rather
> than impose a hard cap?

### Option C: Risk-Premia / SDF Channel

The firm maximizes

$$
E[\Lambda \Pi_i],
$$

so financial conditions can enter through the stochastic discount factor \(\Lambda\), not
only through \(B_i \leq \bar B_i\).

Ask:

> Should the financial channel operate through the firm's borrowing constraint, or
> through the SDF that prices repayment risk? In other words, should bad states matter
> because firms cannot borrow, or because the claims they issue become expensive?

My instinct: keep the benchmark with the borrowing-capacity constraint, but ask him
whether the paper needs a pricing equation that links \(\phi_i\) to spreads or risk premia.

## 4. How to Discipline the Finance Variables

Ask him:

> Which empirical financial variables would make the model believable?

Possible answers to propose:

1. **Leverage:** sectoral debt-to-assets or debt-to-sales.
2. **Credit spreads:** sectoral borrowing cost relative to safe rates.
3. **Debt capacity:** committed credit lines, loan quantities, or working-capital loans.
4. **Collateral values:** receivables, inventory, tangible assets, or expected sales.
5. **Default risk:** distance to default or expected default frequency.
6. **Risk premia:** excess returns or bond spreads if the model prices risky claims.

Follow-up:

> If I only have one financial state variable in the model, which one would you pick:
> leverage, spread, collateral value, or risk premium?

This is probably the most valuable question for him.

## 5. Policy Question

Say:

> The policy part of the project is that firms privately choose technologies, but do not
> internalize how their supplier choices change aggregate network fragility. If credit
> shocks cause overconcentration around certain suppliers, should policy be modeled as
> sectoral taxes/subsidies, credit policy, macroprudential policy, or monetary policy?

Then ask:

> From a macro-finance perspective, is it strange to use sectoral taxes/subsidies to
> correct a financial-friction externality? Would it be cleaner to use a credit instrument,
> such as sectoral borrowing taxes, loan-to-value limits, or credit subsidies?

Possible direction:

$$
\text{private firm problem}
\neq
\text{planner problem}
$$

because firms do not price:

$$
\frac{\partial \text{aggregate fragility}}{\partial \alpha_{ij}}.
$$

The key issue is what instrument naturally targets that wedge.

## 6. What I Would Literally Ask Him

Write these down and ask them in order.

1. **Finance object:**
   “Should \(\phi_i\) be modeled as borrowing capacity, an external finance premium, or
   a risk-premia/SDF object?”

2. **Empirical discipline:**
   “If I want to take the model to data, which variable should discipline sectoral credit
   conditions: leverage, spreads, loan quantities, collateral values, or risk premia?”

3. **Timing:**
   “Does it make sense that firms choose technology and planned borrowing before
   productivity is realized, while financing happens only if repayment is feasible after
   the shock?”

4. **Policy instrument:**
   “If the externality is network fragility caused by technology reallocation, should the
   corrective policy be an industrial-policy tax/subsidy, a credit policy, or a monetary
   policy rule?”

5. **Minimum viable model:**
   “For a first version, would you keep \(\phi_i\) exogenous and focus on technology
   choice, or endogenize \(\phi_i\) through collateral values or risk premia?”

## 7. Desired Takeaway

By the end of the meeting, try to get one clear answer to this:

> What is the cleanest financial friction for the first version of the paper?

The best possible outcome is a recommendation like:

> Start with a borrowing-capacity constraint, discipline \(\phi_i\) using sectoral leverage
> or spreads, and leave a full risk-premia/SDF channel for a later extension.

or:

> Replace the hard constraint with an external finance premium, because technology
> choice should respond smoothly to financing costs.

Either answer would sharply improve the model.
