# braven

## stamina changes

Stamina changed to now be a _threshold_ that deals stagger when crossed. Every time this threshold is crossed, bad things happen. Too many times, and the target is K/O'd.

### new stamina rules

- **NEW MECHANIC**: Fatigue. Fatigue is any reduction of Stamina as a result of traveling and/or not resting (becoming tired), as well as reductions due to ability costs.
- Fatigue is reduced slightly after short resting and/or consuming various things, and completely when sleeping (under typical circumstances).
- **NEW MECHANIC**: Stagger. Stagger is a condition that happens when stamina damage is received that is above the current stamina threshold or stamina is spent on an ability when the stamina threshold is at 0. Stagger is always counted after all other damage is dealt, including trauma and wounds.
- Eventually with too much stagger accumulated (or all at once), a target will be knocked out.
- Stagger has 5 ranks with conditions present while that rank is active. Removing stagger will remove the added effect for that rank (with the exception of K/O at 5 ranks).
  1. -20 lost from Initiative, effective immediately (can prematurely end turn)
  2. Health and Sanity damage received is doubled
  3. Unable to use Opportunities, Max Move uses reduced by 1 (typically someone has 3, this reduces move uses to 2)
  4. +2d6 stun (this can be "healed" off with stagger reduction abilities)
  5. K/O (fall where you stand, pass out, cannot take action)
- Stagger ranks can INCREASE a maximum of 3x in a round but only 1 rank increase per attack
  - Dealing 10x the Stamina threshold in one attack is an exception that will immediately add all 5 stagger ranks and K/O the target
- Stagger ranks can DECREASE a maximum of 2x in a round and can decrease
  - "Rest" reduces 1 rank of stagger but cannot be used while stunned, some Charisma and Med/Rest Gifts as well as spells reduce stagger

### balancing changes this causes

- Stamina on the character sheet is now calculated with /10, multipiers purchased or gained reduce this (up to /1 max)
  - All creatures and plebs must have their stamina values reduced by 10
- Mitigation calculations change, since stamina must be much lower now
  - New formula to apply to items/abilities: for stam mit as a mult of 5, add 5 and divide by 2, for mit as a mult of 10, divide by 2 and add 5
  - Stam mitigation max is now 50% (used to be 90). This means previous over-mitigation (90 and above 90) becomes 50
  - Example: 5/10 remains as 5/10, 5/15 is also 5/10, 5/50 becomes 5/30, 5/85 becomes 5/45, 5/90 becomes 5/50 and so on
  - Item crafting tiers and values have changed
- Ability costs are changed, since stamina is not a large pool resource anymore
  - Many abilities have their Stamina cost reduced by an approx equation: ( Stam / 5 - 5 ). These costs now increase Fatigue.
  - Using an ability that costs stamina when you are fully fatigued now adds a rank of Stagger instead.
  - Abilities that heal stamina (see below) now all cost Sanity
- Healing stamina is reduced significantly, either by 5 to 10x less, and mostly only heals fatigue
- Healing stamina abilities now typically also heal a rank of stagger
  - Meditate now only heals 1 rank of stagger (does not heal fatigue)
  - In order to balance fatigue healing, any ability that heals fatigue costs Sanity
- Wounds and Trauma that involve stamina must be reworked (aka Nervous wounds and Trauma damage should increase fatigue)
- Attack and Damage process is now: Calculate hit, calculate initial damage, apply mitigation, calculate trauma points, deal trauma damage, apply wounds, apply stagger
- (needs review) Some items and abilities may increase stamina multiplier when worn or used
- (needs review) Gifts added which interact with stagger, such as being able to only gain a max of 2 per round instead of 3
- (needs review) Gifts and items added that interact with fatigue, such as temporary removal, cost reduction, or healing

## sanity (comfort) changes

"Sanity" will be renamed to "Comfort" as this reflects not only mechanically what Sanity increase and decrease entails, but is also more inclusive language (currently "Sanity" encourages pathologizing language, interpretation, and gameplay).

Also, Stam and Comf are easier to differentiate than Stam and San.

Mechanically, most essential interactions are unchanged. However, reaching 0 Comfort now no longer causes "Insanity" but "Suffering."

### new comfort rules

- **NEW MECHANIC**: Suffering. While below 0 Comfort and until healing back up to 0 or higher, a character is Suffering.
  - Suffering always adds 1 rank of stagger when it is received in combat.
  - Roll for the result of your Suffering: Roll d4 to choose one physical stat (Physique, Wellness, Grace, Prowess) and then roll d4 to choose one mental stat (Erudition, Wits, Charisma, Nerve). All maneuvers performed using those stats receive -50 until Suffering ends. Note that the Host may choose the outcome of these rolls for narrative or character-related reasons (if it makes more sense for the story or otherwise), such as always choosing the same combination for a character because of some kind of history suffering in a particular way. In addition to the maneuver downsides, your character gains the following additional downsides:
    - **Physique/Prowess** + **Erudition**: Who you believe yourself to be is starting to disintegrate. Your Art with the highest Skill value invested receives an additional -100 to all maneuvers. Any Arts with tied maximum skill values all receive -50. Narratively, now any failures at all may provoke ridicule from people who don't like you. You feel a sense of devastation for your loss of self.
    - **Physique/Grace** + **Wits**: You feel paralyzed, unable to act. Your composure is wavering. All Potential costs are increased by 2 for any ability that costs Potential by default. All Potential costs are increased by 1 for any in-combat abilities that do not cost Potential or take time by default. All other actions take 25% longer in order to complete (including sleep and travel). Narratively, you begin to think that others who once relied on you may begin to grow impatient with you as you waste away.
    - **Physique/Prowess** + **Charisma**: You question your bond with your closest friends and lovers. Your connections become painful. Any healing or buffing abilities received by or performed on allies are half as effective (round up, when applicable). Additionally, when an ally receives Trauma Damage, you receive 1 Stagger. Narratively, you believe that you are incapable of being loved and known by the ones you care about. You may withdraw or become insecure.
    - **Physique/Grace** + **Nerve**: You can't handle this anymore. You need an escape, a fantasy, something to help you forget. You begin to dissociate. Meditate no longer heals stagger and you can now only heal a maximum of 1 stagger per round in combat from other sources, and all stun effects received are doubled. Narratively, you might become less and less aware (and more numb) to everything happening around you. You might also seek substances that can increase or decrease your numbness (which may result in addiction).
    - **Wellness/Grace** + **Erudition**: You're worthless. Nothing you do has been good enough. Any time you would crit, you now fumble. Any time you would roll higher in an open ended roll, instead subtract 50 and do not roll higher. Narratively, you believe that others simply view you as a disappointment. You might be depressed or seek validation.
    - **Wellness/Prowess** + **Wits**: You begin to spiral into fear. Panic sets in. You feel compelled to action. If you choose not to move during your turn but you still have at least one use of move left, you take 5 Comfort damage. If you are not actively traveling to a new location, you become unable to heal Fatigue during meditation, rest, or sleep. Narratively, you may grow increasingly anxious or stressed during downtime, slow moments, or when there is inaction.
    - **Wellness/Grace** + **Charisma**: Your sense of self-worth is slipping. You are useless filth. You don't care how others see you as you let yourself go. All maneuvers performed using the stat of yours that has the lowest value receive an additional -50. Additionally this may have broad narrative social effects as you come off as revolting or disgusting in interactions with prejudiced people or on first impressions.
    - **Wellness/Prowess** + **Nerve**: Your mind and body cannot find peace. You carry every failure, every hurt, and every missed opportunity in your thoughts and bones at all times. To avoid making any mistakes again, you now roll a d4 instead for all maneuvers by default. When rolling this d4, a 1 results in a roll of 20, 2 a roll of 40, 3 is 60, and 4 is 80. Any time you fail any roll or miss any attack, receive 20 Fatigue. Narratively, you grow increasingly distressed any time you fail and may simply choose to do less in order to avoid failure.

## miscellaneous

- Snipe shot rework
- Tissue wound (bleeding) rework
-
