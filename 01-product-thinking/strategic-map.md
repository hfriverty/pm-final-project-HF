# Strategic Discovery Map (Module 1)

## Responses
- **Write one feature from the map that, if an engineer asked “why is this a priority for our 12-week roadmap?”, you honestly could not give a strategic answer for.:** Affordability first (B3). I bundled it with the income explainer on the map, and it’s the one I couldn’t defend if an engineer pushed.

The data shows a real problem near it. Variable or shift-income journeys miss payments at 22.5% against 17.4% for fixed salary, and Mara’s story is built on exactly that. But that only shows the problem exists. It doesn’t show that moving a check earlier fixes it, and I can’t point to any row, interview or ticket that does.

It also isn’t clear what B3 changes. The funnel shows affordability questions already come before income documents and plan review, and 88% of starters get through them. So “before the plan options” could mean reordering screens, using the answers to filter which plans are shown, or something else. Those are very different 12-week bets. If it means filtering plans, it runs into the guardrails: no adverse outcome from an opaque decision, explainability to the consumer and the agent, and proxy-discrimination risk. That needs compliance input before an engineer could even size it.

The strongest evidence for it is one interview (N-02), where someone picked the shortest plan, found it too high, and missed the second payment. That story is mostly about the plan screen defaulting to the shortest option, which is the B7 problem. It’s not clearly an affordability-check problem.

Compare B1, B2 or B5. Each has a number and a mechanism: multi-claim agreement is 28–38% against 52% for single claims, 16.2% of agent contacts ask why income is needed, and 853 journeys asked for a document that never arrived. B3 only has a hunch that sounds right.

I’d either split it into a specific, testable change, or hold it until someone can show that missed payments cluster in plans that exceeded what the consumer said they could afford. The value and effort scores are blank, so I haven’t scored it.
- **Write one feature that looks “correct” for the app but has zero strategic weight, you have no idea if it helps the company make money or whether a single user actually asked for it.:** Chat assistant on every portal page (B8), which is the "everywhere" half of the "Hold" leaf on the first map. It sounds like what a modern portal should have, so it passes the sniff test.

No consumer asked for it. N-05 liked how fast the chat was but still wasn't sure what happens after a late payment, and nobody said they wanted it on more screens. The tickets point the other way, since T-208 is a bug where chat confirms a plan without showing what a missed payment costs. Putting that behavior on every page would spread a known flaw.

I also can't tell whether it makes money. Chat users do look better: 53.3% agree to a plan against 44.4%, and 27.1% contact an agent against 31.9%. But people who choose to open a chat aren't comparable to people who don't, so I can't say chat caused any of that. Chat users also miss payments more often (21.6% against 18.3%), which is the opposite of responsible recovery. A wider rollout could raise SSR while hurting the outcomes SSR is supposed to stand for.

The only reason I'd have for building it is that it feels like a portal should have it. An engineer asking why it's on a 12-week roadmap would get nothing from me. I'd stop treating it as a feature and run a small test first: add it to one step, such as the plan review screen where people drop, with the missed-payment explanation fixed first. Then compare outcomes against a control group.
- **Compare V3 to your Step 1 baseline. What changed, and is the output objectively better, did the AI get smarter, or did your added PM knowledge (JTBD, effort/impact, retention) force it to be useful?:** V3 is better as a sprint-planning tool: it’s organized around decisions and flags five strategic tensions, which Step 1 didn’t.
The AI didn’t get smarter. It’s the same model and the same data. Your PM framing (JTBD, effort/impact, tensions) and your two earlier critiques made the output more useful.
- **Key takeaway: how does this prove the PM’s role is to think while the AI’s role is to execute?:** PM Role is getting more important in terms of judgement and thinking - rather delivery slop with AI
