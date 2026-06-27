# Syllogism - Exam Patterns, Concepts & Tricks
## For: TCS NQT & Placement Aptitude Rounds

---

## WHAT IS SYLLOGISM?
Syllogism is a form of logical reasoning where conclusions are drawn from two or more given statements (called premises). You must determine what MUST be true, what CAN be true, and what CANNOT be true — based purely on logic, not real-world knowledge.

GOLDEN RULE: Never use your general knowledge. Go only by what the statements say.

---

## CORE TERMINOLOGY

| Term | Meaning | Example |
|---|---|---|
| Universal Positive (A) | All X are Y | All cats are animals |
| Universal Negative (E) | No X is Y | No cats are dogs |
| Particular Positive (I) | Some X are Y | Some cats are black |
| Particular Negative (O) | Some X are not Y | Some cats are not black |

Statement types remembered as: A E I O

---

## VENN DIAGRAM APPROACH (Most Reliable Method)

Draw circles for each subject. For each statement type:
- All A are B → Circle A is completely inside Circle B
- No A is B → Circles A and B are completely separate (no overlap)
- Some A are B → Circles A and B partially overlap
- Some A are not B → Part of Circle A is outside Circle B

Steps:
1. Draw the most definite/universal statement first
2. Draw the second statement relative to the first
3. Draw ALL possible valid Venn diagrams (there may be more than one)
4. A conclusion is TRUE only if it holds in ALL possible diagrams
5. A conclusion is POSSIBLE if it holds in at least one diagram

---

## STANDARD CONCLUSION RULES (Direct Method)

### Rule 1 - A + A = A
All A are B + All B are C → All A are C [Valid]

### Rule 2 - A + E = E
All A are B + No B is C → No A is C [Valid]

### Rule 3 - E + A = O* (Particular Negative, reversed)
No A is B + All B are C → Some C are not A [Valid]

### Rule 4 - I + A = I
Some A are B + All B are C → Some A are C [Valid]

### Rule 5 - E + I = O* (reversed)
No A is B + Some B are C → Some C are not A [Valid]

### Rule 6 - A + I = I (middle term distributed)
All A are B + Some B are C → No definite conclusion [Invalid — middle term B not fully used]

### INVALID Combinations (No conclusion possible):
- I + I = No conclusion (Some + Some = Nothing)
- O + anything = No conclusion
- I + E = No conclusion directly
- Two negative premises = No conclusion

---

## COMPLEMENTARY PAIR CONCEPT [KEY FOR EXAMS]

When a conclusion and its complement together cover all possibilities, one of them MUST be true. These are called complementary pairs:

| Pair | Why complementary |
|---|---|
| "Some A are B" and "No A is B" | Together they are exhaustive |
| "All A are B" and "Some A are not B" | Together exhaustive |

In MCQ options: if you see "Either (i) or (ii) follows" as a choice, check if (i) and (ii) are complementary pairs. If yes → that option is correct even if neither alone is definitely true.

---

## EXAM PATTERNS (Most Frequent to Least Frequent)

### Pattern 1 - Two Statement, Two/Four Conclusions [MOST COMMON]
Given 2 statements, 2 or 4 conclusions labeled I, II, III, IV.
Answer choices: Only I follows / Only II follows / Both follow / Neither follows / Either I or II follows.
Approach: Draw Venn → check each conclusion against ALL possible diagrams.

### Pattern 2 - Three Statement Syllogism [FREQUENT in TCS NQT]
Three premises given, conclusions drawn from any two of them in chain.
Approach: Apply rules pairwise → (St1 + St2) → intermediate → (intermediate + St3).

### Pattern 3 - Possibility / Possibility Questions [VERY FREQUENT]
"Which of the following is a possibility?"
A conclusion is POSSIBLE if there EXISTS at least one valid Venn arrangement where it holds — even if it does not definitely follow.
Key: "Some A are B" is always a possibility unless "No A is B" is definitively proven.

### Pattern 4 - Coded Syllogism
Statements given in coded language (symbols, numbers, shapes).
Approach: Decode each coded statement into A/E/I/O form → apply standard rules.

### Pattern 5 - Negative Conclusion Trap
"Some A are not B" does NOT mean "No A is B".
"No A is B" does NOT mean "No B is A" — wait, actually it does (E is reversible).
Reversibility rules:
- A (All A are B) → NOT reversible to All B are A. Converts to: Some B are A (I)
- E (No A is B) → Fully reversible: No B is A
- I (Some A are B) → Fully reversible: Some B are A
- O (Some A are not B) → NOT reversible at all

---

## CONVERSION RULES (Crucial)

| Original Statement | Valid Conversion |
|---|---|
| All A are B (A-type) | Some B are A (I-type) |
| No A is B (E-type) | No B is A (E-type) |
| Some A are B (I-type) | Some B are A (I-type) |
| Some A are not B (O-type) | Cannot be converted |

These conversions are used when conclusion subject/predicate order is swapped.

---

## SPEED TRICKS

### Trick 1 - The AEIO Quick Reference
- A = All → Universal Positive → full containment
- E = No → Universal Negative → complete separation
- I = Some → Particular Positive → partial overlap
- O = Some not → Particular Negative → partial exclusion

### Trick 2 - Definite vs Possible Conclusion
- Definite → holds in EVERY possible Venn diagram
- Possible → holds in AT LEAST ONE Venn diagram
- "Some A are B" is always at least POSSIBLE unless statements explicitly rule it out

### Trick 3 - Quick Invalidity Check
Before drawing Venn, check:
- Are both premises negative? → No conclusion (invalid)
- Does middle term appear in conclusion? → Invalid (middle term must not appear in conclusion)
- Is the conclusion stronger than what premises allow? → Invalid
  Example: Premises give "Some A are C" → cannot conclude "All A are C"

### Trick 4 - Either/Or Check (Complementary Pairs)
Step 1: Check if conclusion I alone follows → No
Step 2: Check if conclusion II alone follows → No
Step 3: Check if I and II are complementary (one is exact negation of other in exhaustive sense)
Step 4: If yes → "Either I or II follows" is correct

Complementary pairs:
- "All A are B" and "Some A are not B"
- "Some A are B" and "No A is B"

### Trick 5 - The Middle Term Test
In a valid syllogism, the middle term (the one that connects both premises) must:
- Appear in BOTH premises
- NOT appear in the conclusion
If middle term appears in conclusion → invalid conclusion

### Trick 6 - Shortcut for All+All and All+No
- All A are B + All B are C → All A are C (chain rule, strongest conclusion)
- All A are B + No B is C → No A is C (strong negative chain)
These two are the most tested in TCS NQT — memorize directly.

### Trick 7 - Possibility Statement Recognition
Watch for these words:
- "All A being B is a possibility" → valid if "No A is B" is not definitively proven
- "Some A are not B being false is a possibility" → means "All A are B" is possible
Always convert the possibility statement back to standard form before checking.

---

## COMMON TRAPS IN EXAMS

1. "All A are B" does NOT mean "All B are A" — never reverse A-type directly
2. "No A is B" DOES mean "No B is A" — E-type is fully reversible
3. Real world knowledge is irrelevant: "All dogs are cats" must be accepted as given
4. Two negative premises NEVER give a valid conclusion
5. Particular conclusion (Some) from two universal premises is valid — don't over-strengthen
6. "Some A are B" and "Some B are C" → NO conclusion about A and C (I+I = nothing)
7. Complementary pair trap: neither alone follows, but "Either/Or" does follow
8. "Some A are not B" cannot be converted — O-type has no valid conversion
9. Possibility questions: check if the possibility is ruled out by a definite conclusion
10. Three-statement questions: solve as two separate two-statement syllogisms in chain

---

## VENN DIAGRAM QUICK REFERENCE

Statement → Diagram shape:
- All A are B → A circle completely inside B circle
- No A is B → A and B circles completely apart
- Some A are B → A and B circles partially overlapping
- Some A are not B → A circle partially outside B circle (overlap + exclusion both exist)

For conclusions:
- Draw the most restrictive arrangement AND the most liberal arrangement
- If conclusion holds in both → Definitely follows
- If conclusion holds in only one → Possible but not definite
- If conclusion holds in neither → Does not follow

---

## STATEMENT COMBINATION TABLE

| Premise 1 | Premise 2 | Conclusion | Type |
|---|---|---|---|
| All A-B (A) | All B-C (A) | All A-C | A |
| All A-B (A) | No B-C (E) | No A-C | E |
| Some A-B (I) | All B-C (A) | Some A-C | I |
| No A-B (E) | All B-C (A) | Some C not A | O* |
| No A-B (E) | Some B-C (I) | Some C not A | O* |
| Some A-B (I) | No B-C (E) | Some A not C | O |
| All A-B (A) | Some B-C (I) | No definite conclusion | - |
| Some A-B (I) | Some B-C (I) | No conclusion | - |
| Any + O type | Any | No conclusion | - |
| Two negatives | Any | No conclusion | - |

O* = conclusion subject and predicate are reversed compared to premises

---

## SOLVED TRAPS FROM PRACTICE
(Will be updated as questions are solved in sessions)

---

## PRACTICE PROBLEM TYPES (TCS NQT Frequency)
1. Two statements, four conclusions — which follow?
2. Three statements syllogism — chain reasoning
3. Either/or complementary pair conclusion
4. Possibility-type conclusions — what is possible?
5. Coded syllogism — decode then apply rules
6. Conversion-based: swap subject/predicate in conclusion and check
7. Negative conclusion traps — Some not vs No
8. Mixed universal and particular premises
