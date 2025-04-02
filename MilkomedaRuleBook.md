# MILKOMEDA - Rulebook Draft

## Table of Contents (Conceptual)

1. Introduction & Lore
2. Game Objective
3. Components
4. Setup
5. Civilizations
6. Game Play Overview
7. Turn Structure
8. Core Actions (Explore, Move, Build, Attack)
9. Combat Rules ("Vector Command")
    * Combat Initiation
    * Combat Sequence
    * The Battle Mat
10. Fleets & Ship Types (RPS Details)
11. Objective Cards & Claiming
12. Structures
13. Directive & Action Module Rules
14. End of Game
15. Scoring
16. Glossary
17. Appendix A: Historical Protocol File 147-XC (Lore)
18. Appendix B: Civilization Details (Lore)

---

## 1. INTRODUCTION & LORE

**Milkomeda** is a strategic board game where players aim to dominate a grid of space sectors, deploying fleets and utilizing resources to engage in tactical battles and achieve dominance before the galaxy is fully explored. Victory is determined by amassing the most Victory Points (VP) through sector control, fleet management, economic strength, structure placement, and achieving specific goals.

*(See Appendix A for the full text of Historical Protocol File 147-XC detailing the lore background of the Aetharan Ascendancy and their exodus into The Caelum Void).*

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
* **Fleet Roster Card:** A private player card showing the 5 Ship Types (Beam Frigate, Shield Cruiser, Artillery Platform, Drone Carrier, Fighter Squadron). Used for Secret Fleet Configuration and **Secret Hit Allocation (Targeting) by ship type.**
* **Fleet Roster Indicators:** 5 tokens per player, used on the Fleet Roster card during secret configuration **and secret targeting allocation.**
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
  * Connecting Arrows between nodes indicating the Rock-Paper-Scissors (RPS) relationships and serving as "Attack Vector Areas" for dice placement. Each arrow area allows each player to place 1 die.
* **Master of the Order Token:** Passed to the player who acted last in the previous round, granting control over Order Card distribution and Directive/Module adjustments.
* **Command Point (CP) Tokens:** \[Placeholder - TBD based on next discussion] Tokens or tracker needed for players to secretly allocate their 2 CP during combat (Maneuver Selection phase).
* **Dice:** Standard six-sided dice (d6) for combat resolution.

## 4. SETUP

1. **Prepare Play Area:** Designate a central area for the space grid. Place the Battle Mat nearby. Designate space for 4 **Directive/Module Positions**.
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
    * 1 Action Display Card and 1 Action Marker.
    * 1 Storage Card and 4 Resource Trackers.
    * A supply of their Claim Markers.
    * \[Placeholder: Define starting CP tokens/markers if physical, based on TBD mechanic].
7. **Place Homeworld:** Players place their Homeworld card in a corner of the designated grid area.
8. **Initial Fleets:** Place 3 Fleet Tokens on your Homeworld sector.
9. **Initial Resources:** Place your **Blue, Orange, and Red** Resource Trackers on the value **3** on your Storage Card. Place your **Green** Resource Tracker on the value **5**.
10. **Initial Action Marker:** Place the Action Marker on a designated "start" position off the main actions on the Action Display Card.
11. **Reveal Adjacent Sectors:** Each player draws the top 2 cards from the Sector Deck. **Pay Exploration Cost:** Calculate the total `back_value` of these 2 cards. If you can afford the total cost, pay this amount in **Green (Scientific)** resources and place both cards face-up adjacent to your Homeworld sector in any orientation (declare orientation). If you cannot afford the total cost, choose one card you *can* afford, pay its `back_value` in Green, place it adjacent to your Homeworld (declare orientation), and shuffle the other card back into the Sector Deck. If you can afford both but choose to only place one, pay its cost, place it, and shuffle the unplaced card back into the Sector Deck. Shuffle any other unused drawn cards back into the Sector Deck.

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
            **Outpost Bonus:* For each controlled Outpost sector, build +1 Fleet (paying cost) in *that Outpost's sector*.
        2. **Build Structures:**
            * Pay structure cost (see table). Place 1 structure in a controlled sector without your structure of the same type (except Outposts). Limit 1 Starlance, 1 Hypergate, 1 M-Brain, 2 Outposts per player.
            **Benefits Active:* Start of your next turn.
            * **Structure Costs & Benefits:**

                | Structure | **Blue** Cost | **Orange** Cost | Benefit                                                                            | VP   |
                | :-------- | :------------ | :-------------- | :--------------------------------------------------------------------------------  | :--- |
                | Outpost   | 1             | 3               | Build +1 fleet in sector.                                                          | 2    |
                | Starlance | 1             | 4               | Enable Attack Structure option.                                                    | 2    |
                | Hypergate | 2             | 6               | Explore range +2 sectors (placement distance). Move range +1 sector.               | 2    |
                | M-Brain   | 4             | 7               | +1 income/choice from adjacent controlled sectors. Allows repeating *main* action. | 3    |

* **D. ATTACK ACTION**
  * **Effect:** Choose up to 2 options:
        1. **Attack Fleets:**
            *Declare attack on adjacent sector with opponent fleets. Choose up to 2 controlled origin sectors.
            * Pay 1 **Blue** per sector boundary crossed to reach target. (Min 1).
            *Move any Fleets from origin(s) into contested sector.
            * **Trigger Combat:** Initiate Combat sequence (Section 9).
            **Hypergate Attack:* Attack any sector connected via explored path from Hypergate. Pay **Blue** cost for path length. Cannot cross unexplored sectors.
        2. **Attack Structure:**
            * Requires controlling a Starlance. Choose one Starlance.
            *Pay 2 **Red** (Strategic) and 2 **Blue** (Logistic).
            * Choose adjacent sector containing *any* structure. Remove it to owner's supply. (Unavailable if no Starlances controlled).

## 9. COMBAT RULES

Resolves conflicts when fleets from different players occupy the same sector after an Attack Action.

### 9.A. Combat Sequence

1. **Initiation:** Identify Attacker and Defender(s).
2. **Fleet Configuration (Secret & Simultaneous):** All involved players secretly assign their fleet tokens in the sector to ship type nodes on their Fleet Roster using Fleet Roster Indicators. Reveal simultaneously and place corresponding *fleet tokens* from the sector onto the appropriate Battle Mat nodes, leaving Indicators on the Roster.
3. **Declare Attack Vectors & Place Dice (Open & Simultaneous):** Each player places 1 die into any valid Attack Vector Area (RPS arrow) from their ship type towards an opponent type they counter. Max 1 die *per player* per arrow area. Can target any opponent(s) with valid vectors.
4. **Gain & Allocate Command Points (Secret & Simultaneous):** \[Placeholder - CP Mechanic TBD] Each player gets 2 CP. Secretly allocate, then reveal:
    * `Boost Attack [1CP]`: Roll 1 extra attack die (add to one chosen vector pool).
    * `Boost Defense [1CP]`: Choose *one opponent*. Force them to re-roll 1 successful hit die against you. Announce target on reveal.
    * `Prepare Reshape [2CP]`: If one of your ships survives, you may change its type later.
5. **Roll Dice Pools (Simultaneous):** Roll all placed dice (+ Boost Attack, if applicable). 5+ is potential hit.
6. **Apply Forced Re-rolls:** Targeted attackers re-roll one chosen success die per Boost Defense used against them (if applicable).
7. **Determine Final Hits:** Count own successful hits (5+) after re-rolls.
8. **Secretly Allocate Hits to Target Types (Roster Method):** Each player secretly uses their Fleet Roster Indicators on their Fleet Roster card to indicate *which opponent ship types* they intend to target with their successful hits. Distribute indicators among the valid ship types they counter. *(Example: If you scored 3 hits with Beam Frigates, you might place 2 indicators on the Shield Cruiser slot and 1 indicator on the Drone Carrier slot on your Roster).*
9. **Simultaneous Roster Reveal:** All players reveal their Fleet Roster cards showing the targeting allocations indicated by the Fleet Roster Indicators.
10. **Resolve Targeting & Casualties (Ordered Assignment):** Determine resolution order by Turn Order among combatants (Attacker first). In order, the active player verbally assigns their hits one by one based on their **revealed Roster allocations**. For each allocated hit indicated on their Roster for a specific *type*, they choose one *available* opponent ship token of that type on the Battle Mat to destroy.
    * **Choosing Targets (Multiple Opponents):** Assigner chooses which opponent's ship of the targeted type to hit for each allocated hit.
    * Remove casualties immediately from the Battle Mat. Hits are wasted if no valid targets of the allocated type remain when it's time to assign them.
11. **Execute Prepared Reshapes:** Players who used Prepare Reshape \[2CP] (if applicable) and have surviving fleets *may* now move one surviving ship token on Battle Mat to an adjacent node (following RPS arrow) representing a different type.
12. **End of Round Check:** If >1 player remains, start New Combat Round (Step 3, gain 2 fresh CP - *CP gain pending final mechanic*). If 1 or 0 players remain, Combat Ends.
13. **Post-Combat Control:** The single player with remaining fleets takes or retains control. If mutual destruction (0 survivors), the sector becomes uncontrolled, **unless** one player involved was the original Defender *and* had a structure present in the sector, in which case that player retains control.

### 9.B. The Battle Mat

* **Node Representation:** 5 nodes for 5 Ship Types. Place configured fleet tokens here.
* **Arrows Indication (RPS):** Show which type counters which target type (valid Attack Vectors).
* **Attack Vector Areas:** Lines/arrows where dice are placed for attacks along that vector.

## 10. FLEETS & SHIP TYPES

Fleets configured into types during combat via RPS system.

* **RPS Rules & Descriptions:**
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
* **Interaction with Combat:** Allows the original defender to retain control of the sector on mutual destruction if they had a structure present. No direct combat bonus.

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
* **Action Module:** Card providing a bonus action. When activated *after* performing a Main Core Action (if the corresponding Directive condition is met), allows the player to perform the indicated Core Action as a *secondary* action, provided it is **different** from the Main Core Action just performed. Requires paying **both** the Module's cost **and** the normal cost of the Core Action being performed. Limit one activation per turn. Tiered decks (M1, M2, M3) determine cost. Discarded to Tiered Discard Pile; deck reshuffles from discard when empty.
* **Action Repetition:** Normally, a player cannot choose the same Core Action as their *main* action on consecutive turns. The M-Brain structure allows repeating the *main* Core Action. An action performed via an Action Module cannot be the same as the *main* Core Action chosen in the same turn. The action performed chronologically last in the turn (Main or Module) counts as the "action taken last turn" for restricting the *next* turn's main action choice.
* **Attack Action:** Core action for Combat or Structure Attack.
* **Attack Vector Area:** Arrow on Battle Mat where dice are placed.
* **Battle Mat:** Tile for resolving combat.
* **Build Action:** Core action for Fleets/Structures.
* **Claim Marker:** Player token for claiming Objective VP slots.
* **Command Points (CP):** \[Placeholder - TBD] Combat resource for tactical benefits.
* **Combat:** Process triggered by Attack Action, uses "Vector Command".
* **Controlled Sector:** Sector with most Fleets. **Tiebreaker:** If fleets are tied, the player who controlled the sector *before* the most recent Move/Attack action that caused the tie retains control (if involved in the tie); otherwise, it becomes uncontrolled. Exception: Defender with structure retains control on mutual destruction.
* **Directive Card:** Card defining a spatial pattern condition based on its 4 dots (representing resource types at a 2x2 Sector Card intersection). If a player achieves **Pattern Matching** at an intersection adjacent to their controlled sectors after their Main Action, they may activate the paired Action Module. Tiered decks (D1, D2, D3) determine pattern difficulty. Discarded to Tiered Discard Pile; deck reshuffles from discard when empty.
* **Economic (Resource): Orange** resource.
* **Explore Action:** Core action to place new Sector cards.
* **Fleet Configuration:** Secret assignment of fleet tokens to ship types at combat start using Fleet Roster Indicators on Fleet Roster Card.
* **Fleet Roster Card:** Private player card showing ship types. Used with Fleet Roster Indicators for secret fleet configuration and **secret hit allocation (targeting) by ship type during combat.**
* **Fleet Roster Indicators:** Tokens used on the Fleet Roster Card for secret configuration and targeting allocation.
* **Fleet Tokens:** Generic tokens for fleets on main board.
* **Homeworld:** Starting Sector card.
* **Hypergate:** Structure boosting Explore/Move.
* **Intersection Point:** Point where four Sector Card corners meet. Used for checking Directive Pattern Matching.
* **Logistic (Resource): Blue** resource.
* **M-Brain:** Structure providing +1 resource **of choice** per adjacent *controlled* sector during income, and allows repeating the *main* Core Action on consecutive turns. (3 VP).
* **Maneuver Selection:** Combat phase for allocating CP.
* **Master of the Order Token:** Grants control over Turn Order/Directive refresh.
* **Move Action:** Core action to move fleets without combat.
* **Node:** Point on Battle Mat representing a Ship Type.
* **Objective Cards:** Public goals for VP. *(Pending review)*.
* **Order Cards:** Determine turn order.
* **Outpost:** Structure allowing local fleet building.
* **Pattern Matching (Directives):** Process of checking resource types at corners of an Intersection Point against a Directive Card's colored dots. Checked only at Intersections where the player controls at least one contributing sector corner. Requires resource value > 0 for matched types. White dots ignored. Player must control at least one sector contributing a matched colored corner.
* **Prepare Reshape:** CP option allowing ship type change post-combat (if CP mechanic includes it).
* **Reshape:** Action (via Prepare Reshape) to change surviving ship type (if CP mechanic includes it).
* **Rock-Paper-Scissors (RPS):** System defining Ship Type counters.
* **Scientific (Resource): Green** resource (Explore boost/cost).
* **Sector Card:** Card forming map grid.
* **Standard Resource Order:** (For corner assumption) TL=Blue, TR=Orange, BL=Red, BR=Green.
* **Starlance:** Structure enabling Attack Structure.
* **Storage Card:** Player board for tracking resources.
* **Strategic (Resource): Red** resource.
* **Structure Tokens:** Physical tokens for structures.
* **Targeting Allocation:** Secret use of Fleet Roster Indicators on Fleet Roster Card to determine which enemy ship *types* to hit during combat resolution.
* **Tiered Decks:** Directive (D1, D2, D3) and Module (M1, M2, M3) decks sorted by difficulty/cost. Feed specific Directive/Module Positions. Each Tier has own Draw/Discard pile, reshuffles from discard when empty.

---
