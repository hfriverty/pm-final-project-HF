# AI Synthesis, Product Health & Insights Summary (Module 2)

## Responses
- **Assumption to validate #1:** The Data Quality of the Notes is not good enough
- **Assumption to validate #2:** The Questions are too broad and not fitting
- **Assumption to validate #3:** The Data package is too small
- **Moment of misery / red flag #1 (e.g., “user gave up after 3 tries”):** The income question stops people cold (N-01, N-06)

Moment: The consumer reaches the affordability questions, doesn’t know if “income” means this month or a normal month, and closes the portal. N-06 is afraid of typing the wrong number because it might be used against them.
Why it’s a red flag: The person leaves with intent to return, and the product gives them no reason to feel safe answering.
Data signal: Variable or shift-work earners agree to a plan at 41.6% versus 48.1% for fixed salary, and miss payments more often (22.5% vs 17.4%). “Why income is asked” is also 16.2% of agent contacts.
- **Moment of misery / red flag #2:** The “obvious” plan is the wrong one, and nobody warns them (N-02, N-05)

Moment: The consumer picks the shortest plan because it looks like the right answer, the amount is too high, and they miss the second payment. N-05 got a quick “yes” from the chat but still didn’t know what a late payment would mean.
Why it’s a red flag: The product let the consumer agree without understanding the consequences, so the failure shows up weeks later.
Data signal: “What if I miss a payment” is the top agent-contact reason (18.6%). Missed payments within 60 days rose from 15.6% to 18.4% when the 6-month plan became the first option in Month 4, and chat users miss at 21.6%. The Month 4 change is timing-correlated, not proven causal.
- **Moment of misery / red flag #3:** Multiple claims are handled one at a time (N-03)

Moment: The consumer can see only one claim and doesn’t know whether paying it stops the letters about the other.
Why it’s a red flag: The person with the most debt gets the most fragmented experience and likely falls back on the phone.
Data signal: Agreement rate drops from 52.1% (1 claim) to 37.7% (2) to 27.6% (3+), and “can claims be combined” is 17.3% of agent contacts. Ticket T-202 confirms there is no way to set up one plan for two claims.
- **Product Health & Insights Summary (Claude's output):** # Product Health & Insights Summary
*BU Collection, digital instalment journey (German portal). Sources: 12 interview notes and the 8 tickets from the data pack. All figures are fictional sample data.*

## Executive Summary
The portal is stable at the headline level: about 46% of started journeys end in an agreement, and that rate has risen over six months. That stability hides experience failures. The main problems are not outages but ambiguity around income, plan consequences and multi-claim handling, and the quality of agreements is declining, with missed payments within 60 days rising from 15.2% to 19.0%. The product converts more people into plans that fewer of them can sustain, while about 31% of starters still contact an agent for answers the portal does not give.

## Thematic Synthesis

### 1. Technical Stability
Core flows work for most users, and the defects are concentrated in specific hand-offs rather than systemic failure. The most consequential is document upload on mobile, which matters because mobile carries about 79% of journey starters. These defects also compound the experience problems below, since a user who hits a timeout is already likely to be uncertain about the income step.

- **Income document upload times out on mobile for large photos (T-201):** 853 journeys in the sample month requested a document that never arrived. **High**
- **Payment reminder sometimes arrives after the due date (T-207):** Directly affects the first instalment, though the sample gives no volume. **Medium**

### 2. Onboarding & Journey UX
Friction is concentrated at the affordability and plan-selection steps, where consumers must make a financial decision with little guidance. Users with variable income and users with several open claims fare worst, so the journey works best for the simplest case (one claim, fixed salary) and degrades as complexity rises.

- **Plan default steers users to an unsustainable choice (N-02):** Users choose the shortest plan as the "right" answer, and the monthly amount is too high. Missed payments rose from 15.6% to 18.4% when the 6-month plan became the first option (timing-correlated, not proven causal). **Critical**
- **"Income" is undefined (N-01):** Users do not know whether it means this month or a normal month, and they abandon the journey. Variable and shift earners agree to a plan at 41.6% versus 48.1% for fixed salary, and miss payments more often (22.5% vs 17.4%). **High**
- **No way to resolve multiple claims in one plan (N-03, T-202):** Users cannot see their combined position or know whether paying one claim stops letters on another. Agreement rates fall from 52.1% (one claim) to 37.7% (two) and 27.6% (three or more). **High**
- **Desktop-versus-mobile gap:** Mobile agrees to plans at 43.8% versus 54.0% on desktop, consistent with the upload issue and with a flow that is harder to complete on small screens. **Medium**

### 3. Trust & Clarity
The consumer-facing theme is a lack of reassurance. Users do not know what information is used for, whether the numbers are right, or what happens if something goes wrong. Hesitation is rational: users defer or switch to a human when the portal cannot answer questions that carry financial consequences.

- **Online amount differs from the letter (N-07, T-203):** 531 journeys were affected, 343 of them purchased-portfolio cases. Users refuse to commit until someone explains the gap. **High**
- **Fear of misreporting income, with no explanation of use or retention (N-06, T-206):** Users on tight finances worry the data will be used against them. "Why income is asked" accounts for 16.2% of agent contacts. **High**
- **Chat confirms plans without showing the consequences of a missed payment (N-05, T-208):** Chat users agree more often (53.3% vs 44.4%) but miss payments more often (21.6% vs 18.3%). This is correlational and may reflect self-selection. **High**
- **Preference for a human to confirm cost (N-04):** Some users do not trust the portal to tell them whether a plan will cost more. **Medium**

### 4. Support Load & Agent Enablement
Agent contacts are largely the portal's unanswered questions arriving by phone. Agents work without context, so they re-ask what the consumer has already entered and cannot explain why a plan was offered. This raises handling effort (roughly 11 to 13 minutes per contact) and undermines the self-service premise.

- **Agents cannot see consumer inputs or the rationale for a plan (N-08, N-09, T-205):** Calls begin with repeated questions, and failed plans are opaque to the people who must manage them. **High**
- **Contact drivers mirror portal gaps:** The top reasons are missed-payment consequences (18.6%), combining claims (17.3%), why income is asked (16.2%) and lower monthly amounts (14.7%). **High**
- **Self-service ceiling:** Only about 35% of starters resolve a plan without agent contact within 7 days, below the 46% who reach an agreement. **Medium**

### 5. Governance & Portfolio Constraints
These issues come from stakeholders outside the consumer journey. They matter because they limit what the product can safely do and how its outcomes are judged.

- **Explainability requirement (N-12):** Any plan recommendation must be defensible to both consumer and agent, and the current product cannot show how a decision was made. **High**
- **Client-facing impact of broken plans (N-10):** Spikes in failed plans appear in client reporting, so complaints weigh alongside recovery. **High**
- **Inconsistent data across acquired portfolios (N-11):** Some portfolios lack reliable contact or address history, which limits any logic that depends on consistent inputs. **Medium**

### Minor Technical Debt
Back-button navigation on the plan review screen clears affordability answers (T-204), and other edge-case defects have no volume attached in the sample. **Low**

## Evidence Notes
- The consumer view rests on 7 interviews, so the interview-derived themes are hypotheses. The quantitative signals come from about 8,360 journey starters in the sample month.
- Segment comparisons and the Month 4 change show association, not causation.
- **Did the AI catch the specific moment of misery / pain point you found in Step 1?:** yes, but much more structured through the prompt structure for the output
- **Did it smooth over a critical frustration into a generic bullet point?:** yes, in a few instances it made it feel AI-generic
- **Did the AI try to suggest features or a roadmap despite the constraints?:** no
- **Logic leak / hallucination #1 (e.g., “AI suggested a new search bar feature, roadmap leak”):** the Executive Summary says the portal is “stable at the headline level,” and the evidence doesn’t support it.
- **Logic leak / hallucination #2:** Smaller leaks I’d put next in line:

N-02 is one consumer, but the bullet says “users choose the shortest plan” and rates it Critical. The Month 4 timing supports it, but the generalization comes from one quote.
“Consistent with the upload issue” for the mobile versus desktop gap is a plausible link that I haven’t tested.
