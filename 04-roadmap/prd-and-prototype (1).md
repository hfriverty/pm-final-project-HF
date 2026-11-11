# PRD & Prototype Sprint (Module 4)

## Pick & scope with MoSCoW
- **The “Now” feature I’m scoping (name + one-line core description):** B2Plain explainer for why income is asked and how it is used
- **My finalized Must-Haves (after overriding the AI):** ID	Requirement	Pass or fail	Blocked by, and the fallback
M1	The income question names one period and one basis, and the label matches what the system stores. It states the rule for changing income in one sentence. The same term is used wherever income appears in the journey, including the document request and plan review.	The label contains the period and basis. A text audit finds no contradicting wording.	Policy decision on period and rule. If undecided by day 2: keep the current question, ship nothing, and say so. A guessed period is worse than the old ambiguity.
M2	One block, three true facts: why income is asked, what it’s used for, and who sees it. It makes no promise that compliance hasn’t approved (“won’t affect your claim”, a retention figure).	Compliance approves each sentence. About 50 words in total, in German and second person.	Compliance and data protection. If not approved by day 7: ship M1 alone and record that “fear of misuse” is unaddressed.
M3	M1 and M2 are visible on the question screen without a tap: no modal, tooltip or link needed.	At 390 px width, the label, statement and field are all readable on one screen.	UX and design-syste
- **What I demoted from Must → Should/Won’t, and why:** various topics

## Generate your Simplified PRD
- **One thing my PRD makes explicit that a vague brief would have missed:** Structure and clear descriptions

## Prompt-to-prototype sprint
- **Where did the prototype reveal a gap in my PRD logic? (what I had to update):** _(not filled in)_
- **My prototype: save Claude's HTML as prototype.html in 04-roadmap/, open it in your browser, and add a screenshot:** https://claude.ai/artifact/Ddz2P5awLn5GtTFsHbPUHo?sk=jDl14DXXAK8CP7Velaniig#release
