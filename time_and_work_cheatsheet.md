# Time & Work - Exam Patterns, Concepts & Tricks
## For: TCS NQT & Placement Aptitude Rounds

---

## HOW THIS DIFFERS FROM TIME-SPEED-DISTANCE
- In TSD: Speed x Time = Distance
- In T&W: Efficiency x Time = Work
- Work is always treated as 1 unit (the full job) unless stated otherwise
- Efficiency = 1 / Days_to_complete (fraction of work done per day)
- More workers → less time (inverse); More efficiency → less time (inverse)

---

## CORE TERMINOLOGY

| Term | Meaning |
|---|---|
| Efficiency | Fraction of work done per day = 1/n (if person takes n days alone) |
| Combined Efficiency | Sum of individual efficiencies when working together |
| LCM Method | Assign total work = LCM of all given days; find per-day work as integers |
| Negative Work | Work done against the process (e.g. a pipe that drains, a person who destroys) |
| Man-Days | Total work unit = Number of men x Number of days |

---

## CORE FORMULA BANK

| Need to find | Formula |
|---|---|
| Days taken alone | 1 / Efficiency |
| Combined time (A and B together) | AB / (A+B) [where A,B = individual days] |
| Combined time (A, B, C together) | ABC / (AB+BC+CA) |
| Work done in t days by A | t / A [where A = days A takes alone] |
| Remaining work | 1 - Work already done |
| Men x Days = constant | M1 x D1 = M2 x D2 (for same work) |
| Men x Days x Hours = constant | M1 x D1 x H1 = M2 x D2 x H2 |
| Efficiency ratio | Inverse of time ratio: if A:B days = m:n, efficiency ratio = n:m |

---

## LCM METHOD (Fastest Technique — Use This Always)

Instead of fractions, assign Total Work = LCM of all days given.
Then each person's per-day work = Total Work / Their days.

Example: A takes 12 days, B takes 15 days.
- LCM(12,15) = 60 → Total Work = 60 units
- A does 60/12 = 5 units/day
- B does 60/15 = 4 units/day
- Together: 5+4 = 9 units/day
- Time together = 60/9 = 6.67 days

This avoids all fraction arithmetic. Use LCM method for every T&W problem.

---

## EXAM PATTERNS (Most Frequent to Least Frequent)

### Pattern 1 - Two/Three People Working Together [MOST FREQUENT]
Given individual times, find combined time.
- Formula: Combined = AB/(A+B) for two people
- LCM method preferred for 3+ people
- A = 20 days, B = 30 days → Combined = 20x30/50 = 12 days

### Pattern 2 - One Person Leaves Midway [VERY FREQUENT]
A and B work together for some days, then one leaves, other finishes.
Approach:
1. Assign total work via LCM
2. Calculate work done together in first phase
3. Remaining work done by one person alone
4. Total time = first phase + remaining/individual rate

Example: A=12d, B=15d, work together 3 days then B leaves.
- LCM=60, A=5/day, B=4/day
- Together 3 days: 3x9=27 units done
- Remaining: 60-27=33 units, A does alone: 33/5=6.6 days
- Total = 3+6.6 = 9.6 days

### Pattern 3 - Work for Specific Days Then Together [FREQUENT]
A works alone for d days, then B joins. Find total time to finish.
Approach: Work done by A alone first → remaining → both together.

### Pattern 4 - Pipes and Cisterns [VERY FREQUENT]
Same as T&W but with pipes filling/emptying a tank.
- Filling pipe → positive work (+)
- Emptying/leak pipe → negative work (-)
- Tank = 1 unit of work (or use LCM of all pipe times)
- Net rate = Sum of filling rates - Sum of emptying rates
- Time to fill = Total capacity / Net rate

Example: Pipe A fills in 6 hrs, Pipe B empties in 10 hrs, both open:
- LCM=30, A=+5 units/hr, B=-3 units/hr
- Net = 2 units/hr → Time = 30/2 = 15 hrs

### Pattern 5 - Efficiency Ratio / Wage Distribution [FREQUENT]
When workers are paid in proportion to work done:
- Work ratio = Efficiency ratio = Inverse of time ratio
- A takes 10d, B takes 15d → Efficiency ratio = 3:2 → Wage ratio = 3:2
- Total wages x (3/5) goes to A, x (2/5) goes to B

### Pattern 6 - Men-Days Scaling [FREQUENT]
More men, fewer days for same work.
- M1 x D1 = M2 x D2
- Extension: M1 x D1 x H1 = M2 x D2 x H2 (hours per day also changes)
- Example: 10 men finish in 12 days. How many men to finish in 8 days?
  10x12 = Mx8 → M = 15 men

### Pattern 7 - Work Done by A Alone After B Leaves [FREQUENT]
A and B together can do in X days. A alone takes Y days. How long does B take alone?
- B alone = XY/(Y-X)
- Using LCM: Total=LCM(X,Y), A=Total/Y per day, Together=Total/X per day
  B per day = Together rate - A rate → B alone = Total/B rate

### Pattern 8 - Alternate Day Working [FREQUENT]
A and B work on alternate days (A on day 1, B on day 2, A on day 3...).
Approach:
1. LCM method: assign total work
2. Work done in every 2-day cycle = A's rate + B's rate
3. Find how many complete cycles fit, then handle remainder manually

### Pattern 9 - A is Twice/Thrice as Efficient as B [FREQUENT]
"A is twice as efficient as B" → A takes half the time B takes.
- If B takes 20 days → A takes 10 days
- Efficiency ratio A:B = 2:1
- Never confuse: "twice as efficient" ≠ "takes twice as long"

### Pattern 10 - Work and Wages Combined [MODERATE]
Workers hired for a job at daily rates. Some leave midway.
- Calculate exact days each worker works
- Wages = Daily rate x Days worked (not split equally unless efficiency equal)

---

## SPEED TRICKS

### Trick 1 - Always Use LCM Method
Never work with fractions. LCM of all days = Total Work. Per-day work = integer.
Saves 60% of calculation time vs fraction method.

### Trick 2 - Two-Person Combined Formula Shortcut
A and B together = AB/(A+B)
Memorize common results:
- 10 and 10 → 5 days
- 10 and 15 → 6 days
- 12 and 15 → 6.67 days
- 15 and 20 → 8.57 days
- 20 and 30 → 12 days

### Trick 3 - Efficiency is Inverse of Time
- A:B days = 3:4 → A:B efficiency = 4:3
- Always flip the ratio when converting days to efficiency or wages

### Trick 4 - Pipes: Identify Sign First
Before any calculation, list all pipes with + or - sign:
- Inlet = + | Outlet/Leak = -
Net rate = algebraic sum. If net is negative, tank never fills — flag it immediately.

### Trick 5 - Alternate Day Pattern Shortcut
Work done in 2 days (A+B cycle) = A_rate + B_rate
Number of complete cycles = Total Work / (A_rate + B_rate)  [take floor]
Remaining work after complete cycles → check who works on that day and compute.

### Trick 6 - A is n Times as Efficient → Days = 1/n Times
- Twice as efficient → half the days
- Thrice as efficient → one-third the days
- Half as efficient → double the days

### Trick 7 - Men-Days Inverse Proportionality
Work is constant → Men and Days are inversely proportional.
If men increase by factor k → days decrease by factor k.
Quick check: M1xD1 must equal M2xD2 before and after.

---

## COMMON TRAPS IN EXAMS

1. "A is twice as efficient as B" → A takes HALF the days, NOT twice (students reverse this)
2. Pipes: forgetting to make outlet pipe NEGATIVE → gets addition instead of subtraction
3. Alternate days: assuming both work every day instead of checking who works on final day
4. Wages split equally when workers have different efficiencies → wages must be in efficiency ratio
5. "Together they finish in X days" and "A alone takes Y days" → B alone = XY/(Y-X), NOT Y-X
6. Man-days: adding more men to an already finished fraction of work → recalculate only remaining work
7. "A can do a work in 10 days" means WHOLE work in 10 days, not per day
8. Fraction of work done ≠ Fraction of time taken when efficiencies differ
9. If one pipe fills and another empties at same rate → tank never fills (net = 0)
10. Work left after someone leaves: always subtract work DONE, not time elapsed

---

## EFFICIENCY - DAYS QUICK REFERENCE TABLE

| Days to complete | Efficiency (work/day) | % per day |
|---|---|---|
| 2 days | 1/2 | 50% |
| 3 days | 1/3 | 33.33% |
| 4 days | 1/4 | 25% |
| 5 days | 1/5 | 20% |
| 6 days | 1/6 | 16.67% |
| 8 days | 1/8 | 12.5% |
| 10 days | 1/10 | 10% |
| 12 days | 1/12 | 8.33% |
| 15 days | 1/15 | 6.67% |
| 20 days | 1/20 | 5% |
| 25 days | 1/25 | 4% |
| 30 days | 1/30 | 3.33% |

(These are same as percentage fraction table — one table serves both chapters)

---

## CONNECTION TO OTHER CHAPTERS
- Percentage chapter: Efficiency % per day = fraction-to-percentage table (same values)
- Ratio & Proportion: Efficiency ratio → wage ratio (direct); Time ratio → efficiency ratio (inverse)
- TSD chapter: Efficiency = Speed, Work = Distance, Time = Time (exact analogy — do NOT repeat concepts)

---

## SOLVED TRAPS FROM PRACTICE
(Will be updated as questions are solved in sessions)

---

## PRACTICE PROBLEM TYPES (TCS NQT Frequency)
1. A and B together — find combined days (2 or 3 people)
2. One person leaves midway — find total days to complete
3. Pipes and cisterns — find time to fill or empty with multiple pipes
4. Wages distribution based on work done
5. Men-days scaling — more/fewer men, find new days or men needed
6. Alternate day working — who works on which day
7. A is n times efficient as B — find individual or combined days
8. Work partially done, remaining workers change — find completion time
9. Leak/inlet combined — when does tank fill or when does it never fill
10. Three people, two work, one leaves, find time
