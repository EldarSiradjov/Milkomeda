Im a Board game designer: and These are my Rules for a game called Milkomeda. It is work in progress and i want you to help me
Okay, understood. You want a complete dump of the *Milkomeda* rules as they stand based on *all* our discussions, including lore, component descriptions derived from visuals, the detailed combat system ("Vector Command" for both 1v1 and multi-way), thematic names, and outstanding placeholders. This will be a long and detailed document to serve as your consolidated baseline.

---

**MILKOMEDA - Rulebook Draft (Consolidated)**

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

**Milkomeda** is a strategic board game where players aim to dominate a grid of space sectors, deploying fleets and utilizing resources to engage in tactical battles and achieve dominance before the galaxy is fully explored. Victory is determined by amassing the most Victory Points through sector control, fleet management, economic strength, structure placement, and achieving specific goals.

*(See Appendix A for the full text of Historical Protocol File 147-XC detailing the lore background of the Aetharan Ascendancy and their exodus into The Caelum Void).*

**2. GAME OBJECTIVE**

Be the player with the most Victory Points (VP) at the end of the game. The game ends when the last Sector Card is explored and placed onto the grid, or potentially when certain objectives are claimed [Placeholder: Confirm if objective claims can end the game].

**3. COMPONENTS**

*   **Order Cards:** A deck determining turn order, numbered 1-X for players and including a "Master" card (visual reference).
*   **Sector Cards:** Cards representing space sectors, forming the game grid. Each card features four resource/attribute values:
    *   Strategic (Red Icon/Value)
    *   Scientific (Green Icon/Value)
    *   Logistic (Blue Icon/Value)
    *   Economic (Yellow Icon/Value)
    *   *(Assumption: Sector Cards also list a Sector Type - e.g., Biosphere, Warzone, Extraction, etc. - relevant for Objectives, though not explicitly listed in PDF component list).*
*   **Structure Tokens:** Tokens representing buildable structures. Each player receives a set of 5:
    *   Outpost (x2)
    *   Starlance (x1)
    *   Hypergate (x1)
    *   M-Brain (x1)
*   **Fleet Tokens:** 25 tokens per player color, representing generic fleets on the main game board before combat configuration.
*   **Homeworld Cards:** Unique starting Sector cards, one per player/civilization (visual reference shows 4 distinct arts).
*   **Action Display + Marker:** A player board or card showing the 4 core actions. A marker tracks the last action taken, preventing immediate repetition (unless M-Brain allows).
*   **Fleet Roster Card:** A private player card showing the 5 Ship Types (Beam Frigate, Shield Cruiser, Artillery Platform, Drone Carrier, Fighter Squadron) potentially with rows/areas for tracking quantities or assigning damage/targeting. Used for Secret Fleet Configuration and Casualty/Targeting allocation.
*   **Fleet Roster Indicators:** 5 tokens per player, likely used on the Fleet Roster card during secret configuration.
*   **Storage Card:** A player board for tracking the four resource types (Logistic, Economic, Strategic, Scientific) using tracker tokens.
*   **Resource Trackers:** Tokens used on the Storage Card to mark current resource levels.
*   **Objective Cards:** Cards representing public goals providing VP when achieved (visual reference). *(Replaces original Galactic Senate Objectives/Rewards).*
*   **Combat Routine Cards:** [Placeholder: Role TBD] Cards possibly used for advanced combat actions or tied to specific technologies/abilities (visual reference). *Current combat system does not explicitly use these.*
*   **Directive Cards:** [Placeholder: Role TBD] Cards possibly representing ongoing laws, strategies, or special abilities, potentially affecting resource management or player actions (visual reference shows resource icons). *Current rules do not explicitly use these; may replace original Galactic Senate Laws/Sanctions.*
*   **Battle Mat:** A shared game tile used for resolving combat. Includes:
    *   5 Nodes arranged in a pentagon, representing the 5 Ship Types.
    *   Connecting Arrows between nodes indicating the Rock-Paper-Scissors (RPS) relationships and serving as "Attack Vector Areas" for dice placement. Each arrow area allows each player to place 1 die.
    *   *(Potentially)* Tracks for Initiative, Damage, Shields (as shown in early Battle Mat diagram), although their use may be superseded by the "Vector Command" combat system.
*   **Master of the Order Token:** Passed to the player who acted last in the previous round, granting control over Order Card distribution.
*   **Command Point (CP) Tokens:** [Placeholder: Component type TBD] Tokens or tracker needed for players to secretly allocate their 2 CP during combat (Maneuver Selection phase).
*   **Dice:** Standard six-sided dice (d6) for combat resolution.
*   **Damage/Targeting Markers:** [Placeholder: Component type TBD] Tokens or method needed for players to secretly mark targeting intent/casualties on their Fleet Roster cards.

**4. SETUP**

1.  **Prepare Play Area:** Designate a central area for the space grid. Place the Battle Mat nearby.
2.  **Prepare Decks:** Shuffle the Sector Card deck (50 cards) and place it face down. Shuffle the Order Card deck and place it nearby. Shuffle Objective Cards [and Directive Cards if used] and place them as indicated [Placeholder: Define Objective/Directive setup].
3.  **Each Player Chooses Civilization:** Select or randomly assign a Civilization (see Civilizations section).
4.  **Gather Player Components:** Each player takes:
    *   Their chosen Civilization's unique Homeworld Card.
    *   25 Fleet Tokens of their color.
    *   5 Structure Tokens (2 Outposts, 1 Starlance, 1 Hypergate, 1 M-Brain).
    *   1 Fleet Roster Card and 5 Fleet Roster Indicators.
    *   1 Action Display Card and 1 Action Marker.
    *   1 Storage Card and 4 Resource Trackers.
    *   [Placeholder: Define starting CP tokens/markers if physical].
    *   [Placeholder: Define starting Combat Routine/Directive cards if applicable].
5.  **Place Homeworld:** Players place their Homeworld card in a corner of the designated grid area.
6.  **Initial Fleets:** Place 3 Fleet Tokens on your Homeworld sector.
7.  **Initial Resources:** Place all 4 Resource Trackers on the starting value [Placeholder: Define starting value, e.g., 2 or 3] on the Storage Card.
8.  **Initial Action Marker:** Place the Action Marker on a designated "start" position off the main actions on the Action Display Card.
9.  **Reveal Adjacent Sectors:** Each player draws the top 2 cards from the Sector Deck and places them face-up adjacent to their Homeworld sector in any orientation. Return any unused drawn cards to the top of the deck (or shuffle back in - TBD).

**5. CIVILIZATIONS**

Each Civilization provides unique passive abilities or advantages. *(See Appendix B for detailed lore)*.

*   **Stellar Architects:** Megastructures (Starlance, Hypergate, M-Brain) cost 1 fewer Economic resource to build.
*   **Quantum Sentinels:** Gain 1 Strategic resource each time you initiate an Attack action.
*   **Void Navigators:** All your fleets inherently possess Pindown 1 (see Glossary/Move Action).
*   **Helix Cultivators:** [TODO: Define ability - placeholder from PDF].

**6. GAME PLAY OVERVIEW**

Players take turns performing actions to explore the galaxy (placing Sector cards), expand their presence (moving fleets), exploit resources (gaining income), build fleets and structures, and engage in combat to control sectors. The goal is to accumulate the most Victory Points by the time the galaxy grid is filled.

**7. TURN STRUCTURE**

The game is played in rounds. Each round consists of the following phases:

*   **Phase 1: Determine Turn Order:**
    *   **First Round:** Shuffle the Order Card deck. Each player draws one card and reveals it simultaneously. Lowest number goes first, then next lowest, etc.
    *   **Subsequent Rounds:** The player who acted *last* in the previous round takes the **Master of the Order Token**. They draw *two* Order Cards and reveal them. They then *propose* a distribution of all Order Cards (the two revealed + remaining face down) among all players.
        *   **Bribing:** Players may openly discuss and bribe the Master of Orders (immediately transferring resources shown on Storage Cards) to influence the distribution.
        *   **Final Distribution:** The Master of Orders makes the final decision, distributes the cards. Players simultaneously reveal their received Order Card. Lowest number goes first, etc. The Master of Orders token passes to the new last player at the end of the round.
*   **Phase 2: Player Actions:** Starting with the first player and proceeding in turn order, each player performs their turn:
    1.  **Gain Income:**
        *   Mark income from controlled sectors: Gain resources indicated on Sector cards you control (adjust trackers on Storage Card). [Placeholder: Clarify if Sector cards show specific resource icons/values or just grant generic income].
        *   M-Brain Bonus: If you control an M-Brain structure, each controlled sector adjacent to it generates 1 additional resource of your choice.
    2.  **Choose Action:** Select one of the 4 Core Actions (Explore, Move, Build, Attack) on your Action Display card *that is different from the action you took last turn*. Place your Action Marker on the chosen action.
        *   *M-Brain Exception:* If you control an M-Brain structure, you *may* choose the same action you took on your previous turn.
    3.  **Pay Cost:** Pay any resource costs associated with the chosen action by adjusting trackers on your Storage Card.
    4.  **Perform Action:** Resolve the effects of the chosen action (see Core Actions).
*   **Phase 3: Round End:** After all players have completed their turn, the round ends. Check for game end conditions. If the game continues, pass the Master of the Order token to the player who just acted last, and begin the next round (Phase 1).

**8. CORE ACTIONS**

*   **A. EXPLORE ACTION**
    *   **Effect:** Send out up to 2 virtual Probes from sectors you control containing at least one fleet. Draw the top 2 cards from the Sector Deck. Place these cards face-up onto the grid, adjacent to any sector(s) you control with fleets.
    *   **Scientific Boost:** You may spend Scientific resources *before* drawing cards. Each Scientific resource spent allows you to draw and place one additional Sector Card (e.g., spend 1 Scientific -> draw & place 3 cards total).
    *   **Hypergate Boost:** If a probe originates from a sector containing your Hypergate, it can place its revealed Sector Card up to two spaces away (following adjacent connections) from the origin sector, instead of only adjacent.
    *   **Game End Trigger:** If drawing cards for this action empties the Sector Deck, the game ends immediately after placing the final card(s). The player triggering this gains 5 VP.
*   **B. MOVE ACTION**
    *   **Effect:** Choose up to two sectors you control. Move any number of your Fleet Tokens from those origin sectors to any explored sectors within movement range. Movement does *not* trigger combat.
    *   **Base Movement Range:** Minimum 1 sector for all fleets.
    *   **Logistic Boost:** You may spend Logistic resources. Each Logistic resource spent increases the movement range of the moving fleets by 1 sector for this action.
    *   **Hypergate Boost:** If a fleet's movement originates from a sector containing your Hypergate, its movement range is increased by 1 sector for this action.
    *   **Opponent Presence (Pindown):** Moving *through* a sector controlled by an opponent causes Pindown.
        *   *Pindown 0 (Default):* Each opponent fleet in the sector "pins" one of your moving fleets, stopping it in that sector.
        *   *Pindown 1 (Void Navigators / Tech?):* If your fleets have Pindown 1, only *one* of your fleets may continue moving unhindered through the pinning sector; the rest are stopped.
        *   *Pindown 2 (Advanced Tech?):* If your fleets have Pindown 2, *two* of your fleets may continue moving unhindered.
    *   **Arrival & Control:** Movement may end in a sector containing opponent fleets. After movement is complete, reassess control of both the origin sector(s) (if fleets left) and the destination sector(s). Control always belongs to the player with the most Fleet Tokens present in the sector. Ties generally result in no change of control [Placeholder: Confirm tie rule for sector control].
*   **C. BUILD ACTION**
    *   **Cost:** Pay the combined Economic and Logistic resource costs for all chosen build options from your Storage Card.
    *   **Build Options (Choose up to 2 in any combination):**
        1.  **Build Fleets:**
            *   Pay 1 Economic resource per fleet.
            *   Take up to 2 Fleet Tokens from your supply and place them in your Homeworld sector.
            *   *Outpost Bonus:* For each sector you control containing your Outpost structure, you may build 1 additional Fleet Token (paying its cost) in *that Outpost's sector*.
        2.  **Build Structures:**
            *   Pay the structure's cost (see table below).
            *   Place 1 structure token onto a controlled sector that does not already contain another structure token (exception: Outposts?). Limit 1 of each structure type per player (except Outposts - max 2).
            *   *Benefits Active:* Structure benefits become active at the *start* of your next turn.
            *   **Structure Costs & Benefits:**
                | Structure  | Logistic Cost | Economic Cost | Benefit                                                                                                |
                | :--------- | :------------ | :------------ | :----------------------------------------------------------------------------------------------------- |
                | Outpost    | 1             | 3             | Allows building +1 fleet in its sector (see Build Fleets). Grants 2 VP at game end.                      |
                | Starlance  | 1             | 4             | Enables "Attack Structure" option (see Attack Action). Grants 2 VP at game end.                          |
                | Hypergate  | 2             | 6             | Boosts Explore range (+2 sectors). Boosts Move range (+1 sector). Grants 2 VP at game end.             |
                | M-Brain    | 4             | 7             | Grants +1 income/choice from adjacent sectors. Allows repeating actions. Grants 3 VP at game end. |
*   **D. ATTACK ACTION**
    *   **Effect:** Allows moving fleets into an opponent-controlled sector specifically to initiate combat. Choose up to 2 of the following options:
        1.  **Attack Fleets:**
            *   Declare intent to attack an adjacent sector containing opponent fleets. Choose up to 2 controlled sectors as origins for the attack.
            *   Pay 1 Logistic resource for *each sector* the attacking fleet(s) move through to reach the target contested sector.
            *   Move any number of Fleet Tokens from the origin sector(s) into the contested sector.
            *   **Trigger Combat:** This immediately initiates the Combat sequence (see Combat Rules).
            *   *Hypergate Attack:* Fleets can attack through a Hypergate they control, following a continuous line of explored sectors to the target. Pay Logistic cost for path length. Attack is not allowed if unexplored sectors break the path between Hypergate sector and target.
        2.  **Attack Structure:**
            *   Requires you control a Starlance structure. Choose one Starlance you control.
            *   Pay 2 Strategic resources and 2 Logistic resources.
            *   Choose an adjacent sector containing *any* structure (yours or opponent's).
            *   Remove the structure token from that sector and return it to its owner's supply. It can be rebuilt later. (This option is unavailable if you control no Starlances).

**9. COMBAT RULES ("Vector Command")**

Combat resolves conflicts when fleets from different players occupy the same sector after an Attack Action.

*   **Combat Initiation:** Triggered by the Attack Action. Note the Attacker and Defender(s).
*   **Combat Type:**
    *   If exactly 2 players are involved, use the **1v1 Combat Sequence**.
    *   If 3 or more players are involved, use the **Multi-Way Combat Sequence**.

---

**9.A. 1v1 Combat Sequence**

1.  **Initiation:** Attacker moves fleets into Defender's sector.
2.  **Fleet Configuration (Secret & Simultaneous):** Both players secretly assign their fleet tokens to ship type nodes on their Fleet Roster. Reveal simultaneously and place tokens on the Battle Mat.
3.  **Determine Formation Advantage:** Compare revealed fleets based on RPS counters. Player with more counter points gains **Formation Advantage** (tiebreaker).
4.  **Maneuver Selection (Secret & Simultaneous):** Gain 2 CP. Secretly allocate to `Boost Attack [1CP]`, `Boost Defense [1CP]`, `Prepare Reshape [2CP]`. Reveal allocations.
5.  **Roll Dice & Resolve Hits (Simultaneous):** Place 1 die per valid outgoing RPS vector. Roll placed dice + Boost Attack dice. Determine hits (e.g., 5+). Apply opponent's Boost Defense re-rolls. Determine **Final Hits**. Apply Formation Advantage tiebreaker (if hits tied, player without advantage reduces hits by 1).
6.  **Secretly Allocate Hits to Target Types (Roster Method):** Based on own Final Hits, secretly mark on Roster which *opponent ship types* to target.
7.  **Simultaneous Roster Reveal:** Reveal targeting allocations by type.
8.  **Resolve Targeting & Casualties (Ordered Assignment):** Use Turn Order for resolution priority. Active Assigner assigns their hits one by one (based on Roster target types) to specific *available* opponent ship tokens, removing targets immediately. Free choice among opponent's ships of targeted type. Wasted hits if no targets remain. Continue until both players resolve hits.
9.  **Execute Prepared Reshapes:** Players who paid 2 CP (Step 4) and survived Step 8 now Reshape one ship along valid RPS arrows.
10. **End of Round Check:** If both players have fleets, start New Round (Return to Step 4: Maneuver Selection, gain 2 CP). If 1 or 0 players remain, Combat Ends.
11. **Post-Combat Control:** Victor takes control; mutual destruction -> uncontrolled unless defender structure.

---

**9.B. Multi-Way (>2 Player) Combat Sequence**

1.  **Initiation:** Combat begins when >2 players have fleets in the same sector.
2.  **Fleet Configuration (Secret & Simultaneous):** All involved players secretly assign fleet tokens to types via Roster. Reveal simultaneously and place tokens on Battle Mat.
3.  **Declare Attack Vectors & Place Dice (Open & Simultaneous):** Each player places 1 die into each valid Attack Vector Area (RPS line) from their ships towards *any* opponent ships. (Max 1 die per player per vector area).
4.  **Gain & Allocate Command Points (Secret & Simultaneous):** Each player receives 2 CP. Secretly allocate to `Boost Attack [1CP]`, `Boost Defense [1CP]`, `Prepare Reshape [2CP]`. Reveal allocations. Clarify Boost Defense target(s).
5.  **Roll Dice Pools (Simultaneous):** Roll all placed dice + Boost Attack dice. Keep results associated with roller. Count own total successful hits (5+).
6.  **Apply Forced Re-rolls:** Resolve Boost Defense choices. Determine **Final Hits** for each player. *(Note: No Formation Advantage / Tiebreaker applied in multi-way).*
7.  **Secretly Allocate Hits to Target Types (Roster Method):** Based on own Final Hits, secretly mark on Roster which *opponent ship types* to target.
8.  **Simultaneous Roster Reveal:** Reveal targeting allocations by type.
9.  **Resolve Targeting & Casualties (Ordered Assignment):** Determine resolution order (e.g., Turn Order among combatants). In order, Active Assigner assigns their hits one by one (based on Roster target types) to specific *available* opponent ship tokens, removing targets immediately. Free choice of opponent per hit if multiple have the target type. Wasted hits if no targets remain. Continue until all players have assigned hits.
10. **Execute Prepared Reshapes:** Players who paid 2 CP (Step 4) and survived Step 9 now Reshape one ship along valid RPS arrows.
11. **End of Round Check:** Check survivors. If >1 player remains, start New Round (Return to Step 3: Place Dice, gain 2 fresh CP). If 1 or 0 remain, Combat Ends.
12. **Post-Combat Control:** Victor takes control; mutual destruction -> uncontrolled unless defender structure.

---

**9.C. The Battle Mat**

*   **Node Representation:** The 5 nodes represent the 5 Ship Types. Players place configured fleet tokens on these nodes.
*   **Arrows Indication (RPS):** Arrows connecting nodes show which ship type "beats" or "counters" which target ship types, determining valid Attack Vectors for placing dice.
*   **Attack Vector Areas:** The lines/arrows themselves serve as areas where players place their dice when attacking along that vector. Each area accommodates 1 die per player attacking along it.
*   **Tracks:** [Placeholder: Confirm relevance] Early designs showed tracks for Initiative, Damage, and Shields. Their function may be altered or replaced by the CP system and hit resolution. Damage/Shields might be represented by hits/HP implicitly (1 hit = 1 ship removal). Initiative is less relevant with simultaneous rolls but used for resolving Step 9 targeting order in multi-way.

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
*   *(Interaction with Combat):* A structure allows a defender to retain control of a sector even if all defending fleets are destroyed in mutual annihilation. [Placeholder: Do structures provide any defensive bonuses during combat? e.g., absorb 1 hit?].

**12. END OF GAME**

The game ends immediately when one of the following occurs:

1.  **Grid Completion:** The last Sector Card is drawn and placed during an Explore action. The exploring player gains 5 bonus VP.
2.  **[Placeholder: Objective Claim Trigger?]** Confirm if claiming the last slot on a public Objective track also triggers the game end.

Proceed immediately to Scoring.

**13. SCORING**

Players calculate their final Victory Point totals:

1.  **Grid Completion Bonus:** +5 VP for the player who placed the last Sector card.
2.  **Controlled Sectors:** +1 VP for each sector controlled at game end (must have at least one fleet present, or be the defender with a structure in case of mutual destruction).
3.  **Sectors with Structure Tokens:** Additional VP for sectors containing your structures:
    *   Outpost: +2 VP per token.
    *   M-Brain: +3 VP per token.
    *   Hypergate: +2 VP per token.
    *   Starlance: +2 VP per token.
4.  **Fleet Tokens:** +1 VP for each of your Fleet Tokens remaining on the game grid (in any sector).
5.  **Economic Resources:** +1 VP for every 1 Economic resource you have remaining on your Storage Card.
6.  **Special Goals (Civilization Specific):**
    *   *Stellar Architects:* +3 VP for each Megastructure (Starlance, Hypergate, M-Brain) built.
    *   *Quantum Sentinels:* +3 VP for every combat won [Placeholder: Define "combat won" - surviving with ships? Wiping out opponent?].
    *   *Void Navigators:* +1 VP for each explored sector on the grid at game end.
    *   *Helix Cultivators:* Accumulate a total of 15 Strategic resources on your resource storage card [Placeholder: Needs confirmation if this is end-game state or achieved during game].
7.  **Objective Cards:** Award VP indicated on any achieved public [or private?] Objective Cards. [Placeholder: Detail Objective Card mechanics if used].

The player with the most total VP wins. Ties are friendly [Placeholder: Define tiebreaker rule if needed, e.g., most Strategic resources?].

**14. GLOSSARY**

*(Based on Milkomeda PDF Glossary + our terms)*

*   **Action Display:** Player board showing core actions, used with Action Marker.
*   **Action Marker:** Token used on Action Display to track last action, prevents repeats (unless M-Brain).
*   **Attack Action:** Core action to move fleets into an opponent's sector to initiate Combat. Can also target structures via Starlance.
*   **Attack Vector Area:** The connecting lines/arrows between Ship Type nodes on the Battle Mat, representing valid RPS attacks. Dice are placed here.
*   **Battle Mat:** Shared tile where combat is resolved using ship tokens on nodes.
*   **Build Action:** Core action to spend resources to build Fleets or Structures.
*   **Command Points (CP):** Resource (2 per player per combat round) allocated secretly for tactical benefits (Boost Attack/Defense, Prepare Reshape).
*   **Combat:** The process triggered by the Attack Action, resolved using the "Vector Command" system.
*   **Controlled Sector:** A sector where a player has the most Fleet Tokens present, or where the defender retains control via a structure after mutual destruction.
*   **Economic (Resource):** Yellow resource, primarily used for building fleets/structures, worth VP at game end.
*   **Explore Action:** Core action to draw and place new Sector cards onto the grid.
*   **Fleet Configuration:** The secret, simultaneous step at the start of combat where players assign their generic Fleet Tokens to specific Ship Type nodes on the Battle Mat via their Fleet Roster.
*   **Fleet Roster Card:** Private player card showing the 5 ship types, used for secret Fleet Configuration and secret targeting/casualty allocation.
*   **Fleet Tokens:** Generic physical tokens representing a player's fleets on the main game board. Their specific Ship Type is determined during Fleet Configuration in combat.
*   **Formation Advantage:** (1v1 Combat Only) Tiebreaker advantage gained by having more RPS counters during Fleet Configuration. Breaks ties in Final Hit comparison.
*   **Homeworld:** Unique starting Sector card for each player.
*   **Hypergate:** Structure improving Explore and Move ranges.
*   **Logistic (Resource):** Blue resource, used to boost Move range and pay for Attack movement/Structure Attack.
*   **M-Brain:** Structure providing income bonus and allowing action repetition.
*   **Maneuver Selection:** Phase in combat where players secretly allocate Command Points.
*   **Master of the Order Token:** Token granting control over turn order card distribution.
*   **Move Action:** Core action to move fleets between explored sectors.
*   **Node:** A point on the Battle Mat representing one of the 5 Ship Types.
*   **Order Cards:** Cards determining player turn order each round.
*   **Outpost:** Structure allowing localized fleet building.
*   **Pindown:** Mechanic restricting fleet movement through enemy-controlled sectors. Values (0, 1, 2) determine how many fleets can pass unhindered.
*   **Prepare Reshape:** CP allocation option allowing a ship to change type after combat resolution.
*   **Reshape:** Action (enabled by CP) allowing a surviving ship token to move to an adjacent node on the Battle Mat (following RPS arrows) after casualties are removed.
*   **Rock-Paper-Scissors (RPS):** System defining which Ship Types counter others, determining valid Attack Vectors.
*   **Scientific (Resource):** Green resource, used to boost the Explore action.
*   **Sector Card:** Card representing a region of space, forming the map grid.
*   **Starlance:** Structure enabling the Attack Structure action.
*   **Storage Card:** Player board for tracking resource levels.
*   **Strategic (Resource):** Red resource, used for Structure Attack, potentially for Civ abilities.
*   **Structure Tokens:** Physical tokens representing Outposts, Starlances, Hypergates, M-Brains.
*   **Targeting Markers:** Conceptual markers placed secretly on the Fleet Roster to indicate which opponent ship types are being targeted by hits.


---

This consolidated draft incorporates all the decisions, mechanics, lore, and terminology we've discussed. It clearly marks placeholders where further definition or clarification is needed. Please review this carefully. It should serve as a robust foundation for your continued development.