# Ghost Strategy for Iterated Prisoner's Dilemma

## Behavior Rules

1. **First Move**: Always defects (plays 0)
2. **Against Overly Cooperative Opponents**:
   - If opponent cooperated >15 times total → always defect
3. **Against Non-Cooperative Opponents**:
   - If no cooperation in last 15 rounds → always defect
4. **Default Behavior**:
   - Alternates between defect (0) and cooperate (1)

## Strategy Profile

| Trigger Condition | Action | Purpose |
|-------------------|--------|---------|
| First move | Defect | Test opponent |
| Opponent cooperated >15 times total | Always defect | Exploit pushovers |
| No cooperation in last 15 rounds | Always defect | Punish non-cooperators |
| Normal case | Alternate 0/1 | Stay unpredictable |

When selecting the next opponent:

It choose the first available opponent with whom It has played fewer than 200 rounds.