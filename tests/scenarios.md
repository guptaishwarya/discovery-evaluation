# V1 Manual Test Scenarios

Use these to test the skill in an LLM environment.

For each scenario, evaluate:
1. Did it detect the right discovery risk?
2. Did it choose the right mechanism?
3. Did it ask the right question?
4. Did it preserve state?
5. Did it know when not to intervene?

---

## 1. Solution gravity

Builder:
"I want to build an AI app that automatically creates personalized travel itineraries."

Expected:
Problem vs Solution.

It should not immediately design itinerary features.

---

## 2. Clear problem

Builder:
"Travelers spend hours comparing destinations because they don't know which ones fit their interests and available time."

Expected:
No unnecessary intervention. The problem is reasonably clear.

---

## 3. AI escalation

Builder:
"Recommendation is useful, but maybe we should use prediction to predict which destination they'll enjoy most."

Expected:
Two-Journey.

The skill should question whether prediction addresses a different or more important friction.

---

## 4. Unsupported assumption

Builder:
"Parents will definitely trust an AI recommendation for their children."

Expected:
Assumption Challenge.

---

## 5. State preservation

Conversation:
Builder: "Travelers struggle to choose which destination fit their trip."
Skill: establishes problem.
Builder: "Let's personalize recommendations based on travel style."

Expected:
Two-Journey, without asking the builder to redefine the problem.

---

## 6. Evidence changes direction

Conversation:
Builder: "Travelers don't want to spend time planning."
Later:
"In interviews, travelers actually said their biggest concern was making the wrong choice."

Expected:
Update the relevant assumption/problem understanding rather than restarting discovery.

---

## 7. Agent temptation

Builder:
"Could we make an agent that searches destination, compares them, books everything, and keeps monitoring the trip?"

Expected:
Two-Journey.

The skill should decompose the proposed value rather than treat "agent" as automatically better.

---

## 8. Already sufficient

Builder:
"The problem is clear, we have evidence from interviews, and we've decided the smallest solution is a recommendation with reasoning."

Expected:
Stop discovery and move toward execution.

---

## 9. Low-impact assumption

Builder:
"We haven't decided whether the button should say 'Get recommendation' or 'Find my match.'"

Expected:
No Assumption Challenge. This does not materially affect discovery.

---

## 10. New evidence invalidates assumption

Builder:
"We assumed users would want automatic recommendations. But our test showed most users prefer choosing the criteria themselves."

Expected:
Challenge/update the solution direction. Do not keep optimizing automatic recommendation as if the assumption still holds.
