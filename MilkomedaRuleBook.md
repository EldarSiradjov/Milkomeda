# MILKOMEDA - Rulebook

## Table of Contents

1. Introduction
2. Game Objective
3. Components
4. Setup
5. Civilizations
6. Game Play Overview
7. Turn Structure
8. Core Actions
9. Combat Rules
10. Fleets & Ship Types
11. Objective Cards & Claiming
12. Structures
13. Directive & Action Module Rules
14. End of Game
15. Scoring
16. Glossary

---

## 1. INTRODUCTION

**Milkomeda** is a strategic board game where players aim to dominate a grid of space sectors, deploying fleets and utilizing resources to engage in tactical battles and achieve dominance before the galaxy is fully explored. Victory is determined by amassing the most Victory Points (VP) through sector control, fleet management, economic strength, structure placement, and achieving specific goals.

## 2. GAME OBJECTIVE

Be the player with the most Victory Points (VP) at the end of the game. The game ends when **either** the last Sector Card is explored and placed onto the grid, **or** when the last available Victory Point slot on any public Objective Card is claimed by a player.

## 3. COMPONENTS

* **Order Cards:** A deck determining turn order, numbered 1-X for players and including a "Master" card (visual reference). *(Use cards numbered 1 to N, where N is the number of players).*
* **Sector Cards:** Cards representing space sectors, forming the game grid. Each card features four resource/attribute values:
  * Strategic (Red Icon/Value)
  * Scientific (Green Icon/Value)
  * Logistic (Blue Icon/Value)
  * Economic (**Orange** Icon/Value)
  * Keywords defining Sector Type (e.g., Biosphere, Warzone, Extraction, Observatory, Transit, Hazard, Unstable, Wasteland - relevant for Objectives).
  * `back_value`: Exploration Cost paid in Scientific resources.
  * *While not explicitly printed on the corners, assume a default assignment based on Standard Resource Order (TL=Blue, TR=Orange, BL=Red, BR=Green). The player chooses the card's rotation when placing it, affecting which resource faces outwards at each corner.*
* **Structure Tokens:** Tokens representing buildable structures. Each player receives a set of 5:
  * Outpost (x2)
  * Starlance (x1)
  * Hypergate (x1)
  * M-Brain (x1)
* **Fleet Tokens:** 25 tokens per player color, representing generic fleets on the main game board before combat configuration.
* **Homeworld Cards:** Unique starting Sector cards, one per player/civilization (visual reference shows 4 distinct arts, provides base income).
* **Action Display + Marker:** A player board or card showing the 4 core actions. A marker tracks the last action taken, preventing immediate repetition (unless M-Brain allows).
* **Fleet Roster Card:** A private player card showing the 5 Ship Types (Beam Frigate, Shield Cruiser, Artillery Platform, Drone Carrier, Fighter Squadron) as tracks with values (e.g., 0-5). Used **behind a screen** for Secret Fleet Configuration and **later** for Secret Hit Allocation.
* **Fleet Roster Indicators:** 5 tokens per player, used on the Fleet Roster card tracks (behind screen) to set values during secret configuration and secret hit allocation.
* **Player Screens:** (Implied Need) One per player to hide Fleet Roster Card during secret steps.
* **Storage Card:** A player board for tracking the four resource types (Logistic, Economic, Strategic, Scientific) using tracker tokens.
* **Resource Trackers:** Tokens used on the Storage Card to mark current resource levels.
* **Objective Cards:** Cards representing public goals providing VP when achieved. 5 are drawn at the start of the game and placed in the Public Objectives Row. Players track claims on these cards using Claim Markers. *(Note: Objective card details and specific conditions are currently under review and may be simplified/changed.)*
* **Claim Markers:** Player-specific tokens used to mark claimed VP slots on Objective Cards.
* **Directive Cards:** A deck of cards defining spatial pattern conditions players can meet at 2x2 Sector Card intersections. Sorted into three Tiers (D1 Easy, D2 Medium, D3 Hard) based on dot patterns during setup:
  * D1: Exactly 2 colored dots (10 cards).
  * D2: Exactly 3 colored dots, with at least one pair of same colors (10 cards).
  * D3: Exactly 3 different colored dots OR 4 different colored dots (5 cards).
  * *Each Tier has its own discard pile during play.*
* **Action Module Cards:** A deck of cards providing bonus Core Actions when the paired Directive is fulfilled. Sorted into three Tiers (M1 Cheap, M2 Mid, M3 Expensive) based on `cost_amount` during setup:
  * M1: `cost_amount` = 1 (8 cards).
  * M2: `cost_amount` = 2 (8 cards).
  * M3: `cost_amount` = 3 (8 cards).
  * *Each Tier has its own discard pile during play.*
* **Battle Mat:** A shared game tile used for resolving combat. Includes:
  * 5 Nodes arranged in a pentagon, representing the 5 Ship Types.
  * Connecting Arrows between nodes indicating the Rock-Paper-Scissors (RPS) relationships and serving as "Attack Vector Areas".
* **"Marked" Tokens:** A supply of neutral tokens (or use convention of tapping/turning fleet tokens) used during combat resolution to mark ships targeted for destruction.
* **Master of the Order Token:** Passed to the player who acted last in the previous round, granting control over Order Card distribution and Directive/Module adjustments.
* **Dice:** Standard six-sided dice (d6) for combat resolution, **required in unique player colors.**

## 4. SETUP

1. **Prepare Play Area:** Designate a central area for the space grid. Place the Battle Mat nearby. Designate space for 4 **Directive/Module Positions**. Provide area for player screens.
2. **Prepare Decks & Objectives:** Shuffle the Sector Card deck and place it face down. Prepare the Order Card deck. Shuffle the **Objective Card deck**. Draw **5** Objective Cards and place them face-up in a central area visible to all players to form the **Public Objectives Row**. Return the rest to the box. **Prepare empty discard piles for each Tiered Deck (D1, D2, D3, M1, M2, M3).**
3. **Sort & Prepare Tiered Decks:**
    * Separate Directive cards into three piles based on dot patterns: D1 (2 dots), D2 (3 dots, >=1 pair), D3 (3 different dots or 4 dots). Shuffle each pile individually and place face down as Tiered Directive Draw Decks.
    * Separate Action Module cards into three piles based on `cost_amount`: M1 (cost 1), M2 (cost 2), M3 (cost 3). Shuffle each pile individually and place face down as Tiered Action Module Draw Decks.
4. **Establish Initial Directive/Module Pairs:**
    * **Position 1:** Draw the top card of Deck D1 face-up. Draw the top card of Deck M3 face-up below it. Place the remaining D1 and M3 Draw Decks face-down associated with this position.
    * **Position 2:** Draw the top card of Deck D1 face-up. Draw the top card of Deck M2 face-up below it. Place the remaining D1 (shared with Pos 1) and M2 Draw Decks face-down associated with this position.
    * **Position 3:** Draw the top card of Deck D2 face-up. Draw the top card of Deck M2 face-up below it. Place the remaining D2 and M2 (shared with Pos 2) Draw Decks face-down associated with this position.
    * **Position 4:** Draw the top card of Deck D3 face-up. Draw the top card of Deck M1 face-up below it. Place the remaining D3 and M1 Draw Decks face-down associated with this position.
5. **Each Player Chooses Civilization:** Select or randomly assign a Civilization (see Civilizations section).
6. **Gather Player Components:** Each player takes:
    * Their chosen Civilization's unique Homeworld Card.
    * 25 Fleet Tokens of their color.
    * 5 Structure Tokens (2 Outposts, 1 Starlance, 1 Hypergate, 1 M-Brain).
    * 1 Fleet Roster Card and 5 Fleet Roster Indicators.
    * 1 Player Screen.
    * 1 Action Display Card and 1 Action Marker.
    * 1 Storage Card and 4 Resource Trackers.
    * A supply of their Claim Markers.
    * A set of Dice in their player color.
7. **Place Homeworld:** Players place their Homeworld card in a corner of the designated grid area.
8. **Initial Fleets:** Place 3 Fleet Tokens on your Homeworld sector.
9. **Initial Resources:** Place your **Blue, Orange, and Red** Resource Trackers on the value **3** on your Storage Card. Place your **Green** Resource Tracker on the value **5**.
10. **Initial Action Marker:** Place the Action Marker on a designated "start" position off the main actions on the Action Display Card.
11. **Reveal Adjacent Sectors:** Each player draws the top 2 cards from the Sector Deck. **Pay Exploration Cost:** Calculate the total `back_value` of these 2 cards. If you can afford the total cost, pay this amount in **Green (Scientific)** resources and place both cards face-up adjacent to your Homeworld sector in any orientation (declare orientation). If you cannot afford the total cost, choose one card you *can* afford, pay its `back_value` in Green, place it adjacent to your Homeworld (declare orientation), and shuffle the other card back into the Sector Deck. If you can afford both but choose to only place one, pay its cost, place it, and shuffle the unplaced card back into the Sector Deck. Shuffle any other unused drawn cards back into the Sector Deck.
12. **Place Shared Components:** Place the "Marked" tokens supply near the Battle Mat.

## 5. CIVILIZATIONS

Each Civilization provides unique passive abilities or advantages. *(See Appendix B for detailed lore)*.

* **Stellar Architects:** Megastructures (Starlance, Hypergate, M-Brain) cost 1 fewer **Orange** (Economic) resource to build.
* **Quantum Sentinels:** Gain 1 **Red** (Strategic) resource each time you initiate an Attack action (either Main or via Module).
* **Void Navigators:** **\[Ability TBD - Pindown removed]** *(Placeholder: Consider ability related to movement efficiency, Hypergates, or perhaps resilience in empty/hazardous space).*
* **Helix Cultivators:** When claiming an Objective VP slot, gain 1 **Scientific (Green)** resource immediately.

## 6. GAME PLAY OVERVIEW

Players take turns performing actions to explore the galaxy (placing Sector cards), expand their presence (moving fleets), exploit resources (gaining income), build fleets and structures, and engage in combat to control sectors. Directive/Module pairs offer opportunities for bonus actions. The goal is to accumulate the most Victory Points.

## 7. TURN STRUCTURE

The game is played in rounds. Each round consists of the following phases:

* **Phase 1: Determine Turn Order & Adjust Directives:**
  * **First Round:** Shuffle the Order Card deck (Master + Player numbers). Each player draws one card and reveals it simultaneously. Lowest number goes first, then next lowest, etc. The player drawing the "Master" card goes last and holds it. *(No Directive adjustment in the very first round).*
  * **Subsequent Rounds:**
        1. The player who acted *last* in the previous round (holding the Master Card) takes the **Master of the Order Token**.
        2. **Master Adjusts Directives/Modules (Tier-Locked):** The Master of Orders *must* choose **one** of the following actions, targeting a single **Directive/Module Position (1-4)**:
            ***A) Refresh Pair:** Choose one Position. Discard both its face-up Directive and Action Module cards into their respective Tiered Discard Piles. Draw replacements from the top of that Position's assigned Draw Decks (see Draw Replacement rule below).
            * **B) Refresh Directive:** Choose one Position. Discard its face-up Directive card into its Tiered Discard Pile. Draw a replacement from that Position's assigned Directive Draw Deck (see Draw Replacement rule below).
            * **C) Refresh Module:** Choose one Position. Discard its face-up Action Module card into its Tiered Discard Pile. Draw a replacement from that Position's assigned Action Module Draw Deck (see Draw Replacement rule below).
        3. **Draw Replacement Rule:** When drawing a replacement card, attempt to draw the top card from the corresponding Tiered Draw Deck. **If that Draw Deck is empty:** Shuffle that Tier's entire Discard Pile to form a new face-down Draw Deck for that Tier, then draw the top card. (If both Draw Deck and Discard Pile for that Tier are empty, the slot remains empty).
        4. **Propose Turn Order:** The Master draws *two* Order Cards (numbered player cards) and reveals them. They then *propose* a distribution of all Order Cards (the two revealed + remaining face down player cards + the Master Card) among all players (including themselves).
        5. **Bribing:** Players may openly discuss and bribe the Master of Orders (regarding *both* the Directive/Module refresh action *and* the Order Card distribution), immediately transferring resources shown on Storage Cards.
        6. **Final Distribution:** The Master of Orders makes the final decision, distributes the cards. Players simultaneously reveal their received Order Card. Lowest number goes first, etc. The player receiving the Master Card goes last.
* **Phase 2: Player Actions:** Starting with the first player and proceeding in turn order, each player performs their turn:
    1. **Gain Income:**
        * Gain 3 of each resource type (Logistic, Economic, Strategic, Scientific) from your Homeworld.
        * For each *other* Sector Card you control, gain resources matching the **`values`** shown on that card.
        * If you control an M-Brain, for each sector you control that is adjacent to the M-Brain's sector, gain 1 additional resource **of your choice**.
        * Update Storage Card.
    2. **Choose Main Core Action:** Select one of the 4 Core Actions (Explore, Move, Build, Attack) on your Action Display card *that is different from the action you took as your main action last turn* (unless M-Brain allows repeat). Place your Action Marker on the chosen action.
    3. **Pay Main Action Cost:** Pay any resource costs associated with the chosen main Core Action. Adjust trackers on Storage Card.
    4. **Perform Main Core Action:** Resolve the effects of the chosen main Core Action fully.
    5. **Check Directives & Activate Optional Module Action:** After resolving the Main Core Action:
        * **Identify Candidate Intersections:** The current player identifies all **Intersection Points** on the grid where **at least one of the four contributing sector corners belongs to a Sector Card they currently control.**
        * **Scan Candidates:** The player then checks *only these candidate intersections* to see if any achieve **Pattern Matching** (see Glossary) for one of the public **Directive Cards**.
        * **Activate (if matched and desired):** If a match is found, the player *may* choose to activate the paired **Action Module**:
            * **Declare Intent:** State intent to use the Module.
            * **Check Validity:** The Core Action type indicated by the Action Module **must be different** from the Main Core Action just performed this turn. If it is the same, the Module cannot be activated.
            * **Pay Module Cost:** Pay the resource cost listed on the Action Module card. Adjust Storage Card.
            * **Declare Module Action:** Declare the Core Action indicated by the Action Module.
            * **Pay Action Cost:** Pay all normal resource costs associated with performing this secondary Core Action (e.g., Orange/Blue for Build, Green for Explore placement, Blue for Attack movement/Structure attack). Adjust Storage Card.
            * **Perform Module Action:** Resolve the effects of this secondary Core Action fully.
            * **Limit:** A player may only activate one Action Module per turn.
    6. **Set Last Action:** Note which action (Main or Module) was performed chronologically last this turn for next turn's action repetition check.
    7. **Check & Claim Objectives:** Immediately after any action (Main or Module) or income phase that results in meeting the condition for an unclaimed VP slot on a Public Objective Card, the player *may* claim it (Limit 1 claim per turn). See Section 11.1.
* **Phase 3: Round End:** After all players have completed their turn, check for game end conditions. If the game continues, pass the Master of the Order token to the player who just acted last (holding the Master Card), and begin the next round (Phase 1).

## 8. CORE ACTIONS

* **A. EXPLORE ACTION**
    1. **Declare Probes:** Send out up to 2 virtual Probes from sectors you control containing at least one fleet. Note origin sector(s).
    2. **(Optional) Scientific Boost:** Spend **Green** (Scientific) resources *now*. Each spent allows drawing one additional Sector Card.
    3. **Draw Cards:** Draw 2 (or more, if boosted) cards from Sector Deck. Reveal them.
    4. **Place Cards:** Place revealed cards face-up onto the grid. Each must be placed adjacent to a probe's origin or an already placed card in a chain from a probe. **Declare the orientation** (rotation) of each placed card.
        * *Hypergate Boost:* Probe from Hypergate sector can place its card up to **two** spaces away (through explored sectors).
    5. **Pay Exploration Cost:** Calculate **total `back_value`** of all placed cards. Pay this amount in **Green (Scientific)** resources. If unaffordable, choose which card(s) not to place and shuffle back into the Sector Deck.
    6. **Game End Trigger:** If drawing empties the Sector Deck, the game ends after placing/paying for the final card(s). Triggering player gains 5 VP.

* **B. MOVE ACTION**
  * **Effect:** Choose up to two controlled origin sectors. Move any number of your Fleets from there to explored sectors within range. Does *not* trigger combat.
  * **Base Range:** 1 sector.
  * **Logistic Boost:** Spend **Blue** (Logistic). Each resource increases range by 1 for this action.
  * **Hypergate Boost:** Movement from Hypergate sector increases range by 1 (stacks with Logistic Boost).
  * **Opponent Presence:** Moving into or through sectors containing opponent fleets has no inherent effect on movement range or stopping fleets during a Move Action.
  * **Arrival & Control:** Reassess control after movement. Control = most Fleets. **Tiebreaker:** If fleets are tied, the player who controlled the sector *before* the move action retains control (if involved in the tie); otherwise, it becomes uncontrolled.

* **C. BUILD ACTION**
  * **Cost:** Pay combined **Orange** (Economic) and **Blue** (Logistic) costs for chosen options.
  * **Build Options (Choose up to 2 in any combination):**
        1. **Build Fleets:**
            *Pay 1 **Orange** per fleet.
            * Place up to 2 Fleets in Homeworld.
            ***Outpost Bonus:** For each controlled Outpost sector, build +1 Fleet (paying cost) in *that Outpost's sector*.
        2. **Build Structures:**
            * Pay structure cost (see table). Place 1 structure in a controlled sector without your structure of the same type (except Outposts). Limit 1 Starlance, 1 Hypergate, 1 M-Brain, 2 Outposts per player.
            ***Benefits Active:** Start of your next turn.
            * **Structure Costs & Benefits:**

                | Structure | **Blue** Cost | **Orange** Cost | Benefit                                                                           | VP   |
                | :-------- | :------------ | :-------------- | :-------------------------------------------------------------------------------- | :--- |
                | Outpost   | 1             | 3               | Build +1 fleet in sector.                                                         | 2    |
                | Starlance | 1             | 4               | Enable Attack Structure option.                                                   | 2    |
                | Hypergate | 2             | 6               | Explore range +2 sectors (placement distance). Move range +1 sector.              | 2    |
                | M-Brain   | 4             | 7               | +1 income/choice from adjacent controlled sectors. Allows repeating *main* action. | 3    |

* **D. ATTACK ACTION**
  * **Effect:** Choose up to 2 options:
        1. **Attack Fleets:**
            *Declare attack on adjacent sector with opponent fleets. Choose up to 2 controlled origin sectors.
            * Pay 1 **Blue** per sector boundary crossed to reach target. (Min 1).
            *Move any Fleets from origin(s) into contested sector.
            * **Trigger Combat:** Initiate Combat sequence (Section 9).
            ***Hypergate Attack:** Attack any sector connected via explored path from Hypergate. Pay **Blue** cost for path length. Cannot cross unexplored sectors.
        2. **Attack Structure:**
            * Requires controlling a Starlance. Choose one Starlance.
            *Pay 2 **Red** (Strategic) and 2 **Blue** (Logistic).
            * Choose adjacent sector containing *any* structure. Remove it to owner's supply. (Unavailable if no Starlances controlled).

## 9. COMBAT RULES

Resolves conflicts when fleets from different players occupy the same sector after an Attack Action. Uses the "Vector Command" system.

### 9.A. Combat Sequence

1. **Initiation:** Identify the player whose Attack Action initiated combat (the **Attacker**) and any other players with fleets present (the **Defenders**). All players with fleets in the sector participate.
2. **Fleet Configuration (Secret & Simultaneous):**
    * All participating players go **behind their Player Screens**.
    * Secretly assign your fleet tokens currently in the contested sector to the 5 ship type nodes on your *Fleet Roster card* by setting the **Fleet Roster Indicators** on the corresponding tracks to the number of ships of that type. The total number across indicators must match your fleet count in the sector.
    * Simultaneously **reveal** the Fleet Roster cards.
    * Place the corresponding physical *fleet tokens* from the sector onto the appropriate Ship Type Nodes on the shared **Battle Mat**.
    * *The Fleet Roster Card is now cleared and available for the next secret step.*
3. **Determine Dice Allocation (Vector-Based):**
    * Each participating player determines their total dice pool for the round:
    * Look at the Battle Mat. For **each** Ship Type node where you have **at least one** fleet token:
        * Check the **two** outgoing Attack Vector arrows from that node.
        * For **each** of those two arrows: If there is **at least one enemy** fleet token on the node that the arrow points **to**, you gain **one die** for activating that specific vector.
    * **Node Cap:** You can gain a maximum of **two dice** *total* from any single Ship Type node you control.
    * **Total Dice:** Gather the total number of dice earned from all nodes where you have ships. Use dice of your player color. *(Confirm if there's an absolute player cap, e.g., max 5 dice total, if desired).*
4. **Roll Dice Pool (Simultaneous, Consolidated):**
    * Each participating player takes their allocated pool of dice.
    * All players roll their entire pool of **colored dice** simultaneously in their own play area.
5. **Identify Successes ("Hit Pool"):**
    * Each player examines their rolled dice and gathers all dice showing a success (**5 or 6**). These successes form their personal "Hit Pool" for the round. Set aside the misses.
6. **Secretly Allocate Hits on Roster (Simultaneous):**
    * All participating players go **behind their Player Screens** again with their *cleared* Fleet Roster Card.
    * Look at your Hit Pool total (number of successes). Look at the Battle Mat for currently valid Attack Vectors (any of your ship types pointing via an arrow to any enemy ship type they counter that is present).
    * Secretly set your **Fleet Roster Indicators** on the 5 tracks: The track represents the **enemy ship type** you intend to hit. The **value (e.g., 1-5) you set the indicator to** represents **how many of your hits** you are allocating *to damage that enemy type*.
    * The total value set across all 5 indicators must equal the total number of successes in your Hit Pool. You can only allocate hits to tracks corresponding to enemy ship types reachable via valid Attack Vectors from your ships currently on the Battle Mat.
7. **Simultaneous Reveal of Rosters (Damage Allocation):**
    * All players remove their screens and reveal their Fleet Roster Cards, showing their damage allocation decisions for the round.
8. **Sequentially MARK Targets (Open Allocation):**
    * Determine allocation order: The **Attacker** resolves fully first, then any other players involved resolve fully in **player turn order** relative to each other.
    * **Active Player's Turn (e.g., Player A):**
        * Look at your revealed Roster showing your hit allocations (e.g., '2' hits allocated to Track #2: Shield Cruisers).
        * For each hit allocated to a specific track (enemy type): Choose one enemy fleet token of that type currently on the Battle Mat. **Place a "Marked" token** on that enemy fleet token (or tap/turn it sideways).
        * *Target Choice:* If multiple opponents have ships of the target type, you choose which opponent's ship to Mark for each allocated hit. A ship can receive multiple Marks.
        * Repeat this marking process for all hits allocated on your Roster. Mark targets based on the current board state (no ships are removed yet).
    * **Next Player's Turn:** Once the active player has finished marking targets for all their allocated hits, the next player in the resolution order repeats the marking process based on *their* revealed roster.
    * Continue until all participating players have marked targets corresponding to their revealed allocations.
9. **Resolve Casualties (Simultaneous Removal):**
    * **After** all players have finished Step 8 (Marking).
    * Look at the Battle Mat.
    * **Simultaneously remove ALL** fleet tokens that have **one or more "Marked" tokens** on them. Return removed tokens to their owners' supply.
    * Remove all "Marked" tokens from the board.
10. **End of Combat Round Check:**
    * After resolving casualties, check the Battle Mat.
    * If fleets belonging to **more than one player** remain, a **New Combat Round** begins. Return to **Step 3 (Determine Dice Allocation)** based on the remaining fleets.
    * If only **one player** has fleets remaining, or **no players** have fleets remaining, **Combat Ends**.
11. **Post-Combat Control:**
    * If one player has fleets remaining, they take or retain control of the sector.
    * If no players have fleets remaining (mutual destruction), the sector becomes **uncontrolled**, **unless** one of the players involved was the original Defender *and* had a structure present in the sector *before* the combat started. In that specific case, that player retains control of the sector.

### 9.B. The Battle Mat

* **Node Representation:** 5 nodes for 5 Ship Types. Place configured fleet tokens here during combat.
* **Arrows Indication:** Show which type counters which target type (defining valid Attack Vectors). Used for determining dice allocation (Step 3) and validating hit allocation choices (Step 6 & 8).
* **Attack Vector Areas:** The arrows visually represent the paths attacks follow. Hit dice/tokens are placed onto these arrows during the Marking phase (Step 8).

## 10. FLEETS & SHIP TYPES

Fleets configured into types during combat via RPS system.

* **Rules & Descriptions:**
  * **Beam Frigate:**
    * *Counters:* Shield Cruiser, Drone Carrier
    * *Countered By:* Artillery Platform, Fighter Squadron
    * *Description:* Uses precise energy beams effective against shields and drone swarms, but vulnerable to long-range artillery and agile fighters.
  * **Shield Cruiser:**
    * *Counters:* Fighter Squadron, Artillery Platform
    * *Countered By:* Beam Frigate, Drone Carrier
    * *Description:* Heavy shields absorb fighter attacks and mitigate artillery impact, but can be penetrated by focused beams or overwhelmed by coordinated drone attacks.
  * **Artillery Platform:**
    * *Counters:* Drone Carrier, Beam Frigate
    * *Countered By:* Shield Cruiser, Fighter Squadron
    * *Description:* Engages from extreme range, effective against frigates and drone swarms, but vulnerable to shielded cruisers absorbing hits and fighters closing distance.
  * **Drone Carrier:**
    * *Counters:* Fighter Squadron, Shield Cruiser
    * *Countered By:* Beam Frigate, Artillery Platform
    * *Description:* Overwhelms fighters with numbers and exploits shield gaps, but vulnerable to anti-swarm beams and area-effect artillery.
  * **Fighter Squadron:**
    * *Counters:* Beam Frigate, Artillery Platform
    * *Countered By:* Shield Cruiser, Drone Carrier
    * *Description:* Agile craft dodge beams and evade slow artillery to counter-attack, but struggle against heavy shields and drone swarms.

## 11. OBJECTIVE CARDS & CLAIMING

Five Objective Cards form the **Public Objectives Row**. *(Note: Objective card details and specific conditions are currently under review and may be simplified/changed.)*

* **11.1. Claiming Objectives**
  * **Eligibility:** During your turn, if you meet the condition for an unclaimed VP slot on a Public Objective Card.
  * **Timing:** Declare claim **immediately** after the game state reflects the condition is met (after action resolution, during income, etc.).
  * **Limit:** Max **one** Objective VP slot claim per turn.
  * **Procedure:** Declare claim. Place one **Claim Marker** on that specific VP slot.
  * **Exclusivity:** Claimed slots cannot be claimed again.
  * **"This Turn" Objectives:** Must be claimed immediately following the event. Opportunity lost if you proceed without claiming.
  * **Game End Trigger:** Claiming the very last available VP slot across all 5 cards ends the game immediately.

## 12. STRUCTURES

Provide ongoing benefits and VP. See Build Action for costs/placement.

* **Outpost:** Enables fleet building in sector (2 VP).
* **Starlance:** Enables Attack Structure action (2 VP).
* **Hypergate:** Improves Explore/Move ranges (2 VP).
* **M-Brain:** When gaining income, for each sector you control that is adjacent to the M-Brain's sector, gain 1 additional resource **of your choice**. Allows repeating the *main* Core Action on consecutive turns. (3 VP).
* **Interaction with Combat:** Allows the original defender to retain control of the sector on mutual destruction if they had a structure present. No direct active combat bonus currently defined.

## 13. DIRECTIVE & ACTION MODULE

Four public **Directive/Module Positions** offer bonus actions.

* **Tiers:** Directives (D1 Easy, D2 Med, D3 Hard) and Modules (M1 Cheap, M2 Mid, M3 Exp) are tiered.
* **Positions:** Initial setup pairs tiers: Pos 1 (D1/M3), Pos 2 (D1/M2), Pos 3 (D2/M2), Pos 4 (D3/M1).
* **Activation:** After your Main Action, check for **Pattern Matching** at intersections adjacent to your controlled sectors. If a match for a Directive is found, you *may* activate its paired Module.
* **Module Use:** Pay Module cost + normal Action cost. Module action must differ from Main Action. Limit 1 Module activation per turn. See Turn Structure Phase 2, Step 5 for full details.
* **Master Influence:** Master of Orders refreshes one pair/card within its tier each round (Phase 1, Step 2).
* **Deck Management:** Tiered decks reshuffle from their discard pile when empty.

## 14. END OF GAME

Game ends **immediately** when:

1. **Grid Completion:** Last Sector Card drawn, placed, paid for. Exploring player gains 5 bonus VP.
2. **Objective Completion:** Player claims the final available VP slot on any Public Objective Card.

Proceed immediately to Scoring.

## 15. SCORING

Calculate final VP:

1. **Grid Completion Bonus:** +5 VP for player placing last Sector card (if applicable).
2. **Controlled Sectors:** +1 VP per controlled sector.
3. **Structures:** +VP per structure owned on the map (Outpost/Starlance/Hypergate=2 VP, M-Brain=3 VP).
4. **Fleet Tokens:** +1 VP per 3 of your Fleet Tokens remaining on the map.
5. **Economic Resources:** +1 VP per 1 **Orange** resource remaining.
6. **Special Goals (Civilization Specific):** ... *(Currently only Helix Cultivators gain minor non-VP benefits)*
7. **Objective Cards:** Gain VP equal to value of each Objective slot claimed with your Claim Marker. *(Objectives pending review)*

Player with most VP wins. **Tiebreaker:** Most total remaining non-Orange resources (Blue+Red+Green combined). If still tied, most Fleet Tokens remaining on the map.

## 16. GLOSSARY

* **Action Display:** Player board showing core actions.
* **Action Marker:** Token on Action Display tracking last main action.
* **Action Module:** Card providing a bonus action. See Section 13.
* **Action Repetition:** See Section 7, Phase 2, Step 2 & M-Brain (Section 12).
* **Attack Action:** Core action for Combat or Structure Attack.
* **Attack Vector:** An arrow on the Battle Mat showing a valid RPS counter (Origin Ship Type -> Target Ship Type). Used for determining dice allocation and validating hit allocation.
* **Attacker:** The player whose Attack Action initiated the current combat sequence. Resolves first in sequential steps.
* **Battle Mat:** Tile for resolving combat. See Section 9.B.
* **Build Action:** Core action for Fleets/Structures.
* **Claim Marker:** Player token for claiming Objective VP slots.
* **Combat:** Process triggered by Attack Action, uses "Vector Command". See Section 9.
* **Controlled Sector:** Sector with most Fleets. **Tiebreaker:** If fleets are tied, the player who controlled the sector *before* the most recent Move/Attack action that caused the tie retains control (if involved in the tie); otherwise, it becomes uncontrolled. Exception: Defender with structure retains control on mutual destruction (See Section 9.A Step 11).
* **Defender(s):** Player(s) with fleets in a sector when an opponent initiates combat via an Attack Action into that sector.
* **Directive Card:** Card defining a spatial pattern condition. See Section 13.
* **Dice Allocation:** Process (Step 3 of Combat) determining how many dice each player rolls based on their ships and valid attack vectors.
* **Economic (Resource): Orange** resource.
* **Explore Action:** Core action to place new Sector cards.
* **Fleet Configuration:** Secret assignment (Step 2 of Combat) of fleet tokens to ship types using the Fleet Roster Card.
* **Fleet Roster Card:** Private player card with 5 tracks (representing ship types) and values. Used behind screen for **secret fleet configuration** (Step 2), then cleared and used again for **secret hit allocation** (Step 6).
* **Fleet Roster Indicators:** Tokens used behind screen on the Fleet Roster Card tracks to set ship counts (Configuration) or allocate hits (Hit Allocation).
* **Fleet Tokens:** Generic tokens for fleets on main board.
* **Hit Allocation:** Secret decision (Step 6 of Combat) made on the Fleet Roster Card determining how many hits to assign against specific enemy ship types.
* **Hit Pool:** The set of dice that rolled successes (5 or 6) in Step 5 of Combat.
* **Homeworld:** Starting Sector card.
* **Hypergate:** Structure boosting Explore/Move.
* **Intersection Point:** Point where four Sector Card corners meet. Used for checking Directive Pattern Matching.
* **Logistic (Resource): Blue** resource.
* **M-Brain:** Structure providing income bonus and allowing repeat actions.
* **Marked Token / Marked Status:** A neutral token placed on a fleet token (or the fleet token is tapped/turned) during Step 8 of Combat (Mark Targets). Designates the fleet for removal in Step 9 (Resolve Casualties). Removed after casualties are resolved.
* **Master of the Order Token:** Grants control over Turn Order/Directive refresh.
* **Move Action:** Core action to move fleets without combat.
* **Node:** Point on Battle Mat representing a Ship Type.
* **Objective Cards:** Public goals for VP. *(Pending review)*.
* **Order Cards:** Determine turn order.
* **Outpost:** Structure allowing local fleet building.
* **Pattern Matching (Directives):** Process of checking resource types at Intersection Points against a Directive Card. See Section 13 & Glossary entry in previous version for full details.
* **Player Screen:** Component used to hide the Fleet Roster Card during secret steps.
* **Rock-Paper-Scissors (RPS):** System defining Ship Type counters. See Section 10.
* **Scientific (Resource): Green** resource (Explore boost/cost).
* **Sector Card:** Card forming map grid.
* **Standard Resource Order:** (For corner assumption) TL=Blue, TR=Orange, BL=Red, BR=Green.
* **Starlance:** Structure enabling Attack Structure.
* **Storage Card:** Player board for tracking resources.
* **Strategic (Resource): Red** resource.
* **Structure Tokens:** Physical tokens for structures.
* **Success:** A die roll result of 5 or 6 in combat.
* **Tiered Decks:** Directive (D1, D2, D3) and Module (M1, M2, M3) decks. See Section 13.

---
