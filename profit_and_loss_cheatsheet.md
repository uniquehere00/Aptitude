# Profit & Loss - Exam Patterns, Concepts & Tricks
## For: TCS NQT & Placement Aptitude Rounds

---

## CORE TERMINOLOGY

| Term | Meaning |
|---|---|
| Cost Price (CP) | Price at which item is bought |
| Selling Price (SP) | Price at which item is sold |
| Marked Price (MP) | Price printed on item (before discount) |
| Discount | Reduction on MP — always calculated on MP |
| Profit | SP > CP → Profit = SP - CP |
| Loss | SP < CP → Loss = CP - SP |
| Profit % | (Profit / CP) x 100 |
| Loss % | (Loss / CP) x 100 |

WARNING: Profit% and Loss% are ALWAYS on CP, never on SP (unless question says so)

---

## CORE FORMULA BANK

| Need to find | Formula |
|---|---|
| Profit | SP - CP |
| Loss | CP - SP |
| Profit % | (SP - CP) / CP x 100 |
| Loss % | (CP - SP) / CP x 100 |
| SP when profit% known | SP = CP x (100 + P%) / 100 |
| SP when loss% known | SP = CP x (100 - L%) / 100 |
| CP when profit% and SP known | CP = SP x 100 / (100 + P%) |
| CP when loss% and SP known | CP = SP x 100 / (100 - L%) |
| Discount | MP - SP |
| Discount % | (Discount / MP) x 100 |
| SP after discount | SP = MP x (100 - D%) / 100 |
| MP when SP and discount% known | MP = SP x 100 / (100 - D%) |

---

## EXAM PATTERNS (Most Frequent to Least Frequent)

### Pattern 1 - Basic Profit / Loss Calculation
Find profit%, loss%, SP, or CP given two of the four values.
- CP = 400, SP = 500 → Profit = 100 → Profit% = (100/400)x100 = 25%
- CP = 600, Profit% = 20% → SP = 600x120/100 = 720

### Pattern 2 - Find CP or SP from % [VERY FREQUENT]
Most common single-step question.
- SP = 880, Profit% = 10% → CP = 880x100/110 = 800
- SP = 750, Loss% = 25% → CP = 750x100/75 = 1000

### Pattern 3 - Marked Price + Discount then Profit [VERY FREQUENT]
Two-step chain: MP → SP (after discount) → Profit% on CP.
- MP = 1000, Discount = 10%, CP = 800
  SP = 1000x90/100 = 900 → Profit = 100 → Profit% = 100/800x100 = 12.5%

### Pattern 4 - Successive Discounts then Profit [VERY FREQUENT]
Three-step: two discounts on MP → SP → compare with CP for profit/loss.
- MP = 2000, discounts 20% and 10%, CP = 1400
  After 20%: 1600 → After 10%: 1440 → Profit = 40 → Profit% = 40/1400x100 = 2.86%

### Pattern 5 - Dishonest Dealer / False Weight [VERY FREQUENT]
Dealer claims to sell at CP but uses a false weight.
- Formula: Profit% = (True weight - False weight) / False weight x 100
- Dealer uses 900g but sells as 1000g → Profit% = (1000-900)/900x100 = 11.11%

### Pattern 6 - Two Items Same SP, One Profit One Loss [CLASSIC TRAP]
Sell two items at same SP, one at x% profit, one at x% loss.
- Net result is ALWAYS a loss — never break-even
- Loss% = x^2 / 100
- Example: both at 20% → Net loss% = 400/100 = 4%

### Pattern 7 - CP of Two Items Same, Different SP Profit/Loss
- CP each = 500, one sold at 10% profit, one at 10% loss
  SP1 = 550, SP2 = 450 → Total SP = Total CP → No profit no loss
  (When CP is same and profit% = loss%, net = 0)
  Contrast with Pattern 6: there SP is same, here CP is same — opposite results

### Pattern 8 - Profit on CP vs Profit on SP
Some questions give profit% on SP instead of CP. Always convert first.
- If profit is r% of SP → Profit% on CP = r/(100-r) x 100
- Example: 20% profit on SP → on CP = 20/80x100 = 25%

### Pattern 9 - Shopkeeper Marks Up then Gives Discount
MP increased by x% above CP, then discount of y% given on MP.
- Net multiplier = (1 + x/100)(1 - y/100)
- If net multiplier > 1 → profit; if < 1 → loss
- Example: MP marked 40% above CP, discount 25%
  Net = 1.4 x 0.75 = 1.05 → 5% profit

---

## SPEED TRICKS

### Trick 1 - Multiplier Method (Fastest for all questions)
Use a single multiplier instead of formula steps:
- 20% profit → SP = CP x 1.2 | Reverse: CP = SP / 1.2
- 25% loss  → SP = CP x 0.75 | Reverse: CP = SP / 0.75
- SP = 840, 20% profit → CP = 840/1.2 = 700

### Trick 2 - Same SP Two Articles (Most Frequent Trap)
- Sold at x% profit and x% loss at same SP → ALWAYS net LOSS
- Net Loss% = x^2 / 100
- x=10 → 1% loss | x=20 → 4% loss | x=25 → 6.25% loss | x=30 → 9% loss

### Trick 3 - False Weight Profit Shortcut
- Profit% = (True - False) / False x 100
- Alt: Profit% = Error / (True weight - Error) x 100
- Uses 800g, sells as 1kg → Profit% = 200/800x100 = 25%

### Trick 4 - Profit% on SP to Profit% on CP Conversion
- Profit% on CP = (Profit% on SP) / (100 - Profit% on SP) x 100
- 20% on SP → 20/80x100 = 25% on CP
- 25% on SP → 25/75x100 = 33.33% on CP

### Trick 5 - CP Finding Shortcut (Memorize These)
Profit% → divide SP by this multiplier:
- 10% → 1.1 | 20% → 1.2 | 25% → 1.25 | 33.33% → 1.333 | 50% → 1.5

Loss% → divide SP by this multiplier:
- 10% → 0.9 | 20% → 0.8 | 25% → 0.75 | 33.33% → 0.667 | 50% → 0.5

### Trick 6 - MP → SP → Profit Chain Rule
Always move in this direction only:
MP → (apply discount%) → SP → (compare with CP) → Profit%
Never reverse or skip steps in this chain.

### Trick 7 - Successive Discounts on MP
Net discount = a + b - ab/100 (both a and b positive for discounts)
SP = MP x (1 - a/100) x (1 - b/100)
Connects directly to Percentage chapter Trick 7.

### Trick 8 - Mark Up % to ensure profit after discount
If shopkeeper wants p% profit after giving d% discount:
MP = CP x (100 + p%) / (100 - d%)
Example: wants 20% profit after 20% discount → MP = CP x 120/80 = 1.5 x CP → mark 50% above CP

---

## COMMON TRAPS IN EXAMS

1. Profit% and Loss% are on CP — never on SP unless explicitly stated
2. Discount% is on MP — never on CP or SP
3. Two articles same SP, one profit one loss → ALWAYS net loss (x^2/100), never 0
4. Two articles same CP, one profit one loss at same % → net = 0 (opposite of above)
5. "Gains 20% on SP" is NOT same as "20% profit" — must convert via Trick 4
6. "Sold at 1/3rd profit" = 33.33% profit, NOT 33%
7. False weight: dealer uses 800g labelled as 1kg → profit base is 800g not 1000g
8. Markup then discount → never assume profit; always calculate net multiplier
9. "Cost price includes overhead/transport" → add overhead to CP before profit%
10. MP is NOT always higher than CP — question may give weird combos; always check

---

## CP:SP RATIO → INSTANT PROFIT/LOSS TABLE

| CP : SP | Result |
|---|---|
| 4 : 5 | 25% profit |
| 5 : 4 | 20% loss |
| 2 : 3 | 50% profit |
| 3 : 2 | 33.33% loss |
| 5 : 6 | 20% profit |
| 6 : 5 | 16.67% loss |
| 3 : 4 | 33.33% profit |
| 4 : 3 | 25% loss |
| 9 : 11 | 22.22% profit |
| 11 : 9 | 18.18% loss |

---

## CONNECTION TO PERCENTAGE CHAPTER
- Successive discounts on MP = successive % decrease (same formula)
- Markup then discount = successive % change (one +, one -)
- Net multiplier concept is identical in both chapters
- Always use: Net = (1 +/- a/100)(1 +/- b/100)

---

## SOLVED TRAPS FROM PRACTICE
(Will be updated as questions are solved in sessions)

---

## PRACTICE PROBLEM TYPES (TCS NQT Frequency)
1. Find CP or SP from given profit/loss% — basic reversal
2. MP + single discount → find profit% on CP
3. MP + two successive discounts → find SP or profit%
4. Two articles same SP, one profit one loss → find net loss%
5. False weight / dishonest dealer → find profit%
6. Profit% on SP given → convert and find actual profit% on CP
7. Shopkeeper marks up then discounts → net profit or loss%
8. Overall profit/loss when two items bought/sold at different %
9. Find MP to ensure desired profit% after a given discount%
