# MILKOMEDA - Rulebook Draft (Consolidated)

**Version:** [Date based on this conversation]

**Table of Contents (Conceptual)**

1.  Introduction & Lore
2.  Game Objective
3.  Components
4.  Setup
5.  Civilizations
6.  Game Play Overview
7.  Turn Structure
8.  Core Actions (Explore, Move, Build, Attack)
9.  Combat Rules ("Vector Command")
    *   Combat Initiation
    *   1v1 Combat Sequence
    *   Multi-Way (>2 Player) Combat Sequence
    *   The Battle Mat
10. Fleets & Ship Types (RPS Details)
11. Structures
12. End of Game
13. Scoring
14. Glossary
15. Appendix A: Historical Protocol File 147-XC (Lore)
16. Appendix B: Civilization Details (Lore)

---

**1. INTRODUCTION & LORE**

**Milkomeda** is a strategic board game where players aim to dominate a grid of space sectors, deploying fleets and utilizing resources to engage in tactical battles and achieve dominance before the galaxy is fully explored. Victory is determined by amassing the most Victory Points (VP) through sector control, fleet management, economic strength, structure placement, and achieving specific goals.

*(See Appendix A for the full text of Historical Protocol File 147-XC detailing the lore background of the Aetharan Ascendancy and their exodus into The Caelum Void).*

**2. GAME OBJECTIVE**

Be the player with the most Victory Points (VP) at the end of the game. The game ends when **either** the last Sector Card is explored and placed onto the grid, **or** when the last available Victory Point slot on any public Objective Card is claimed by a player.

**3. COMPONENTS**

*   **Order Cards:** A deck determining turn order, numbered 1-X for players and including a "Master" card (visual reference). *(Use cards numbered 1 to N, where N is the number of players).*
*   **Sector Cards:** Cards representing space sectors, forming the game grid. Each card features four resource/attribute values:
    *   Strategic (Red Icon/Value)
    *   Scientific (Green Icon/Value)
    *   Logistic (Blue Icon/Value)
    *   Economic (**Orange** Icon/Value)
    *   Keywords defining Sector Type (e.g., Biosphere, Warzone, Extraction, Observatory, Transit, Hazard, Unstable, Wasteland - relevant for Objectives).
    *   `back_value`: Exploration Cost paid in Scientific resources.
*   **Structure Tokens:** Tokens representing buildable structures. Each player receives a set of 5:
    *   Outpost (x2)
    *   Starlance (x1)
    *   Hypergate (x1)
    *   M-Brain (x1)
*   **Fleet Tokens:** 25 tokens per player color, representing generic fleets on the main game board before combat configuration.
*   **Homeworld Cards:** Unique starting Sector cards, one per player/civilization (visual reference shows 4 distinct arts, provides base income).
*   **Action Display + Marker:** A player board or card showing the 4 core actions. A marker tracks the last action taken, preventing immediate repetition (unless M-Brain allows).
*   **Fleet Roster Card:** A private player card showing the 5 Ship Types (Beam Frigate, Shield Cruiser, Artillery Platform, Drone Carrier, Fighter Squadron) potentially with rows/areas for tracking quantities or assigning damage/targeting. Used for Secret Fleet Configuration and Casualty/Targeting allocation.
*   **Fleet Roster Indicators:** 5 tokens per player, likely used on the Fleet Roster card during secret configuration.
*   **Storage Card:** A player board for tracking the four resource types (Logistic, Economic, Strategic, Scientific) using tracker tokens.
*   **Resource Trackers:** Tokens used on the Storage Card to mark current resource levels.
*   **Objective Cards:** Cards representing public goals providing VP when achieved (visual reference). *(Replaces original Galactic Senate Objectives/Rewards).* \[Placeholder: Define Objective setup and claiming mechanics].
*   **Combat Routine Cards:** \[Placeholder: Role TBD] Cards possibly used for advanced combat actions or tied to specific technologies/abilities (visual reference). *Current combat system does not explicitly use these. Decision needed: Keep or Cut?*
*   **Directive Cards:** \[Placeholder: Role TBD] Cards possibly representing ongoing laws, strategies, or special abilities, potentially affecting resource management or player actions (visual reference shows resource icons). *Current rules do not explicitly use these; may replace original Galactic Senate Laws/Sanctions. Decision needed: Define function (dots, etc.) or Cut?*
*   **Battle Mat:** A shared game tile used for resolving combat. Includes:
    *   5 Nodes arranged in a pentagon, representing the 5 Ship Types.
    *   Connecting Arrows between nodes indicating the Rock-Paper-Scissors (RPS) relationships and serving as "Attack Vector Areas" for dice placement. Each arrow area allows each player to place 1 die.
    *   *(Potentially)* Tracks for Initiative, Damage, Shields (use may be superseded by the "Vector Command" combat system).
*   **Master of the Order Token:** Passed to the player who acted last in the previous round, granting control over Order Card distribution.
*   **Command Point (CP) Tokens:** \[Placeholder: Component type TBD] Tokens or tracker needed for players to secretly allocate their 2 CP during combat (Maneuver Selection phase).
*   **Dice:** Standard six-sided dice (d6) for combat resolution.
*   **Damage/Targeting Markers:** \[Placeholder: Component type TBD] Tokens or method needed for players to secretly mark targeting intent/casualties on their Fleet Roster cards.

**4. SETUP**

1.  **Prepare Play Area:** Designate a central area for the space grid. Place the Battle Mat nearby.
2.  **Prepare Decks:** Shuffle the Sector Card deck (ensure consistency with `SectorCards.json` - check card count) and place it face down. Prepare the Order Card deck (Master card + numbered cards 1 to N for N players) and place it nearby. Shuffle Objective Cards \[and Directive Cards if used] and place them as indicated \[Placeholder: Define Objective/Directive setup].
3.  **Each Player Chooses Civilization:** Select or randomly assign a Civilization (see Civilizations section).
4.  **Gather Player Components:** Each player takes:
    *   Their chosen Civilization's unique Homeworld Card.
    *   25 Fleet Tokens of their color.
    *   5 Structure Tokens (2 Outposts, 1 Starlance, 1 Hypergate, 1 M-Brain).
    *   1 Fleet Roster Card and 5 Fleet Roster Indicators.
    *   1 Action Display Card and 1 Action Marker.
    *   1 Storage Card and 4 Resource Trackers.
    *   \[Placeholder: Define starting CP tokens/markers if physical].
    *   \[Placeholder: Define starting Combat Routine/Directive cards if applicable].
5.  **Place Homeworld:** Players place their Homeworld card in a corner of the designated grid area.
6.  **Initial Fleets:** Place 3 Fleet Tokens on your Homeworld sector.
7.  **Initial Resources:** Place all 4 Resource Trackers on the value **3** on your Storage Card, representing the initial resources provided by your Homeworld. *(See Glossary for standard resource order if needed).*
8.  **Initial Action Marker:** Place the Action Marker on a designated "start" position off the main actions on the Action Display Card.
9.  **Reveal Adjacent Sectors:** Each player draws the top 2 cards from the Sector Deck. **Pay Exploration Cost:** Calculate the total `back_value` of these 2 cards and pay this amount in **Green (Scientific)** resources. Place these cards face-up adjacent to your Homeworld sector in any orientation. *(If a player cannot afford the initial cost, perhaps allow them to draw replacements until they find affordable ones, or provide a small starting Scientific boost? Needs clarification for edge case).* Return any unused drawn cards to the top of the deck (or shuffle back in - TBD).

**5. CIVILIZATIONS**

Each Civilization provides unique passive abilities or advantages. *(See Appendix B for detailed lore)*.

*   **Stellar Architects:** Megastructures (Starlance, Hypergate, M-Brain) cost 1 fewer **Orange** (Economic) resource to build.
*   **Quantum Sentinels:** Gain 1 **Red** (Strategic) resource each time you initiate an Attack action.
*   **Void Navigators:** All your fleets inherently possess Pindown 1 (see Glossary/Move Action).
*   **Helix Cultivators:** \[TODO: Define ability - placeholder from PDF. Example based on Objectives: *Gain 1 VP immediately each time you spend 5 or more Scientific resources in a single action?*].

**6. GAME PLAY OVERVIEW**

Players take turns performing actions to explore the galaxy (placing Sector cards), expand their presence (moving fleets), exploit resources (gaining income), build fleets and structures, and engage in combat to control sectors. The goal is to accumulate the most Victory Points by the time the galaxy grid is filled.

**7. TURN STRUCTURE**

The game is played in rounds. Each round consists of the following phases:

*   **Phase 1: Determine Turn Order:**
    *   **First Round:** Shuffle the Order Card deck (Master + Player numbers). Each player draws one card and reveals it simultaneously. Lowest number goes first, then next lowest, etc. The player drawing the "Master" card goes last and holds it.
    *   **Subsequent Rounds:** The player who acted *last* in the previous round (holding the Master Card) takes the **Master of the Order Token**. They draw *two* Order Cards (numbered player cards) and reveal them. They then *propose* a distribution of all Order Cards (the two revealed + remaining face down player cards + the Master Card) among all players (including themselves).
        *   **Bribing:** Players may openly discuss and bribe the Master of Orders (immediately transferring resources shown on Storage Cards) to influence the distribution.
        *   **Final Distribution:** The Master of Orders makes the final decision, distributes the cards. Players simultaneously reveal their received Order Card. Lowest number goes first, etc. The player receiving the Master Card goes last. The Master of Orders token passes to the new last player at the end of the round.
*   **Phase 2: Player Actions:** Starting with the first player and proceeding in turn order, each player performs their turn:
    1.  **Gain Income:**
        *   **Gain Homeworld Income:** Gain 3 of each resource type (Logistic, Economic, Strategic, Scientific) from your Homeworld.
        *   **Gain Sector Income:** For each *other* Sector Card you control (have the most fleets present, or a structure if combat resulted in mutual destruction), gain resources exactly matching the **`values`** shown on that card (e.g., a card showing `{ "blue": 1, "orange": 2, "red": 0, "green": 0 }` provides 1 Blue and 2 **Orange** resources).
        *   **Apply M-Brain Bonus:** If you control an M-Brain structure, each controlled sector adjacent to it generates 1 additional resource of your choice (Blue, **Orange**, Red, or Green).
        *   **Update Storage Card:** Adjust all resource trackers on your Storage Card accordingly.
    2.  **Choose Action:** Select one of the 4 Core Actions (Explore, Move, Build, Attack) on your Action Display card *that is different from the action you took last turn*. Place your Action Marker on the chosen action.
        *   *M-Brain Exception:* If you control an M-Brain structure, you *may* choose the same action you took on your previous turn.
    3.  **Pay Cost:** Pay any resource costs associated with the chosen action by adjusting trackers on your Storage Card. *(Note: Explore action cost is paid during the action itself).*
    4.  **Perform Action:** Resolve the effects of the chosen action (see Core Actions).
*   **Phase 3: Round End:** After all players have completed their turn, the round ends. Check for game end conditions. If the game continues, pass the Master of the Order token to the player who just acted last (holding the Master Card), and begin the next round (Phase 1).

**8. CORE ACTIONS**

*   **A. EXPLORE ACTION**
    1.  **Declare Probes:** Send out up to 2 virtual Probes from sectors you control containing at least one fleet. Note the origin sector(s).
    2.  **(Optional) Scientific Boost (Draw More):** You may spend **Green** (Scientific) resources *now*. Each Scientific resource spent allows you to draw and reveal one additional Sector Card beyond the base 2 during the next step. Keep track of how many extra cards you intend to draw.
    3.  **Draw Cards:** Draw the top 2 (or more, if boosted) cards from the Sector Deck. Reveal them.
    4.  **Place Cards:** Place these revealed cards face-up onto the grid. Each card must be placed adjacent to one of the probe's origin sectors (or adjacent to an already placed card in a chain originating from a probe sector, following standard adjacency rules).
        *   *Hypergate Boost:* If a probe originates from a sector containing your Hypergate, it may place its revealed Sector Card up to **two** spaces away (following adjacent connections through explored sectors) from the origin sector, instead of only adjacent.
    5.  **Pay Exploration Cost:** Calculate the **total `back_value`** listed on all Sector Cards you just placed. Pay this amount in **Green (Scientific)** resources from your Storage Card. If you cannot afford the full cost, you cannot place the card(s) that push you over your limit; choose which newly revealed card(s) not to place and return them to the top of the Sector Deck in any order. *(Note: You must be able to pay for at least one card to perform the Explore action meaningfully).*
    6.  **Game End Trigger:** If drawing cards for this action empties the Sector Deck, the game ends immediately after successfully placing and paying for the final card(s). The player triggering this gains 5 VP.

*   **B. MOVE ACTION**
    *   **Effect:** Choose up to two sectors you control. Move any number of your Fleet Tokens from those origin sectors to any explored sectors within movement range. Movement does *not* trigger combat.
    *   **Base Movement Range:** Minimum 1 sector for all fleets.
    *   **Logistic Boost:** You may spend **Blue** (Logistic) resources. Each Logistic resource spent increases the movement range of the moving fleets by 1 sector for this action.
    *   **Hypergate Boost:** If a fleet's movement originates from a sector containing your Hypergate, its movement range is increased by 1 sector for this action (stacks with Logistic Boost).
    *   **Opponent Presence (Pindown):** Moving *through* a sector controlled by an opponent causes Pindown.
        *   *Pindown 0 (Default):* Each opponent fleet in the sector "pins" one of your moving fleets, stopping it in that sector.
        *   *Pindown 1 (Void Navigators / Tech?):* If your fleets have Pindown 1, only *one* of your fleets may continue moving unhindered through the pinning sector per opponent player present; the rest are stopped.
        *   *Pindown 2 (Advanced Tech?):* If your fleets have Pindown 2, *two* of your fleets may continue moving unhindered per opponent player present.
    *   **Arrival & Control:** Movement may end in a sector containing opponent fleets. After movement is complete, reassess control of both the origin sector(s) (if fleets left) and the destination sector(s). Control always belongs to the player with the most Fleet Tokens present in the sector. Ties generally result in no change of control, or the defender retains control if one was present. \[Placeholder: Confirm tie rule for sector control - Suggestion: Defender (player who controlled it before movement) retains control on a tie].

*   **C. BUILD ACTION**
    *   **Cost:** Pay the combined **Orange** (Economic) and **Blue** (Logistic) resource costs for all chosen build options from your Storage Card.
    *   **Build Options (Choose up to 2 in any combination):**
        1.  **Build Fleets:**
            *   Pay 1 **Orange** (Economic) resource per fleet.
            *   Take up to 2 Fleet Tokens from your supply and place them in your Homeworld sector.
            *   *Outpost Bonus:* For each sector you control containing your Outpost structure, you may build 1 additional Fleet Token (paying its **Orange** cost) in *that Outpost's sector*.
        2.  **Build Structures:**
            *   Pay the structure's cost (see table below).
            *   Place 1 structure token onto a controlled sector that does not already contain another structure token of yours (multiple players *can* build in the same sector if rules allow). Limit 1 of each structure type per player (except Outposts - max 2).
            *   *Benefits Active:* Structure benefits become active at the *start* of your next turn.
            *   **Structure Costs & Benefits:**
                | Structure  | **Blue** (Logistic) Cost | **Orange** (Economic) Cost | Benefit                                                                                                |
                | :--------- | :----------------------- | :------------------------- | :----------------------------------------------------------------------------------------------------- |
                | Outpost    | 1                        | 3                          | Allows building +1 fleet in its sector (see Build Fleets). Grants 2 VP at game end.                      |
                | Starlance  | 1                        | 4                          | Enables "Attack Structure" option (see Attack Action). Grants 2 VP at game end.                          |
                | Hypergate  | 2                        | 6                          | Boosts Explore range (+2 sectors). Boosts Move range (+1 sector). Grants 2 VP at game end.             |
                | M-Brain    | 4                        | 7                          | Grants +1 income/choice from adjacent sectors. Allows repeating actions. Grants 3 VP at game end. |

*   **D. ATTACK ACTION**
    *   **Effect:** Allows moving fleets into an opponent-controlled sector specifically to initiate combat. Choose up to 2 of the following options:
        1.  **Attack Fleets:**
            *   Declare intent to attack an adjacent sector containing opponent fleets. Choose up to 2 controlled sectors containing your fleets as origins for the attack.
            *   Pay 1 **Blue** (Logistic) resource for *each sector boundary* crossed by the attacking fleet(s) to reach the target contested sector. (Min cost 1).
            *   Move any number of Fleet Tokens from the origin sector(s) into the contested sector.
            *   **Trigger Combat:** This immediately initiates the Combat sequence (see Combat Rules).
            *   *Hypergate Attack:* Fleets originating from a sector with your Hypergate can attack any sector connected by a continuous line of explored sectors. Pay the **Blue** (Logistic) cost for the path length (number of boundaries crossed). Attack is not allowed if unexplored sectors break the path between Hypergate sector and target.
        2.  **Attack Structure:**
            *   Requires you control a Starlance structure. Choose one Starlance you control.
            *   Pay 2 **Red** (Strategic) resources and 2 **Blue** (Logistic) resources.
            *   Choose an adjacent sector containing *any* structure (yours or opponent's).
            *   Remove the structure token from that sector and return it to its owner's supply. It can be rebuilt later. (This option is unavailable if you control no Starlances).

**9. COMBAT RULES ("Vector Command")**

Combat resolves conflicts when fleets from different players occupy the same sector after an Attack Action.

*   **Combat Initiation:** Triggered by the Attack Action. Note the Attacker (the player whose turn it is) and Defender(s) (any other players with fleets in the sector).
*   **Combat Sequence:** Regardless of the number of players involved (2 or more), use the **Combat Sequence** described below (formerly Multi-Way Combat).

---

**9.A. Combat Sequence**

1.  **Initiation:** Combat begins when fleets from 2 or more players occupy the same sector following an Attack Action. Identify the Attacker (current player) and all Defenders.
2.  **Fleet Configuration (Secret & Simultaneous):** All involved players secretly assign their fleet tokens present in the combat sector to ship type nodes on their Fleet Roster. Reveal simultaneously and place corresponding tokens/indicators on the Battle Mat nodes.
3.  **Declare Attack Vectors & Place Dice (Open & Simultaneous):** Each player may place 1 die into any valid Attack Vector Area (RPS arrow) originating from one of their ship types and pointing towards an opponent ship type they counter via RPS. A player can target *any* opponent(s) they have valid vectors against. A player may place multiple dice if they have multiple valid outgoing vectors, but still only 1 die *per player* is allowed in a single Attack Vector Area (arrow).
4.  **Gain & Allocate Command Points (Secret & Simultaneous):** Each player involved in the combat receives 2 CP. Secretly allocate CP to one or more of the following options, then reveal simultaneously:
    *   `Boost Attack [1CP]`: Roll 1 extra attack die this round (add to one chosen vector pool before rolling).
    *   `Boost Defense [1CP]`: Choose *one opponent*. Force that opponent to re-roll 1 successful hit die against you this round. Announce the targeted opponent when revealing CP. (If only one opponent exists, the choice is automatic).
    *   `Prepare Reshape [2CP]`: If one of your ships survives this round, you may change its type after casualties are removed.
5.  **Roll Dice Pools (Simultaneous):** All players roll all dice they placed (plus any Boost Attack dice). Keep results associated with the roller. A roll of 5+ is a potential hit.
6.  **Apply Forced Re-rolls:** For each player targeted by an opponent's Boost Defense, the attacker must re-roll one successful hit die (defender's choice which die if multiple hits were scored).
7.  **Determine Final Hits:** Each player counts their own total successful hits (5+) after re-rolls.
8.  **Secretly Allocate Hits to Target Types (Roster Method):** Based on your own Final Hits, secretly mark on your Fleet Roster *which of the opponent's ship types* you intend to target with your hits. You can distribute hits among valid target types as you wish. (If multiple opponents exist, you allocate hits without specifying *which* opponent's ship type, just the type itself).
9.  **Simultaneous Roster Reveal:** All players reveal their targeting allocations by ship type (e.g., "I target Shield Cruisers with 2 hits and Fighters with 1 hit").
10. **Resolve Targeting & Casualties (Ordered Assignment):** Determine resolution order based on player Turn Order among the combatants (starting with the Attacker, then proceed in normal turn order). In order, the active assigner assigns their hits one by one, based on their Roster target types, to specific *available* opponent ship tokens of that type on the Battle Mat.
    *   **Choosing Targets:** If only one opponent exists, assign hits to their available ships of the targeted type.
    *   **Choosing Targets (Multiple Opponents):** If multiple opponents have ships of the targeted type, **the assigner chooses which opponent's ship to hit** for each allocated hit.
    *   Remove casualties immediately. Wasted hits if no targets of the chosen type remain among any valid opponents. Continue until all players have assigned all their hits.
11. **Execute Prepared Reshapes:** Players who allocated 2 CP to Prepare Reshape (Step 4) and still have at least one fleet token remaining *may* now choose one of their surviving ship tokens on the Battle Mat and move it to an adjacent node (following an RPS arrow) representing a different ship type. Update the Roster if necessary.
12. **End of Round Check:** Check remaining fleets. If more than one player still has fleets in the sector, start a New Combat Round (Return to Step 3: Place Dice, gain 2 fresh CP). If only one player or zero players remain, Combat Ends.
13. **Post-Combat Control:** The single surviving player takes/retains control of the sector. If mutual destruction (zero survivors), the sector becomes uncontrolled, **unless** one of the players involved was the original Defender *and* had a structure present, in which case that player retains control.

---

**9.B. The Battle Mat** *(Formerly 9.C)*

*   **Node Representation:** The 5 nodes represent the 5 Ship Types. Players place configured fleet tokens/indicators on these nodes during combat.
*   **Arrows Indication (RPS):** Arrows connecting nodes show which ship type "beats" or "counters" which target ship types. These define the valid Attack Vectors.
*   **Attack Vector Areas:** The lines/arrows themselves serve as areas where players place their dice when attacking along that vector (i.e., when attacking a ship type countered by the originating ship type). Each area accommodates 1 die per player attacking along it per combat round.
---
**10. FLEETS & SHIP TYPES (RPS Details)**

Fleets are represented by tokens, configured into specific ship types during combat. Each type has strengths and weaknesses defined by the Rock-Paper-Scissors (RPS) system, which determines valid attack vectors.

*   **RPS Rules & Descriptions:**
    *   **Beam Frigate:**
        *   *Counters:* Shield Cruiser, Drone Carrier
        *   *Countered By:* Artillery Platform, Fighter Squadron
        *   *Description:* Uses precise energy beams effective against shields and drone swarms, but vulnerable to long-range artillery and agile fighters.
    *   **Shield Cruiser:**
        *   *Counters:* Fighter Squadron, Artillery Platform
        *   *Countered By:* Beam Frigate, Drone Carrier
        *   *Description:* Heavy shields absorb fighter attacks and mitigate artillery impact, but can be penetrated by focused beams or overwhelmed by coordinated drone attacks.
    *   **Artillery Platform:**
        *   *Counters:* Drone Carrier, Beam Frigate
        *   *Countered By:* Shield Cruiser, Fighter Squadron
        *   *Description:* Engages from extreme range, effective against frigates and drone swarms, but vulnerable to shielded cruisers absorbing hits and fighters closing distance.
    *   **Drone Carrier:**
        *   *Counters:* Fighter Squadron, Shield Cruiser
        *   *Countered By:* Beam Frigate, Artillery Platform
        *   *Description:* Overwhelms fighters with numbers and exploits shield gaps, but vulnerable to anti-swarm beams and area-effect artillery.
    *   **Fighter Squadron:**
        *   *Counters:* Beam Frigate, Artillery Platform
        *   *Countered By:* Shield Cruiser, Drone Carrier
        *   *Description:* Agile craft dodge beams and evade slow artillery to counter-attack, but struggle against heavy shields and drone swarms.

**11. STRUCTURES**

Structures provide ongoing benefits and VP. See Build Action for costs and placement rules.

*   **Outpost:** Enables fleet building in its sector, worth 2 VP.
*   **Starlance:** Enables the Attack Structure action, worth 2 VP.
*   **Hypergate:** Improves Explore and Move Action ranges, worth 2 VP.
*   **M-Brain:** Improves income generation and allows action repetition, worth 3 VP.
*   **(Interaction with Combat):** A structure allows a defender to retain control of a sector even if all defending fleets are destroyed in mutual annihilation combat in that sector. \[Placeholder: Do structures provide any defensive bonuses during combat? e.g., absorb 1 hit? - Suggestion: No direct combat bonus to keep things cleaner, their survival benefit is indirect].

**12. END OF GAME**

The game ends **immediately** when one of the following conditions is met:

1.  **Grid Completion:** The last Sector Card is drawn, placed, and successfully paid for during an Explore action. The exploring player gains 5 bonus VP.
2.  **Objective Completion:** A player successfully claims the final available Victory Point slot on any public Objective Card during their turn. *(The action that allowed the claim is completed, then the game ends immediately before proceeding further).*

Proceed immediately to Scoring.

**13. SCORING**

Players calculate their final Victory Point totals:

1.  **Grid Completion Bonus:** +5 VP for the player who placed the last Sector card.
2.  **Controlled Sectors:** +1 VP for each sector controlled at game end (must have at least one fleet present, or be the defender with a structure in case of mutual destruction).
3.  **Sectors with Structure Tokens:** Additional VP for sectors containing your structures at game end:
    *   Outpost: +2 VP per token.
    *   M-Brain: +3 VP per token.
    *   Hypergate: +2 VP per token.
    *   Starlance: +2 VP per token.
4.  **Fleet Tokens:** +1 VP for every 3 of your Fleet Tokens remaining on the game grid (in any sector). *(Adjusted from 1:1 for balance - needs testing)*.
5.  **Orange (Economic) Resources:** +1 VP for every 1 **Orange** resource you have remaining on your Storage Card.
6.  **Special Goals (Civilization Specific):**
    *   *Stellar Architects:* +3 VP for each Megastructure (Starlance, Hypergate, M-Brain) you have on the grid at game end.
    *   *Quantum Sentinels:* +1 VP for every combat round won \[Placeholder: Define "combat round won" - Suggestion: Inflicting more casualties than you took in a single round? Or perhaps +3VP per *entire combat* won where you were the sole survivor? Simpler might be: +1 VP per enemy fleet destroyed during combats you initiated?].
    *   *Void Navigators:* +1 VP for each explored sector on the grid at game end that is *not* adjacent to your Homeworld.
    *   *Helix Cultivators:* +5 VP if you have 15 or more **Green** (Scientific) resources on your Storage Card at the end of the game. *(Changed from Strategic Red to Green Scientific based on theme suggestion, value adjusted)*.
7.  **Objective Cards:** Award VP indicated on any achieved public \[or private?] Objective Cards. \[Placeholder: Detail Objective Card mechanics if used - how are they claimed? Public/Private? Number available?].

The player with the most total VP wins. Ties are friendly \[Placeholder: Define tiebreaker rule if needed - Suggestion: Most remaining non-Orange resources (Blue+Red+Green), then most fleets].

**14. GLOSSARY**

*(Based on Milkomeda PDF Glossary + our terms)*

*   **Action Display:** Player board showing core actions, used with Action Marker.
*   **Action Marker:** Token used on Action Display to track last action, prevents repeats (unless M-Brain).
*   **Attack Action:** Core action to move fleets into an opponent's sector to initiate Combat. Can also target structures via Starlance.
*   **Attack Vector Area:** The connecting lines/arrows between Ship Type nodes on the Battle Mat, representing valid RPS attacks. Dice are placed here.
*   **Battle Mat:** Shared tile where combat is resolved using ship tokens/indicators on nodes.
*   **Build Action:** Core action to spend resources to build Fleets or Structures.
*   **Command Points (CP):** Resource (2 per player per combat round) allocated secretly for tactical benefits (Boost Attack/Defense, Prepare Reshape).
*   **Combat:** The process triggered by the Attack Action, resolved using the "Vector Command" system.
*   **Controlled Sector:** A sector where a player has the most Fleet Tokens present, or where the defender retains control via a structure after mutual destruction combat in that sector. Check ties based on \[Placeholder: Define tie rule - Suggestion: Defender retains control].
*   **Economic (Resource): Orange** resource, primarily used for building fleets/structures via the Build Action, worth VP at game end.
*   **Explore Action:** Core action to draw, place, and pay the Scientific cost for new Sector cards onto the grid.
*   **Fleet Configuration:** The secret, simultaneous step at the start of combat where players assign their generic Fleet Tokens to specific Ship Type nodes on the Battle Mat via their Fleet Roster.
*   **Fleet Roster Card:** Private player card showing the 5 ship types, used for secret Fleet Configuration and secret targeting/casualty allocation.
*   **Fleet Tokens:** Generic physical tokens representing a player's fleets on the main game board. Their specific Ship Type is determined during Fleet Configuration in combat.
*   **Formation Advantage:** (1v1 Combat Only) Tiebreaker advantage gained by having more RPS counters during Fleet Configuration. Breaks ties in Final Hit comparison if hits are equal.
*   **Homeworld:** Unique starting Sector card for each player, providing base income.
*   **Hypergate:** Structure improving Explore and Move ranges.
*   **Logistic (Resource): Blue** resource, used to boost Move range and pay for Attack movement/Structure Attack.
*   **M-Brain:** Structure providing income bonus and allowing action repetition.
*   **Maneuver Selection:** Phase in combat where players secretly allocate Command Points.
*   **Master of the Order Token:** Token granting control over turn order card distribution. Held by the player who goes last.
*   **Move Action:** Core action to move fleets between explored sectors without initiating combat.
*   **Node:** A point on the Battle Mat representing one of the 5 Ship Types.
*   **Order Cards:** Cards determining player turn order each round (Numbered player cards + Master Card).
*   **Outpost:** Structure allowing localized fleet building.
*   **Pindown:** Mechanic restricting fleet movement through enemy-controlled sectors. Values (0, 1, 2) determine how many fleets can pass unhindered per opponent player.
*   **Prepare Reshape:** CP allocation option allowing a ship to change type after combat resolution.
*   **Reshape:** Action (enabled by Prepare Reshape CP) allowing a surviving ship token to move to an adjacent node on the Battle Mat (following RPS arrows) after casualties are removed.
*   **Rock-Paper-Scissors (RPS):** System defining which Ship Types counter others, determining valid Attack Vectors.
*   **Scientific (Resource): Green** resource, used to boost the number of cards drawn during the Explore action **and required to pay the Exploration Cost (`back_value`) of newly placed Sector Cards.** Associated with Helix Cultivator goal.
*   **Sector Card:** Card representing a region of space, forming the map grid. Provides income based on `values`, has keywords for objectives, and a `back_value` exploration cost.
*   **Standard Resource Order:** For reference in component descriptions (like Homeworld values): 1. Blue (Logistic), 2. Orange (Economic), 3. Red (Strategic), 4. Green (Scientific).
*   **Starlance:** Structure enabling the Attack Structure action.
*   **Storage Card:** Player board for tracking resource levels.
*   **Strategic (Resource): Red** resource, used for Structure Attack via Starlance, gained by Quantum Sentinels when attacking.
*   **Structure Tokens:** Physical tokens representing Outposts, Starlances, Hypergates, M-Brains.
*   **Targeting Markers:** Conceptual markers placed secretly on the Fleet Roster to indicate which opponent ship types are being targeted by hits.


---

**15. APPENDIX A: HISTORICAL PROTOCOL FILE 147-XC (LORE)**

*(Include the text from MilkomedaLore.md here)*

---

**16. APPENDIX B: CIVILIZATION DETAILS (LORE)**

*(Include relevant lore snippets for each Civilization here, connecting to their abilities)*

---