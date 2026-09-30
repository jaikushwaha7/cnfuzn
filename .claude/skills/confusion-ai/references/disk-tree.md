# Disk-tree sizing

Goal: see how big a confusion is and where its weight sits, the way a disk-usage tool shows what fills a drive.

## Build

1. **Root** = the confusion in one phrase.
2. **Branches** = sub-problems. Seed by root question:
   - What is true? → Facts I'm missing · Sources I can't judge · What's at stake if I'm wrong
   - What do I want? → What I feel · What others expect of me · What I practically need
   - What should I do? → Things I don't know yet · Constraints (time, money, people) · Values in conflict
   - Who am I? → What I inherited · What I chose · Pressures around me
   - Where am I going? → Skills I'd need · Resources I'd need · Unknown unknowns
   - Add one extra branch per identity layer in play (Gender, Race / ethnicity, Caste, Religion / belief, Nationality, Class, Family expectations).
3. **Leaves** = specific pieces under each branch. Ask: "What exactly is hard about this branch?"
4. **Weight** each leaf 1 (tiny) to 10 (huge): how much of the confusion it carries.
5. **Kind** each leaf:
   - **Find out**: a fact to look up or ask
   - **Decide**: a choice to make
   - **Feel**: something to process emotionally
   - **Wait**: needs time or a future event

## Compute

- Branch size = sum of its leaves. Root size = sum of branches. Percent = size / root size.
- Size label by root size: Small < 15 · Medium < 35 · Large < 70 · Huge ≥ 70.
- **Big rocks**: sort leaves by weight, take leaves until they cover ≥ 60% of the total.
- **Actionable share** = (Find out + Decide weight) / total.
- **Biggest actionable rock** = heaviest leaf of kind Find out or Decide. The next step starts here.

## Render

```
▾ 100%  My family expects a tradition I doubt            42
  ▾  55%  What I inherited                               23
    └  31%  Whether I believe it                         13 ★ find out
    └  24%  What my parents would feel                   10   feel
  ▾  45%  What I chose                                   19
    └  29%  Which practices still mean something         12 ★ decide
    └  17%  How to tell my family                         7   decide
```

Then one sentence: "Small/Medium/Large/Huge problem. ★ N of M pieces carry 60%. X% is actionable now; the rest needs feeling or time."

## Reading the result

- Mostly **Feel/Wait**: don't force a decision. Do a small reversible step and schedule a review.
- Mostly **Find out**: the confusion is a knowledge gap. Use the evidence ledger.
- Mostly **Decide**: use the ability-to-act lenses.
- One huge leaf: name it plainly and start there.
- Many tiny leaves: the problem is smaller than it feels; pick three and move.
