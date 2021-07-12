---
layout: essay
type: essay
title: Paying Off Your Tech Debts
# All dates must be YYYY-MM-DD format!
date: 2021-07-06
labels:
  - Software Engineering
  - Learning
---

How do we measure tech debt and ensure that it is prioritized? It's a common occurance across the industry - maintenance of old code is pushed aside to make room for shiny new features. On my team, we've had to address tech debt left over after a redesign set a new standard for UI across the app. 

The answer was right in front of us, but we needed to reorient our thinking on it to be able to come up with a strategy. **At its core, paying off tech debt is about knowing the tenets of good financial responsibility**. You can get "cash advances" in the way of scrappy features, but the interest on it will eventually weigh you down. If the tech debt is too large, you may have to abandon (foreclose on) the project, and start again greenfield.

When our team was formed, we were tasked with only working on tech debt for 3 months. We did some research into how other companies are doing it, and left off looking at it like a loan repayment
```
IMPACT - The amount of effort it takes to live with this debt
FIX COST - The amount of effort it would take to pay off this debt
INTEREST - The speed at which this debt will grow if not paid off
```

We decided to create a template for tech debt, that looked something like this:

```
| IMPACT | FIX COST | INTEREST |
|--------|----------|----------| 
| Low	 | Low	    | Low      |

### Recommended payoff strategy:
  Annuity / Lump sum
### Description of Problem:
  TBD
### Recommended Fix:
  TBD
```

 We paid off debt with highest interest first, then paid off the debt with the highest impact, which required a lump sum payment. After that we were able to distribute some of that debt onto feature teams, particularly if it was an annuity.

This also makes a case against taking out new "tech loans", we don't want to be stuck making a high payment each cycle

Lots of credit to this [article by riot games](https://technology.riotgames.com/news/taxonomy-tech-debt), which helped us to frame the problem.