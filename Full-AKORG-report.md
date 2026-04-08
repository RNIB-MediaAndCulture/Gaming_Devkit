# Accessibility Kick-Off Report

## Selected Game Aspects

- Menu (textual)
- Character Progression
- Class-Based Play /Role-play
- Combat (1v1)
- Combat (beat 'em up)
- Combat (first-person)
- Combat (continuous)
- Combat (menu driven)
- Exploration
- Management / Tycoon
- Environmental Interaction
- Construction
- Narrative Choice / Branching Paths
- Stealth
- Sports [stub]
- Simulation
- Adventure
- Survival
- Rhythm / Timing
- Racing
- strategy
- Co-op Mechanics
- Puzzle
- Combat (multi-character turn-based)

---

## Mechanics to Implement

### Aim

The player must precisely position a targeting reticle or crosshair to interact with objects or attack  enemies, typically using mouse, joystick, or motion controls.

**Required for:** Combat (first-person), Sports [stub]

#### Accessibility Barriers & Considerations

**Barrier 1:** Precise aiming requires fine motor control that may be difficult for gamers with motor impairments or tremors.

**Consider:**
- Providing aim assist options with adjustable strength (target magnetism, friction, tracking).
- Offering target lock-on mechanics as an alternative to free aiming.
- Implementing larger hit boxes or more forgiving aim requirements.

**Barrier 2:** Players with sight loss cannot see targets to aim at them.

**Consider:**
- Providing audio targeting systems that indicate target direction and distance through sound.
- Implementing auto-aim options for accessibility.
- Using haptic feedback to indicate when aim is on target.

**Related Patterns:** [Audio beacons](#audio-beacons), [Coded audio](#coded-audio)

**Barrier 3:** Players with partial sight may struggle to see small crosshairs or distant targets.

**Consider:**
- Allowing customization of crosshair size, color, and contrast.
- Providing target highlighting or outline options.

**Related Patterns:** [Customisable UI / HUD](#customisable-ui-hud), [High Contrast](#high-contrast), [Audio aiming](#audio-aiming)

---

### attack

The player initiates an offensive action against an enemy or object, typically through button presses or  trigger pulls.

**Required for:** Combat (1v1), Combat (beat 'em up), Combat (first-person), Combat (multi-character turn-based), Rhythm / Timing, Adventure, Sports [stub], strategy

#### Accessibility Barriers & Considerations

**Barrier 1:** Precise timing or button combinations may be difficult for gamers with motor impairments.

**Consider:**
- Offering simpler attack inputs with fewer button combinations.
- Implementing attack queuing or buffering to make timing more forgiving.
- Providing one-button attack options or auto-attack modes.

**Barrier 2:** Players with sight loss cannot see when attacks connect or when they should attack.

**Consider:**
- Using distinct audio feedback for successful hits, misses, and critical hits.
- Implementing haptic feedback for attack confirmation.
- Providing audio cues for optimal attack timing windows.

**Related Patterns:** [Coded audio](#coded-audio), [Adjustable semantic audio profiles](#adjustable-semantic-audio-profiles)

**Barrier 3:** Rapid repeated button presses (button mashing) can cause fatigue or be impossible for some players.

**Consider:**
- Offering toggle or hold alternatives to repeated pressing.
- Reducing or eliminating quick-time events that require rapid inputs.

**Related Patterns:** [Digital control](#digital-control)

---

### attack - continuous

The player's character automatically continues attacking once an attack command is given, until told to stop  or the target is defeated.

**Required for:** Combat (continuous)

#### Accessibility Barriers & Considerations

**Barrier 1:** Players need to know when continuous attacks start, stop, or if the target changes.

**Consider:**
- Providing clear audio feedback when entering/exiting continuous attack mode.
- Using distinct sounds for attacks on different targets.
- Visual indicators showing continuous attack status.

**Related Patterns:** [Coded audio](#coded-audio)

**Barrier 2:** Players with sight loss may not know when to cancel continuous attacks (e.g., when target is defeated or a better target appears).

**Consider:**
- Announcing target status changes through audio (Target defeated, New threat detected).
- Implementing smart targeting that automatically switches to optimal targets.

**Related Patterns:** [Text to speech](#text-to-speech), [Audio beacons](#audio-beacons), [Coded audio](#coded-audio)

**Barrier 3:** Managing multiple characters with continuous attacks can be cognitively overwhelming.

**Consider:**
- Providing clear character identification in audio feedback.
- Allowing simplified group commands.

**Related Patterns:** [Coded audio](#coded-audio)

---

### block

The player performs a defensive action to reduce or negate incoming damage, typically requiring timing and  directional awareness.

**Required for:** Combat (1v1), Combat (beat 'em up), Combat (first-person), Adventure

#### Accessibility Barriers & Considerations

**Barrier 1:** Precise timing for blocks can be difficult for players with delayed reaction times or motor impairments.

**Consider:**
- Offering extended block windows or more forgiving timing.
- Implementing auto-block options or assisted blocking.
- Providing block buffering to accept inputs slightly early.

**Barrier 2:** Players with sight loss cannot see incoming attacks to time blocks appropriately.

**Consider:**
- Using distinct audio cues that telegraph attack timing and type.
- Implementing rhythmic audio patterns that indicate when to block.
- Providing haptic feedback as attack timing indicator.

**Related Patterns:** [Coded audio](#coded-audio), [Binaural audio](#binaural-audio), [Surround sound](#surround-sound)

**Barrier 3:** Directional blocking requires knowing which direction attacks come from.

**Consider:**
- Using surround sound or binaural audio to indicate attack direction.
- Simplifying to non-directional blocking or assisted directional blocking.

**Related Patterns:** [Audio beacons](#audio-beacons), [Binaural audio](#binaural-audio), [Surround sound](#surround-sound)

---

### character creation

Players design and customize their character's appearance, attributes, class, background, and other defining  characteristics.

**Required for:** Class-Based Play /Role-play

#### Accessibility Barriers & Considerations

**Barrier 1:** Visual-only character appearance customization is inaccessible to players with sight loss.

**Consider:**
- Providing text descriptions of appearance options (Short spiky hair, red).
- Using text-to-speech to describe customization choices.
- Allowing players to skip appearance customization if not gameplay-relevant.

**Related Patterns:** [Text to speech](#text-to-speech)

**Barrier 2:** Complex multi-stage character creation can be overwhelming and difficult to navigate.

**Consider:**
- Providing clear audio/visual indicators of progress through creation steps.
- Announcing how many steps remain in the process.
- Allowing players to save and return to character creation.
- Offering quick creation presets as alternatives.

**Related Patterns:** [Text to speech](#text-to-speech), [Pre-recorded audio clips](#pre-recorded-audio-clips)

**Barrier 3:** Understanding stat implications and build viability requires complex information processing.

**Consider:**
- Providing clear explanations of what each stat affects.
- Offering recommended builds or templates for different play styles.
- Announcing when choices have significant gameplay impacts.

**Barrier 4:** Visual feedback on how customization affects appearance may not be perceivable.

**Consider:**
- Describing appearance changes verbally as they're made.
- Allowing characters to be re-customized later if mistakes are made.
- Providing presets that can be slightly modified.

**Related Patterns:** [Screenreader support](#screenreader-support), [Clear fonts and text](#clear-fonts-and-text), [High Contrast](#high-contrast)

---

### character selection

Choose a character to play from a roster of available options, each potentially with different abilities,  stats, or play styles.

**Required for:** Class-Based Play /Role-play, Combat (multi-character turn-based)

#### Accessibility Barriers & Considerations

**Barrier 1:** Character differences are communicated primarily through visual design.

**Consider:**
- Providing audio descriptions of each character's appearance and personality.
- Announcing character names clearly as they're highlighted.
- Using distinct audio themes or voice lines for each character.

**Related Patterns:** [Text to speech](#text-to-speech), [Pre-recorded audio clips](#pre-recorded-audio-clips)

**Barrier 2:** Understanding character abilities and playstyles requires reading or observing complex information.

**Consider:**
- Providing clear, concise audio summaries of character abilities.
- Announcing character difficulty or recommended experience level.
- Offering try before you select preview modes with audio guidance.

**Related Patterns:** [Text to speech](#text-to-speech)

**Barrier 3:** Large character rosters are difficult to navigate efficiently.

**Consider:**
- Implementing character filtering by role, difficulty, or attributes.
- Providing favorites or recent selections for quick access.
- Announcing position in roster (Character 5 of 20).

**Related Patterns:** [Text to speech](#text-to-speech)

**Barrier 4:** Locked or unavailable characters may not be clearly indicated.

**Consider:**
- Announcing lock status when hovering over characters.
- Explaining unlock requirements audibly.
- Using distinct audio cues for locked vs. unlocked characters.

**Related Patterns:** [Coded audio](#coded-audio), [High Contrast](#high-contrast), [Clear fonts and text](#clear-fonts-and-text)

---

### checkbox - additive selection

Multiple items can be independently toggled on or off, allowing zero, one, or multiple simultaneous selections.

**Required for:** Menu (textual), Combat (menu driven)

#### Accessibility Barriers & Considerations

**Barrier 1:** Players with sight loss cannot perceive which checkboxes are checked or unchecked.

**Consider:**
- Announcing the state of each checkbox as it's focused (Sound effects: checked).
- Using distinct sounds for checking vs. unchecking actions.
- Announcing total number of checked items when appropriate.

**Related Patterns:** [Text to speech](#text-to-speech), [Coded audio](#coded-audio)

**Barrier 2:** Visual checkbox states may be unclear for partially sighted players.

**Consider:**
- Using high contrast checkmarks or fill colors.
- Making checkboxes larger and more visually distinct.
- Using text labels in addition to checkmarks (ON/OFF).

**Related Patterns:** [High Contrast](#high-contrast), [Clear fonts and text](#clear-fonts-and-text)

**Barrier 3:** Understanding that multiple selections are possible may not be obvious.

**Consider:**
- Announcing that multiple selections are allowed when entering the menu.
- Using distinct terminology (Toggle rather than Select).
- Providing a select all or clear all option for convenience.

**Related Patterns:** [Text to speech](#text-to-speech), [Screenreader support](#screenreader-support), [Opaque background](#opaque-background)

---

### combat mode

The player switches between different combat stances or modes that affect available abilities, defensive  posture, or combat style (e.g., aggressive/defensive stance, different weapon sets, combat/exploration mode).

**Required for:** Combat (continuous), Combat (multi-character turn-based), strategy

#### Accessibility Barriers & Considerations

**Barrier 1:** Players with sight loss cannot see which combat mode is currently active.

**Consider:**
- Announcing combat mode changes audibly (Defensive stance activated).
- Using distinct ambient sounds or audio signatures for each combat mode.
- Providing audio confirmation when attempting to use mode-specific abilities.

**Related Patterns:** [Text to speech](#text-to-speech), [Coded audio](#coded-audio)

**Barrier 2:** Visual-only mode indicators may be missed during intense combat.

**Consider:**
- Making mode indicators prominent and high contrast.
- Positioning mode indicators within the visual safe zone.
- Using screen effects or color grading to reinforce mode changes.

**Related Patterns:** [High Contrast](#high-contrast), [Visual safe zone](#visual-safe-zone), [Customisable UI / HUD](#customisable-ui-hud)

**Barrier 3:** Accidentally switching modes during combat due to complex input requirements.

**Consider:**
- Requiring deliberate input to switch modes (hold button, confirm prompt).
- Providing clear feedback when mode switches occur.
- Allowing mode switching to be disabled or remapped.

**Related Patterns:** [Digital control](#digital-control)

---

### Companion

**Required for:** Combat (first-person)

---

### cooldown

The player must wait a specified time period before using an ability, item, or action again. Tracking  multiple cooldowns simultaneously is common in many games.

**Required for:** Combat (continuous)

#### Accessibility Barriers & Considerations

**Barrier 1:** Visual-only cooldown indicators (progress circles, grayed-out icons) are inaccessible to players with sight loss.

**Consider:**
- Announcing when abilities come off cooldown (Fireball ready).
- Providing audio cues that indicate cooldown progress (rising pitch, ticking).
- Using distinct sounds when attempting to use abilities still on cooldown.

**Related Patterns:** [Text to speech](#text-to-speech), [Coded audio](#coded-audio)

**Barrier 2:** Small or subtle cooldown timers are difficult to read for partially sighted players.

**Consider:**
- Making cooldown indicators larger and more prominent.
- Using high contrast for cooldown displays.
- Displaying numerical countdown timers in addition to visual progress indicators.

**Related Patterns:** [High Contrast](#high-contrast), [Resizable UI](#resizable-ui), [Customisable UI / HUD](#customisable-ui-hud)

**Barrier 3:** Tracking multiple cooldowns simultaneously can be cognitively overwhelming.

**Consider:**
- Prioritizing important cooldown notifications.
- Allowing players to set which cooldowns trigger audio notifications.
- Grouping or categorizing cooldowns by importance.

**Related Patterns:** [Adjustable semantic audio profiles](#adjustable-semantic-audio-profiles)

---

### crouch

The player makes their character adopt a lower stance, often used for stealth, avoiding detection, or  dodging high attacks.

**Required for:** Combat (first-person), Stealth

#### Accessibility Barriers & Considerations

**Barrier 1:** Toggle vs. hold crouch mechanics - holding buttons can cause fatigue for players with motor impairments.

**Consider:**
- Offering both toggle and hold options for crouching.
- Making toggle the default to reduce sustained input requirements.

**Related Patterns:** [Digital control](#digital-control)

**Barrier 2:** Players with sight loss may not know when crouching is necessary or beneficial.

**Consider:**
- Providing audio cues when crouch-appropriate situations arise (e.g., Low clearance ahead, Enemy looking this way).
- Implementing contextual auto-crouch options.

**Related Patterns:** [Text to speech](#text-to-speech), [Coded audio](#coded-audio)

**Barrier 3:** Remembering crouch state can be difficult without clear feedback.

**Consider:**
- Providing persistant audio cues, coded background audio or haptic feedback while crouched.
- Using distinct movement sounds when crouched vs. standing.

**Related Patterns:** [Coded audio](#coded-audio)

---

### dodge

The player performs an evasive maneuver to avoid attacks or hazards, often requiring quick directional input  and timing.

**Required for:** Combat (1v1), Combat (beat 'em up), Combat (first-person)

#### Accessibility Barriers & Considerations

**Barrier 1:** Dodge timing windows are often very tight, difficult for players with delayed reaction times.

**Consider:**
- Offering extended dodge timing windows or dodge buffering.
- Implementing assisted dodge mechanics that trigger automatically.
- Providing visual or audio telegraphing of dodge opportunities.

**Barrier 2:** Directional dodging requires simultaneous direction and action inputs, challenging for motor-impaired players.

**Consider:**
- Simplifying to non-directional dodges or auto-directional dodges.
- Allowing dodge direction to be set separately from execution.

**Barrier 3:** Players with sight loss cannot see attacks coming to time dodges.

**Consider:**
- Using distinct audio cues that clearly telegraph dodge timing.
- Implementing rhythmic audio patterns for dodge windows.
- Providing haptic feedback for dodge timing.

**Related Patterns:** [Coded audio](#coded-audio), [Binaural audio](#binaural-audio), [Surround sound](#surround-sound)

---

### emoji

Players use emojis or emoticons to communicate non-verbally with other players, often for quick  communication or to overcome language barriers.

**Required for:** Co-op Mechanics

#### Accessibility Barriers & Considerations

**Barrier 1:** Players with sight loss cannot see emojis sent by other players.

**Consider:**
- Announcing emoji meanings through text-to-speech (Player 2 sent thumbs up).
- Providing text descriptions of emojis.
- Supporting screenreader descriptions of emoji content.

**Related Patterns:** [Text to speech](#text-to-speech), [Screenreader support](#screenreader-support)

**Barrier 2:** Players with sight loss cannot easily select and send emojis.

**Consider:**
- Providing text-to-speech navigation of emoji menus.
- Organizing emojis into logical categories with audio navigation.
- Offering quick-access favorites or frequently used emojis.

**Related Patterns:** [Text to speech](#text-to-speech), [Navigate menu 2D](#navigate-menu-2d), [Digital control](#digital-control)

**Barrier 3:** Small emoji icons may be difficult to distinguish for partially sighted players.

**Consider:**
- Allowing emoji size customization.
- Providing text labels or tooltips for emojis.
- Using high contrast display modes for emoji panels.

**Related Patterns:** [Resizable UI](#resizable-ui), [High Contrast](#high-contrast)

---

### enter menu

The player activates or opens a menu system, typically to access settings, inventory, character information,  or game options.

**Required for:** Menu (textual), Combat (menu driven)

#### Accessibility Barriers & Considerations

**Barrier 1:** Players may not know which button opens menus or how to access different menu types.

**Consider:**
- Using consistent button mappings for menu access across the game.
- Providing clear tutorials or button prompts for menu access.
- Allowing menu access through multiple input methods (button, pause, voice).

**Barrier 2:** Menu activation confirmation may only be visual, leaving players with sight loss uncertain if the menu opened.

**Consider:**
- Playing a distinct sound effect when menus open.
- Providing verbal confirmation (Settings menu opened).
- Using haptic feedback for menu state changes.

**Related Patterns:** [Text to speech](#text-to-speech), [Coded audio](#coded-audio)

**Barrier 3:** Overlapping menus or complex menu hierarchies can be confusing.

**Consider:**
- Announcing which menu has been opened when entering.
- Providing clear menu breadcrumbs or navigation paths.
- Using distinct audio signatures for different menu types.

**Related Patterns:** [Digital control](#digital-control), [Coded audio](#coded-audio)

---

### levelling-up

The character gains a level, typically accompanied by stat increases, new abilities, or skill points to  allocate. May involve making choices about character progression.

**Required for:** Character Progression

#### Accessibility Barriers & Considerations

**Barrier 1:** Visual-only level-up notifications and progression screens are inaccessible to players with sight loss.

**Consider:**
- Announcing level-up events clearly (Level 5 achieved!).
- Providing text-to-speech for all progression information and stat changes.
- Using celebratory audio cues for level-up moments.

**Related Patterns:** [Text to speech](#text-to-speech), [Coded audio](#coded-audio)

**Barrier 2:** Complex skill trees or progression choices require understanding visual relationships and hierarchies.

**Consider:**
- Providing clear audio descriptions of progression paths and requirements.
- Announcing stat changes and their gameplay effects.
- Offering recommended progression paths for players who want guidance.

**Related Patterns:** [Text to speech](#text-to-speech), [Screenreader support](#screenreader-support)

**Barrier 3:** Small text and complex UI layouts make progression information hard to read.

**Consider:**
- Making progression interfaces resizable and high contrast.
- Using clear fonts and adequate text size.
- Providing opaque backgrounds for text readability.

**Related Patterns:** [Resizable text](#resizable-text), [High Contrast](#high-contrast), [Clear fonts and text](#clear-fonts-and-text), [Opaque background](#opaque-background)

---

### locate opponant2D

The player must identify and track the position of enemies or opponents within the game space, whether on  screen or off screen.

**Required for:** Combat (1v1), Combat (beat 'em up), Combat (continuous), Combat (first-person), Combat (multi-character turn-based), Stealth, strategy

#### Accessibility Barriers & Considerations

**Barrier 1:** Players with sight loss cannot visually locate opponents.

**Consider:**
- Using directional audio (surround sound/binaural) to indicate opponent positions.
- Implementing audio beacons or pings that reveal enemy locations.
- Providing verbal callouts of opponent positions (e.g., Enemy behind you).

**Related Patterns:** [Audio beacons](#audio-beacons), [Binaural audio](#binaural-audio), [Surround sound](#surround-sound), [Coded audio](#coded-audio)

**Barrier 2:** Players with partial sight may struggle to distinguish opponents from the environment or friendlies.

**Consider:**
- Offering high contrast modes for enemy highlighting.
- Allowing customization of enemy outline colors and thickness.
- Providing clear visual/audio distinction between enemy types.

**Related Patterns:** [High Contrast](#high-contrast)

**Barrier 3:** Off-screen opponents are difficult to track without visual indicators.

**Consider:**
- Implementing off-screen indicators with audio cues.
- Using 3D audio to maintain spatial awareness of off-screen enemies.

**Related Patterns:** [Audio beacons](#audio-beacons), [Binaural audio](#binaural-audio), [Surround sound](#surround-sound)

---

### move building

The player repositions a building, structure, or placed object to a new location, typically in  construction, city-building, or strategy games.

**Required for:** Construction, Management / Tycoon

#### Accessibility Barriers & Considerations

**Barrier 1:** Precise positioning requires visual feedback that is inaccessible to players with sight loss.

**Consider:**
- Implementing grid-based placement with audio feedback for position.
- Announcing coordinates or relative positions (3 spaces north of town hall).
- Using audio cues to indicate valid/invalid placement locations.

**Related Patterns:** [Audio beacons](#audio-beacons), [Text to speech](#text-to-speech), [Coded audio](#coded-audio)

**Barrier 2:** Fine motor control required for drag-and-drop movement is difficult for players with motor impairments.

**Consider:**
- Providing alternative selection and placement methods (select, then place).
- Implementing grid snapping or snap-to-valid-location functionality.
- Using keyboard/controller navigation for precise positioning.

**Related Patterns:** [Digital control](#digital-control)

**Barrier 3:** Visual collision detection and placement previews are not accessible.

**Consider:**
- Providing audio feedback for collisions or invalid placements.
- Announcing whether the current position is valid before confirming.
- Using distinct sounds for different placement states (valid, invalid, optimal).

**Related Patterns:** [Coded audio](#coded-audio)

---

### Movement2D

The player controls their character's movement through a 2D or 3D space, typically using directional  inputs (keyboard, joystick, or other controllers).

**Required for:** Combat (1v1), Combat (beat 'em up), Combat (continuous), Combat (first-person), Combat (multi-character turn-based), Construction, Environmental Interaction, Exploration, Racing, Survival, Adventure, Simulation, Sports [stub], Stealth, strategy, Puzzle

#### Accessibility Barriers & Considerations

**Barrier 1:** Fine motor control required for analogue stick movement can be difficult for gamers with motor impairments.

**Consider:**
- Providing digital directional alternatives (discrete button presses) alongside analogue controls.
- Offering adjustable movement speed settings and acceleration curves.
- Implementing auto-run or hold-to-move options to reduce sustained input requirements.

**Related Patterns:** [Digital control](#digital-control)

**Barrier 2:** Simultaneous movement and other actions (looking, attacking) can be challenging for gamers with limited motor function.

**Consider:**
- Allowing button remapping and custom control schemes.
- Implementing assisted movement options or auto-navigation to waypoints.

**Barrier 3:** Players with sight loss cannot see where they are moving or what obstacles are in their path.

**Consider:**
- Providing audio cues for terrain changes, nearby obstacles, and directional information.
- Implementing audio beacons for navigation waypoints.
- Adding collision sounds to alert players they cannot go further in that direction.

**Related Patterns:** [Audio beacons](#audio-beacons), [Coded audio](#coded-audio)

---

### navigate menu 1D

Move through a menu in one dimension with a next and previous option. This could be vertical (moving up and  down), horizontal (moving left and right) or any other modality with next item, previous item and select options.

**Required for:** Menu (textual), Character Progression, Class-Based Play /Role-play, Combat (menu driven), Construction, Management / Tycoon, Narrative Choice / Branching Paths, Survival, Adventure, Simulation, strategy, Puzzle

#### Accessibility Barriers & Considerations

**Barrier 1:** Gamers without sight cannot perceive menu elements to navigate them.

**Consider:**
- Implementing text-to-speech that reads each menu item as it's highlighted.
- Supporting platform screenreaders where available.
- Using pre-recorded audio clips for menu options to enhance quality.

**Related Patterns:** [Text to speech](#text-to-speech), [Screenreader support](#screenreader-support), [Pre-recorded audio clips](#pre-recorded-audio-clips)

**Barrier 2:** Partially sighted gamers can struggle with low contrast, small or hard to read interfaces.

**Consider:**
- Using clear fonts and text that are easier to read.
- Offering a high contrast option or, preferably, a high contrast default.
- Offering opaque backgrounds, preferably as a default but potentially as part of a high contrast profile.
- Making text resizable to accommodate different visual needs.

**Related Patterns:** [Clear fonts and text](#clear-fonts-and-text), [High Contrast](#high-contrast), [Opaque background](#opaque-background), [Resizable text](#resizable-text)

**Barrier 3:** Movement through the menu via analogue controls can be imprecise and difficult.

**Consider:**
- Supporting digital directional input (discrete button presses) for menu navigation.
- Implementing menu navigation wrapping (going past the last item returns to first).
- Preventing accidental navigation with appropriate input deadzone settings.

**Related Patterns:** [Digital control](#digital-control)

**Barrier 4:** Long menus without clear structure are difficult to navigate efficiently.

**Consider:**
- Announcing position in the menu (Item 3 of 10).
- Implementing quick navigation (jump to first/last, page up/down).
- Providing menu search functionality.

**Related Patterns:** [Text to speech](#text-to-speech), [CVD friendly communication](#cvd-friendly-communication)

---

### navigate menu 2D

Navigate through menus that have both horizontal and vertical dimensions, such as grid layouts, tables, or  menus with multiple columns and rows.

**Required for:** Menu (textual), Character Progression, Class-Based Play /Role-play, Combat (menu driven), Management / Tycoon, Narrative Choice / Branching Paths, Survival, Adventure, Simulation, strategy, Puzzle

#### Accessibility Barriers & Considerations

**Barrier 1:** Gamers without sight cannot perceive the 2D spatial layout of menu elements.

**Consider:**
- Implementing text-to-speech that announces each item and its position.
- Announcing row and column information (Row 2, Column 3 of 5).
- Showing preference to semantic labels for rows and columns rather than numeric ones where possible.
- Providing linear navigation alternatives that traverse the 2D space in a predictable pattern.

**Related Patterns:** [Text to speech](#text-to-speech), [Screenreader support](#screenreader-support)

**Barrier 2:** Understanding the structure and boundaries of 2D menus is cognitively demanding.

**Consider:**
- Playing boundary sounds when reaching edges of the menu.
- Announcing menu dimensions when first entered (3 by 4 grid).
- Allowing toggle between 2D and 1D navigation modes.

**Related Patterns:** [Coded audio](#coded-audio)

**Barrier 3:** Analogue control for 2D menu navigation is imprecise.

**Consider:**
- Supporting digital directional controls for discrete cell-by-cell movement.
- Implementing grid snapping to prevent landing between menu items.
- Using shoulder buttons or triggers for quick row/column jumping.

**Related Patterns:** [Digital control](#digital-control)

**Barrier 4:** Partially sighted gamers may lose track of their position in complex 2D layouts.

**Consider:**
- Highlighting the current selection with high contrast indicators.
- Showing visual breadcrumbs or position markers.
- Announcing current position when navigation resumes after inactivity.

**Related Patterns:** [High Contrast](#high-contrast), [Opaque background](#opaque-background), [Clear fonts and text](#clear-fonts-and-text)

---

### object comparison

Compare two or more items side-by-side to evaluate differences in stats, properties, or characteristics,  helping players make informed decisions.

**Required for:** Character Progression, Management / Tycoon, Survival

#### Accessibility Barriers & Considerations

**Barrier 1:** Visual comparison layouts are inaccessible to players with sight loss.

**Consider:**
- Providing audio readout of key differences between items.
- Announcing which item is better in specific categories.
- Offering a summary comparison (Sword A has higher damage but lower speed).

**Related Patterns:** [Text to speech](#text-to-speech)

**Barrier 2:** Complex comparison tables with multiple columns and rows are difficult to navigate without sight.

**Consider:**
- Implementing structured navigation that reads comparisons systematically.
- Allowing users to select specific attributes to compare.
- Announcing the structure of comparison tables when entering them.

**Related Patterns:** [Text to speech](#text-to-speech), [Screenreader support](#screenreader-support)

**Barrier 3:** Color coding differences (red for worse, green for better) fails for color blind players.

**Consider:**
- Using text indicators (+5, -3) in addition to or instead of colors.
- Using symbols (↑, ↓) alongside color coding.
- Providing CVD-friendly color options.

**Related Patterns:** [CVD friendly communication](#cvd-friendly-communication), [High Contrast](#high-contrast)

**Barrier 4:** Small text or tight layouts make comparisons difficult for partially sighted players.

**Consider:**
- Making comparison interfaces resizable.
- Using high contrast for difference indicators.
- Allowing simplified comparison views with only key differences.

**Related Patterns:** [Resizable text](#resizable-text), [Clear fonts and text](#clear-fonts-and-text)

---

### object description

Present detailed information about an item, character, ability, or game element, typically in text form with  possible accompanying visuals.

**Required for:** Character Progression, Class-Based Play /Role-play, Combat (menu driven), Management / Tycoon, Narrative Choice / Branching Paths, Survival, Adventure

#### Accessibility Barriers & Considerations

**Barrier 1:** Text-only descriptions are inaccessible to players with sight loss.

**Consider:**
- Implementing text-to-speech for all object descriptions.
- Supporting platform screenreaders.
- Using pre-recorded audio descriptions for key items/characters.

**Related Patterns:** [Text to speech](#text-to-speech), [Screenreader support](#screenreader-support), [Pre-recorded audio clips](#pre-recorded-audio-clips)

**Barrier 2:** Small text or poor contrast makes descriptions difficult to read for partially sighted players.

**Consider:**
- Making text resizable or offering multiple text size options.
- Using high contrast color schemes for description panels.
- Providing opaque backgrounds behind description text.
- Using clear, readable fonts.

**Related Patterns:** [Resizable text](#resizable-text), [High Contrast](#high-contrast), [Opaque background](#opaque-background), [Clear fonts and text](#clear-fonts-and-text)

**Barrier 3:** Long descriptions can be overwhelming or difficult to navigate.

**Consider:**
- Breaking descriptions into logical sections that can be navigated.
- Providing a brief summary followed by detailed information.
- Announcing the length of descriptions for audio users.

**Barrier 4:** Visual-only information (icons, color coding, images) within descriptions.

**Consider:**
- Providing text or audio equivalents for all visual information.
- Announcing icon meanings when using text-to-speech.
- Not relying on color alone to convey information.

**Related Patterns:** [CVD friendly communication](#cvd-friendly-communication)

---

### Perceive attack

The gamer needs to know their character is being attacked so they can react accordingly.

**Required for:** Combat (1v1), Combat (beat 'em up), Combat (continuous), Combat (first-person), Combat (menu driven), Combat (multi-character turn-based), Rhythm / Timing

#### Accessibility Barriers & Considerations

**Barrier 1:** If attacks towards the player are only represented visually then gamers without sight will not know that they need to react.

**Consider:**
- Using a sound effect to indicate the attack coming in. The player needs to know what type of attack and which direction.
- Surround sound or stereo encoding may be appropriate to communicate the direction the attack is coming in from.

---

### Perceive collision

When moving around an area a player needs to know that they have collided with something.

**Required for:** Combat (beat 'em up), Combat (first-person), Construction, Exploration, Racing, Survival, Adventure, Simulation, Stealth

#### Accessibility Barriers & Considerations

**Barrier 1:** If objects that characters can collide with are only represented visually then gamers without sight cannot tell that they have collided with something. They may try to keep going in this direction thinking the are still moving.

**Consider:**
- using a sound effect to indicate the collision.

---

### Perceive danger

The player needs to identify environmental hazards, incoming threats, or dangerous situations that require  avoidance or defensive action.

**Required for:** Exploration, Racing, Survival, Stealth

#### Accessibility Barriers & Considerations

**Barrier 1:** Visual-only danger indicators (red zones, warning signs, visual effects) are inaccessible to players with sight loss.

**Consider:**
- Using warning sounds that increase in urgency as danger approaches.
- Implementing haptic feedback for proximity to hazards.
- Providing verbal warnings for specific danger types.

**Related Patterns:** [Coded audio](#coded-audio), [Binaural audio](#binaural-audio), [Adjustable semantic audio profiles](#adjustable-semantic-audio-profiles)

**Barrier 2:** Subtle environmental danger cues may be missed by players with partial sight or attention difficulties.

**Consider:**
- Making danger indicators more pronounced and distinctive.
- Offering adjustable danger warning sensitivity.
- Using multiple sensory channels (audio, visual, haptic) simultaneously.

**Related Patterns:** [High Contrast](#high-contrast), [Coded audio](#coded-audio)

**Barrier 3:** Players with hearing loss may miss audio danger warnings.

**Consider:**
- Providing visual danger indicators with high contrast.
- Using screen shake or controller vibration for imminent danger.
- Implementing visual sound effects for danger cues.

**Related Patterns:** [Visual sound effects](#visual-sound-effects), [High Contrast](#high-contrast)

---

### Perceive direction

In a virtual world the user needs to be able to navigate to a particular direction. This could be because  they need to go north or because they are being told that a quest item is in that direction. This is  separate to knowing which path to take

**Required for:** Combat (first-person), Exploration, Racing, Rhythm / Timing, Adventure, Simulation, Sports [stub], Stealth

#### Accessibility Barriers & Considerations

**Barrier 1:** Direction is communicated visually and is not accessible to people with sight loss

**Consider:**
- providing a ping only when the user is facing the direction to be perceived.
- enabling the player to set a steady sonar ping in the direction that needs to be perceived.

**Related Patterns:** [Audio Beacons](#audio-beacons)

---

### perceive earnings

The player needs to understand income, revenue, or resource generation rates in management, tycoon, or  strategy games. This includes tracking passive income and understanding economic performance.

**Required for:** Management / Tycoon

#### Accessibility Barriers & Considerations

**Barrier 1:** Visual-only displays of earnings, graphs, and financial data are inaccessible to players with sight loss.

**Consider:**
- Announcing earnings and income rates through text-to-speech.
- Providing audio summaries of financial performance (Income up 15% this quarter).
- Using audio cues for significant financial events (profit milestone reached).

**Related Patterns:** [Text to speech](#text-to-speech), [Coded audio](#coded-audio)

**Barrier 2:** Complex graphs and charts are difficult to perceive for people with sight loss and difficult to interpret for players with sight loss or cognitive difficulties.

**Consider:**
- Providing text-based data tables as alternatives to graphs.
- Announcing trends verbally (Sales trending upward, Expenses decreasing).
- Simplifying data presentation with clear summaries.

**Related Patterns:** [Text to speech](#text-to-speech)

**Barrier 3:** Small numbers, graphs, and financial UI elements are hard to read for partially sighted players.

**Consider:**
- Making financial displays resizable and high contrast.
- Using clear fonts for numerical data.
- Providing opaque backgrounds for better readability.

**Related Patterns:** [Resizable text](#resizable-text), [Resizable UI](#resizable-ui), [High Contrast](#high-contrast), [Clear fonts and text](#clear-fonts-and-text), [Opaque background](#opaque-background)

**Barrier 4:** Color-coded financial data (red for loss, green for profit) fails for color blind players.

**Consider:**
- Using symbols and text labels in addition to color (+/-  signs, up/down arrows).
- Providing CVD-friendly color schemes.
- Using patterns or textures to distinguish positive/negative values.

**Related Patterns:** [CVD friendly communication](#cvd-friendly-communication)

---

### Perceive environment state

The player needs to understand the current state of the game environment, such as weather conditions,  time of day, environmental hazards active/inactive, or changes to the world state (bridges raised/lowered,  doors open/closed, etc.).

**Required for:** Environmental Interaction, Puzzle

#### Accessibility Barriers & Considerations

**Barrier 1:** Visual-only indicators of environment state are inaccessible to players with sight loss.

**Consider:**
- Providing audio cues or verbal descriptions of environmental conditions.
- Announcing significant environmental state changes (The storm has cleared, Night is falling).
- Using ambient audio to convey environmental state (rain sounds, wind, crickets at night).

**Related Patterns:** [Text to speech](#text-to-speech), [Coded audio](#coded-audio), [Adjustable semantic audio profiles](#adjustable-semantic-audio-profiles)

**Barrier 2:** Subtle visual changes to environment state may be missed by partially sighted players.

**Consider:**
- Making environmental indicators more pronounced and clear.
- Providing UI indicators for important environmental states.
- Using high contrast visual effects for state changes.

**Related Patterns:** [High Contrast](#high-contrast), [Customisable UI / HUD](#customisable-ui-hud)

**Barrier 3:** Players with hearing loss may miss audio-only environmental cues.

**Consider:**
- Providing visual indicators for environmental sounds and states.
- Using captions or visual cues for ambient sound changes.
- Implementing icons or UI elements that show current environmental conditions.

**Related Patterns:** [Visual sound effects](#visual-sound-effects), [Captions](#captions)

---

### Perceive FoE

The player must identify whether a character or entity is a Friend or Enemy (FoE), which may affect gameplay  decisions and strategies.

**Required for:** Combat (1v1), Combat (beat 'em up), Combat (continuous), Combat (first-person), Combat (multi-character turn-based), Sports [stub], Stealth, strategy

#### Accessibility Barriers & Considerations

**Barrier 1:** Friend/enemy distinction relies on visual cues (colors, uniforms, markers) that players with sight loss or color vision deficiency cannot perceive.

**Consider:**
- Using distinct audio signatures for friends vs. enemies.
- Implementing verbal identification (Ally nearby, Enemy detected).
- Using different sound profiles for friendly and enemy actions.

**Related Patterns:** [Coded audio](#coded-audio), [Text to speech](#text-to-speech), [Audio beacons](#audio-beacons)

**Barrier 2:** Color-coded friend/enemy systems fail for players with color vision deficiency.

**Consider:**
- Using shapes, patterns, and symbols in addition to color.
- Allowing customization of friend/enemy colors.
- Implementing CVD-friendly color profiles.

**Related Patterns:** [CVD friendly communication](#cvd-friendly-communication), [High Contrast](#high-contrast)

**Barrier 3:** Neutral or shifting alliances can be confusing without clear indication.

**Consider:**
- Providing clear audio/visual feedback when alliance status changes.
- Using distinct markers or sounds for neutral entities.

**Related Patterns:** [Coded audio](#coded-audio)

---

### Perceive interactable

The player needs to identify which objects or elements in the environment can be interacted with and  understand what interactions are possible.

**Required for:** Environmental Interaction, Exploration, Survival, Adventure, Puzzle

#### Accessibility Barriers & Considerations

**Barrier 1:** Interactive objects that only indicate interactability through visual highlighting are inaccessible to players with sight loss.

**Consider:**
- Using distinct audio cues when near interactive objects.
- Implementing object scanning with audio feedback listing nearby interactables.
- Providing verbal descriptions of available interactions.

**Related Patterns:** [Audio beacons](#audio-beacons), [Text to speech](#text-to-speech), [Coded audio](#coded-audio)

**Barrier 2:** Subtle visual cues for interactability may be missed by partially sighted players.

**Consider:**
- Making interaction prompts more prominent with high contrast.
- Allowing customization of interaction indicator size and color.
- Using consistent, clear visual language for all interactive elements.

**Related Patterns:** [High Contrast](#high-contrast), [Customisable UI / HUD](#customisable-ui-hud)

**Barrier 3:** Context-sensitive interactions may not be obvious without trying different buttons.

**Consider:**
- Announcing available interactions when approaching objects.
- Displaying/announcing all possible interactions clearly.
- Using consistent interaction buttons across different object types.

**Related Patterns:** [Text to speech](#text-to-speech), [Coded audio](#coded-audio), [Visual sound effects](#visual-sound-effects)

---

### perceive marker

Players need to see, hear, or otherwise perceive markers placed by themselves or teammates in the game world.

**Required for:** Co-op Mechanics

#### Accessibility Barriers & Considerations

**Barrier 1:** Visual-only markers are inaccessible to players with sight loss.

**Consider:**
- Implementing audio beacons at marker locations that play in 3D space.
- Providing distance and direction information to markers (Team marker 30 meters northwest).
- Using distinct audio signatures for different marker types or teammates.

**Related Patterns:** [Audio beacons](#audio-beacons), [Binaural audio](#binaural-audio), [Surround sound](#surround-sound), [Text to speech](#text-to-speech)

**Barrier 2:** Markers may be difficult to distinguish from environment or other UI elements.

**Consider:**
- Making markers high contrast and visually prominent.
- Allowing customization of marker appearance and size.
- Using both visual and audio indicators simultaneously.

**Related Patterns:** [High Contrast](#high-contrast), [CVD friendly communication](#cvd-friendly-communication)

**Barrier 3:** Off-screen markers may be missed without appropriate indicators.

**Consider:**
- Providing edge-of-screen indicators for off-screen markers.
- Using 3D audio that maintains spatial awareness of marker positions.
- Announcing nearby markers periodically.

**Related Patterns:** [Audio beacons](#audio-beacons), [Binaural audio](#binaural-audio), [Surround sound](#surround-sound)

**Barrier 4:** Multiple markers from different players can create visual/audio clutter.

**Consider:**
- Allowing filtering of markers by type or player.
- Implementing priority systems where critical markers are more prominent.
- Using team-specific audio signatures for marker identification.

**Related Patterns:** [Coded audio](#coded-audio)

**Barrier 5:** Marker information (who placed it, what type, when) may not be clearly conveyed.

**Consider:**
- Announcing marker details when focused or approached.
- Using teammate voice lines or audio signatures for identification.
- Providing a quick view/list of all active markers.

**Related Patterns:** [Text to speech](#text-to-speech), [Coded audio](#coded-audio)

---

### Perceive object state

The player needs to understand the current state of interactive objects, such as whether a switch is  on/off, a container is open/closed, an item is charged/depleted, or a mechanism is active/inactive.

**Required for:** Environmental Interaction, Puzzle

#### Accessibility Barriers & Considerations

**Barrier 1:** Visual-only indicators of object state (color changes, animations, position) are inaccessible to players with sight loss.

**Consider:**
- Providing audio feedback when interacting with or scanning objects to announce their state.
- Using distinct sounds for different object states (click for on, clunk for off).
- Announcing object state when focusing or approaching (Lever: down position, Door: locked).

**Related Patterns:** [Text to speech](#text-to-speech), [Coded audio](#coded-audio), [Audio beacons](#audio-beacons)

**Barrier 2:** Color-based state indicators fail for players with color vision deficiency.

**Consider:**
- Using shapes, icons, and text labels in addition to color.
- Implementing patterns or textures to distinguish states.
- Providing CVD-friendly color schemes.

**Related Patterns:** [CVD friendly communication](#cvd-friendly-communication), [High Contrast](#high-contrast)

**Barrier 3:** Small or subtle state indicators may be difficult to perceive for partially sighted players.

**Consider:**
- Making state indicators larger and more prominent.
- Allowing customization of indicator size and contrast.
- Using multiple visual cues simultaneously (color, icon, text).

**Related Patterns:** [High Contrast](#high-contrast), [Customisable UI / HUD](#customisable-ui-hud)

---

### Perceive objects

The player needs to identify and understand objects in the game environment, including interactive items,  collectibles, obstacles, and decorative elements.

**Required for:** Construction, Environmental Interaction, Exploration, Survival, Adventure, Simulation, Sports [stub], Stealth, Puzzle

#### Accessibility Barriers & Considerations

**Barrier 1:** Players with sight loss cannot see objects or distinguish them from the environment.

**Consider:**
- Implementing object scanning or detection systems with audio feedback.
- Using audio beacons for important objects.
- Providing verbal object descriptions when nearby or focused.

**Related Patterns:** [Audio beacons](#audio-beacons), [Text to speech](#text-to-speech), [Coded audio](#coded-audio)

**Barrier 2:** Small objects or poor visual contrast makes objects hard to see for partially sighted players.

**Consider:**
- Highlighting interactive objects with high contrast outlines.
- Allowing customization of object highlight colors and styles.
- Implementing object magnification or zoom features.

**Related Patterns:** [High Contrast](#high-contrast), [Customisable UI / HUD](#customisable-ui-hud)

**Barrier 3:** Visual clutter makes it difficult to distinguish important objects from background elements.

**Consider:**
- Offering simplified visual modes with reduced clutter.
- Providing object filtering options to highlight only specific object types.
- Using distinct audio signatures for different object categories.
- Offer colour coding option for in-game objects (friend, enemy, interactable object etc)

**Related Patterns:** [Audio beacons](#audio-beacons), [Coded audio](#coded-audio)

---

### Perceive path

The player must identify navigable routes, understand terrain layout, and determine where they can or cannot go.

**Required for:** Exploration, Racing, Adventure, Simulation

#### Accessibility Barriers & Considerations

**Barrier 1:** Visual-only path indicators are inaccessible to players with sight loss.

**Consider:**
- Implementing audio breadcrumb trails or path-following audio cues.
- Using haptic feedback to indicate when on/off the path.
- Providing verbal descriptions of path options (Path forward, Dead end ahead).

**Related Patterns:** [Audio beacons](#audio-beacons), [Text to speech](#text-to-speech), [Coded audio](#coded-audio)

**Barrier 2:** Complex 3D environments make paths difficult to perceive even with sight.

**Consider:**
- Offering assisted navigation modes that guide players along paths.
- Implementing waypoint systems with audio/visual guidance.
- Providing minimap audio descriptions.

**Related Patterns:** [Audio beacons](#audio-beacons), [Text to speech](#text-to-speech)

**Barrier 3:** Distinguishing walkable from non-walkable terrain is difficult without visual cues.

**Consider:**
- Using distinct audio for different terrain types.
- Implementing edge detection warnings when approaching boundaries.
- Providing high contrast modes for terrain visualization.

**Related Patterns:** [Coded audio](#coded-audio), [High Contrast](#high-contrast), [Binaural audio](#binaural-audio)

---

### place building

The player positions and constructs a new building, structure, or object in the game world, typically in  construction, city-building, tower defense, or strategy games.

**Required for:** Construction, Management / Tycoon, Survival

#### Accessibility Barriers & Considerations

**Barrier 1:** Visual positioning and placement validation are inaccessible to players with sight loss.

**Consider:**
- Implementing grid-based or snap-to-location placement with audio feedback.
- Announcing coordinates or descriptions of placement locations.
- Using audio cues to indicate valid/invalid placement (chime for valid, buzz for invalid).

**Related Patterns:** [Audio beacons](#audio-beacons), [Text to speech](#text-to-speech), [Coded audio](#coded-audio)

**Barrier 2:** Players with sight loss cannot see terrain features, resources, or existing structures when placing buildings.

**Consider:**
- Providing scanning functionality that describes nearby features and objects.
- Announcing relevant information about the selected location (flat terrain, near water, 5 spaces from existing structure).
- Using audio beacons to indicate important location features.
- Providing an auto place feature that chooses a suitable spot.

**Related Patterns:** [Audio beacons](#audio-beacons), [Text to speech](#text-to-speech)

**Barrier 3:** Drag-and-drop or free-form placement requires fine motor control difficult for players with motor impairments.

**Consider:**
- Implementing grid-based placement with discrete movements.
- Providing keyboard/d-pad navigation for positioning.
- Allowing rotation and placement as separate, deliberate actions.

**Related Patterns:** [Digital control](#digital-control)

**Barrier 4:** Visual-only indicators of placement requirements (radius, coverage area, resource zones) are not accessible.

**Consider:**
- Announcing placement requirements and coverage areas verbally.
- Using audio feedback to indicate optimal placement locations.
- Providing high contrast visual overlays for placement zones.

**Related Patterns:** [Text to speech](#text-to-speech), [High Contrast](#high-contrast)

---

### place marker

Players place markers, pins, or waypoints in the game world to mark locations of interest, coordinate with  teammates, or remember important spots.

**Required for:** Co-op Mechanics

#### Accessibility Barriers & Considerations

**Barrier 1:** Placing markers precisely requires visual aiming or map interaction.

**Consider:**
- Allowing markers to snap to significant locations or objects.
- Providing voice commands or quick-place options for common marker types.
- Implementing assisted marker placement that suggests nearby points of interest.

**Barrier 2:** Players with sight loss cannot see where markers are being placed.

**Consider:**
- Announcing marker placement location (Marker placed 50 meters ahead).
- Playing a sound effect at the marker's 3D position when placed.
- Confirming marker placement with location details.

**Related Patterns:** [Audio beacons](#audio-beacons), [Text to speech](#text-to-speech)

**Barrier 3:** Different marker types or colors may not be distinguishable.

**Consider:**
- Using verbal labels for marker types (Danger marker, Rally point).
- Announcing marker type during placement.
- Using distinct sounds for different marker types.

**Related Patterns:** [Coded audio](#coded-audio), [CVD friendly communication](#cvd-friendly-communication)

**Barrier 4:** Managing multiple markers can become confusing.

**Consider:**
- Providing a list view of all placed markers with descriptions.
- Allowing markers to be named or tagged.
- Announcing when marker limits are approached.

**Related Patterns:** [High Contrast](#high-contrast)

---

### questing/achievements

Track, display, and manage objectives, goals, achievements, and quest progress throughout the game.

**Required for:** Character Progression, Adventure

#### Accessibility Barriers & Considerations

**Barrier 1:** Quest logs and achievement lists are presented as text-heavy interfaces.

**Consider:**
- Implementing text-to-speech for all quest descriptions and achievement names.
- Supporting platform screenreaders.
- Providing audio summaries of active quests.

**Related Patterns:** [Text to speech](#text-to-speech), [Screenreader support](#screenreader-support)

**Barrier 2:** Quest objectives and directions rely on visual map markers or directional indicators.

**Consider:**
- Providing audio waypoint guidance (Objective 200 meters northwest).
- Using audio beacons to indicate objective locations.
- Announcing objectives when they update or change.

**Related Patterns:** [Audio beacons](#audio-beacons), [Text to speech](#text-to-speech)

**Barrier 3:** Progress tracking is visual (progress bars, percentages) without audio equivalents.

**Consider:**
- Announcing progress percentages when checking quest status.
- Providing audio notifications for quest milestones (25%, 50%, 75%, complete).
- Using distinct sounds for different types of progress updates.

**Related Patterns:** [Coded audio](#coded-audio), [Text to speech](#text-to-speech)

**Barrier 4:** Achievement notifications may be visual-only pop-ups.

**Consider:**
- Playing distinctive sounds for achievement unlocks.
- Announcing achievement names and descriptions when unlocked.
- Allowing players to review recent achievements with audio support.

**Related Patterns:** [Coded audio](#coded-audio), [Text to speech](#text-to-speech)

**Barrier 5:** Complex quest requirements or nested objectives are cognitively demanding.

**Consider:**
- Breaking complex quests into clear, manageable steps.
- Highlighting or announcing the current active objective.
- Providing quest hints or simplified explanations.

**Related Patterns:** [High Contrast](#high-contrast), [Clear fonts and text](#clear-fonts-and-text), [Resizable text](#resizable-text)

---

### radio button - mutex selection

Select one option from a mutually exclusive set where selecting a new option automatically deselects the  previous one (e.g., difficulty levels, display modes).

**Required for:** Menu (textual), Combat (menu driven), Narrative Choice / Branching Paths

#### Accessibility Barriers & Considerations

**Barrier 1:** Gamers without sight cannot perceive visual menu elements to change them.

**Consider:**
- Implementing text-to-speech for menu options.
- Announcing the category name when entering the selection group.
- Using pre-recorded audio clips for common settings.

**Related Patterns:** [Text to speech](#text-to-speech), [Pre-recorded audio clips](#pre-recorded-audio-clips)

**Barrier 2:** Gamers without sight cannot tell which setting is currently selected.

**Consider:**
- Announcing the current setting when the menu element is highlighted (Difficulty: Normal, selected).
- Using distinct sounds for the selected option vs. unselected options.
- Announcing when selection changes (Normal deselected, Hard selected).

**Related Patterns:** [Text to speech](#text-to-speech), [Screenreader support](#screenreader-support)

**Barrier 3:** Partially sighted gamers can struggle with low contrast, small or hard to read interfaces.

**Consider:**
- Using clear fonts and text that are easier to read.
- Offering a high contrast option or, preferably, a high contrast default.
- Offering opaque backgrounds, preferably as a default but potentially as part of a high contrast profile.
- Making selected options visually distinct with multiple cues (color, size, icons).

**Related Patterns:** [Clear fonts and text](#clear-fonts-and-text), [CVD friendly communication](#cvd-friendly-communication), [High Contrast](#high-contrast), [Opaque background](#opaque-background)

**Barrier 4:** Understanding that options are mutually exclusive may not be clear.

**Consider:**
- Announcing that only one option can be selected when entering the group.
- Using consistent visual language for radio button groups.
- Grouping related options with clear section headers.

---

### select - atomic selection

**Required for:** Menu (textual), Character Progression, Class-Based Play /Role-play, Combat (menu driven), Construction, Management / Tycoon, Narrative Choice / Branching Paths, Rhythm / Timing, strategy, Puzzle

---

### select-menu

The player confirms a selection or activates a menu item to execute an action or navigate to a submenu.

**Required for:** Menu (textual)

#### Accessibility Barriers & Considerations

**Barrier 1:** Players may not know which button performs selection vs. navigation.

**Consider:**
- Using consistent button mappings for selection throughout the game.
- Announcing available actions when hovering over items (Press X to select).
- Providing clear visual button prompts.

**Barrier 2:** Accidental selections due to sensitive controls or unclear confirmation requirements.

**Consider:**
- Implementing optional confirmation prompts for important selections.
- Using a distinct selection confirmed sound or haptic feedback.
- Allowing brief undo or back functionality after selections.

**Related Patterns:** [Coded audio](#coded-audio)

**Barrier 3:** Players with sight loss need feedback to know their selection was registered.

**Consider:**
- Playing distinct confirmation sounds for successful selections.
- Announcing what was selected (Difficulty: Hard selected).
- Providing haptic feedback on selection.

**Related Patterns:** [Text to speech](#text-to-speech), [Coded audio](#coded-audio), [Digital control](#digital-control)

---

### sell building

The player removes a building or structure from the game world, typically receiving resources or currency  in return.

**Required for:** Construction, Management / Tycoon

#### Accessibility Barriers & Considerations

**Barrier 1:** Players with sight loss cannot easily identify which building to select for selling.

**Consider:**
- Providing text-to-speech descriptions of buildings when selected or scanned.
- Announcing building type, location, and current value when focused.
- Using audio beacons or navigation aids to locate buildings.

**Related Patterns:** [Text to speech](#text-to-speech), [Audio beacons](#audio-beacons)

**Barrier 2:** Confirmation dialogs or sell value information may only be visual.

**Consider:**
- Announcing sell values and confirmation prompts through text-to-speech.
- Providing audio confirmation of successful sales.
- Using distinct sounds for selling actions.

**Related Patterns:** [Text to speech](#text-to-speech), [Coded audio](#coded-audio)

**Barrier 3:** Accidentally selling important buildings due to unclear confirmation or selection.

**Consider:**
- Requiring explicit confirmation for selling actions.
- Announcing what will be sold before requiring confirmation.
- Providing undo functionality or sell cooldown period.

---

### slider - proportion selection

Adjust a value along a continuous or stepped range by moving a slider control, typically used for volume,  brightness, or other scalar settings.

**Required for:** Menu (textual), Combat (menu driven)

#### Accessibility Barriers & Considerations

**Barrier 1:** Analogue slider control is imprecise and difficult for players with motor impairments.

**Consider:**
- Supporting digital button presses for incremental adjustments.
- Implementing multiple adjustment speeds (fine and coarse).
- Allowing direct numerical input as an alternative.

**Related Patterns:** [Digital control](#digital-control)

**Barrier 2:** Players with sight loss cannot see the current slider position or value.

**Consider:**
- Announcing the current value as the slider moves (Volume: 75%).
- Using audio feedback that represents the value (e.g., volume changes audibly).
- Announcing minimum, maximum, and default values.

**Related Patterns:** [Text to speech](#text-to-speech), [Coded audio](#coded-audio)

**Barrier 3:** Visual-only slider representations don't convey the current value to blind players.

**Consider:**
- Providing numerical value announcements.
- Using positional audio cues (pitch or panning) to represent value.
- Implementing haptic feedback at regular intervals along the slider.

**Related Patterns:** [Text to speech](#text-to-speech), [Coded audio](#coded-audio)

**Barrier 4:** Small visual indicators are hard to see and manipulate for partially sighted players.

**Consider:**
- Making slider handles larger and high contrast.
- Displaying the numerical value prominently next to the slider.
- Using clear visual fill or progress indicators.

**Related Patterns:** [High Contrast](#high-contrast), [Clear fonts and text](#clear-fonts-and-text), [Resizable UI](#resizable-ui)

---

### special attack

The player executes a powerful or unique attack ability that is distinct from normal attacks, often with  limited uses, cooldowns, or resource costs.

**Required for:** Combat (continuous), Combat (multi-character turn-based)

#### Accessibility Barriers & Considerations

**Barrier 1:** Players with sight loss cannot see special attack animations, effects, or success indicators.

**Consider:**
- Using distinct, dramatic audio cues for special attack activation.
- Providing audio feedback for successful hits vs. misses.
- Announcing when special attacks are available or charged.

**Related Patterns:** [Coded audio](#coded-audio), [Text to speech](#text-to-speech)

**Barrier 2:** Complex button combinations or timing requirements are difficult for players with motor impairments.

**Consider:**
- Offering simplified input methods for special attacks (single button press).
- Implementing input buffering or queuing for special attacks.
- Providing hold-to-charge alternatives to complex sequences.

**Related Patterns:** [Digital control](#digital-control)

**Barrier 3:** Visual-only indicators of special attack availability (glowing icons, charge meters) are not accessible.

**Consider:**
- Announcing when special attacks are ready (Ultimate ability charged).
- Using rising audio cues to indicate charge progress.
- Providing haptic feedback when special attacks become available.

**Related Patterns:** [Text to speech](#text-to-speech), [Coded audio](#coded-audio)

**Barrier 4:** Aiming or targeting special attacks requires visual precision.

**Consider:**
- Providing auto-targeting or target lock for special attacks.
- Using audio targeting cues to indicate aim direction.
- Implementing area-of-effect attacks that reduce precision requirements.

**Related Patterns:** [Audio beacons](#audio-beacons)

---

### strategy

The player makes tactical or strategic decisions that affect gameplay, such as unit positioning, resource  allocation, tech tree choices, or long-term planning in strategy games.

**Required for:** strategy

#### Accessibility Barriers & Considerations

**Barrier 1:** Visual overview of strategic situations (maps, unit positions, resource distribution) is inaccessible to players with sight loss.

**Consider:**
- Providing text-to-speech summaries of strategic situations.
- Announcing unit counts, positions, and status information.
- Implementing audio scanning to explore the strategic state of the game.

**Related Patterns:** [Text to speech](#text-to-speech), [Audio beacons](#audio-beacons)

**Barrier 2:** Complex visual interfaces for strategic information are difficult to navigate without sight.

**Consider:**
- Organizing strategic information in navigable lists with audio feedback.
- Providing shortcuts to access specific strategic information.
- Supporting screenreader navigation of strategic interfaces.

**Related Patterns:** [Text to speech](#text-to-speech), [Screenreader support](#screenreader-support), [Navigate menu 2D](#navigate-menu-2d)

**Barrier 3:** Processing and comparing multiple sources of information simultaneously is cognitively demanding.

**Consider:**
- Providing strategic summaries that highlight key information.
- Offering AI advisors or recommendations.
- Breaking complex strategic information into digestible sections.

**Barrier 4:** Small text, icons, and map elements are difficult to see for partially sighted players.

**Consider:**
- Making strategic interfaces resizable with high contrast options.
- Using clear fonts and adequate text sizes.
- Providing zoom functionality for maps and strategic views.

**Related Patterns:** [Resizable UI](#resizable-ui), [High Contrast](#high-contrast), [Clear fonts and text](#clear-fonts-and-text), [Magnification](#magnification)

---

### team identification

The player must distinguish between their own team members and opposing team members, which is critical  for cooperative and competitive multiplayer games.

**Required for:** Sports [stub], Co-op Mechanics

#### Accessibility Barriers & Considerations

**Barrier 1:** Color-based team identification fails for players with color vision deficiency.

**Consider:**
- Using shapes, icons, and patterns in addition to colors to identify teams.
- Providing customizable team colors with CVD-friendly presets.
- Using distinct silhouettes or markers for different teams.

**Related Patterns:** [CVD friendly communication](#cvd-friendly-communication), [High Contrast](#high-contrast)

**Barrier 2:** Players with sight loss cannot visually distinguish team members.

**Consider:**
- Using distinct audio signatures for teammate vs. enemy actions and movements.
- Announcing team affiliation when targeting or focusing on characters.
- Providing audio callouts from teammates vs. enemies (using different voice processing).

**Related Patterns:** [Coded audio](#coded-audio), [Text to speech](#text-to-speech), [Audio beacons](#audio-beacons)

**Barrier 3:** Small or subtle team indicators may be missed during fast-paced gameplay.

**Consider:**
- Making team indicators prominent and clear (large icons, outlines).
- Positioning team indicators within the visual safe zone.
- Using multiple redundant indicators (color, icon, outline).

**Related Patterns:** [High Contrast](#high-contrast), [Visual safe zone](#visual-safe-zone), [Customisable UI / HUD](#customisable-ui-hud)

---

### text chat

Players communicate with others through typed text messages, either in real-time or asynchronously.

**Required for:** Co-op Mechanics

#### Accessibility Barriers & Considerations

**Barrier 1:** Players with sight loss cannot read incoming text messages.

**Consider:**
- Implementing text-to-speech for incoming chat messages.
- Announcing who sent each message.
- Providing audio cues when new messages arrive.

**Related Patterns:** [Text to speech](#text-to-speech), [Screenreader support](#screenreader-support), [Coded audio](#coded-audio)

**Barrier 2:** Players with sight loss cannot easily compose and send text messages.

**Consider:**
- Supporting screenreader input for text composition.
- Providing quick-reply options or message templates.
- Implementing voice-to-text for message composition.

**Related Patterns:** [Screenreader support](#screenreader-support), [Speech to text](#speech-to-text)

**Barrier 3:** Small text in chat windows is difficult to read for partially sighted players.

**Consider:**
- Making chat text resizable and high contrast.
- Using clear, readable fonts.
- Providing opaque backgrounds for chat text.

**Related Patterns:** [Resizable text](#resizable-text), [High Contrast](#high-contrast), [Clear fonts and text](#clear-fonts-and-text), [Opaque background](#opaque-background)

**Barrier 4:** Fast-scrolling chat can be overwhelming or difficult to follow.

**Consider:**
- Allowing chat scrollback and pause functionality.
- Providing filtering options to show only important messages.
- Announcing only messages directed at the player or from specific sources.

---

### unavailable

Options which cannot be selected in menus and interfaces are often greyed out or otherwise marked as unavailable.

**Required for:** Menu (textual), Combat (menu driven)

#### Accessibility Barriers & Considerations

**Barrier 1:** If the option can be selected but its unavailability is not indicated in audio, gamers without sight will not know why they can't select it. If it cannot be selected then they may not know it's there which can cause confusion.

**Consider:**
- Allowing the option to be focused/highlighted but not activated.
- Announcing when focusing unavailable items (New Game - locked, complete tutorial to unlock).
- Using a distinct sound effect when attempting to select unavailable items.
- Providing clear explanations of why items are unavailable.

**Related Patterns:** [Text to speech](#text-to-speech), [Coded audio](#coded-audio)

**Barrier 2:** Visual greying out may not be sufficient for partially sighted or color blind players.

**Consider:**
- Using multiple visual indicators (grayed out, crossed out, locked icon).
- Ensuring adequate contrast even for unavailable styling.
- Using text labels like LOCKED or UNAVAILABLE in addition to visual styling.

**Related Patterns:** [CVD friendly communication](#cvd-friendly-communication), [High Contrast](#high-contrast), [Clear fonts and text](#clear-fonts-and-text)

**Barrier 3:** Players may waste time trying to access unavailable options without clear feedback.

**Consider:**
- Providing immediate audio/visual feedback when hovering over unavailable items.
- Explaining requirements or conditions to unlock the option.
- Allowing filtering to hide unavailable options if desired.

---

### upgrade building

The player improves an existing building or structure to enhance its capabilities, increase production,  or unlock new features.

**Required for:** Management / Tycoon

#### Accessibility Barriers & Considerations

**Barrier 1:** Players with sight loss cannot easily identify which buildings can be upgraded or what upgrades are available.

**Consider:**
- Announcing upgrade availability when selecting or scanning buildings (Town Hall: upgrade available).
- Providing text-to-speech descriptions of upgrade options and benefits.
- Using audio cues to indicate upgrade-ready buildings.

**Related Patterns:** [Text to speech](#text-to-speech), [Audio beacons](#audio-beacons), [Coded audio](#coded-audio)

**Barrier 2:** Comparing upgrade options requires understanding complex visual information.

**Consider:**
- Providing clear audio summaries of upgrade effects (Increases production by 25%).
- Announcing cost vs. benefit for upgrade decisions.
- Reading out stat comparisons before and after upgrades.

**Related Patterns:** [Text to speech](#text-to-speech), [Object comparison](#object-comparison)

**Barrier 3:** Small text and complex upgrade trees are difficult to read and navigate.

**Consider:**
- Making upgrade interfaces resizable with high contrast.
- Using clear fonts and adequate spacing.
- Organizing upgrades in a logical, navigable structure.

**Related Patterns:** [Resizable text](#resizable-text), [High Contrast](#high-contrast), [Clear fonts and text](#clear-fonts-and-text), [Navigate menu 2D](#navigate-menu-2d)

**Barrier 4:** Progress indicators for upgrades in progress may only be visual.

**Consider:**
- Announcing upgrade completion through audio.
- Providing progress updates on request (50% complete, 2 minutes remaining).
- Using audio to indicate upgrade milestones.

**Related Patterns:** [Text to speech](#text-to-speech), [Coded audio](#coded-audio)

---

### voice chat

Players communicate with others through real-time voice communication, essential for team coordination  and social gameplay.

**Required for:** Co-op Mechanics

#### Accessibility Barriers & Considerations

**Barrier 1:** Players with hearing loss cannot hear voice communications from teammates.

**Consider:**
- Providing speech-to-text transcription of voice chat.
- Implementing visual indicators showing who is speaking.
- Offering text chat as an alternative communication method.

**Related Patterns:** [Speech to text](#speech-to-text), [Captions](#captions), [Visual sound effects](#visual-sound-effects)

**Barrier 2:** Players with speech impairments may have difficulty using voice chat.

**Consider:**
- Supporting text-to-speech for outgoing messages.
- Providing quick-voice-line options or preset callouts.
- Ensuring text chat is a fully viable alternative.

**Related Patterns:** [Text to speech](#text-to-speech)

**Barrier 3:** Distinguishing between multiple speakers can be difficult.

**Consider:**
- Providing visual indicators showing which player is speaking.
- Using spatial audio so voices come from character directions.
- Announcing speaker names with transcriptions.

**Related Patterns:** [Visual sound effects](#visual-sound-effects), [Binaural audio](#binaural-audio), [Surround sound](#surround-sound)

**Barrier 4:** Background noise and poor audio quality make voice chat hard to understand.

**Consider:**
- Implementing noise cancellation and audio enhancement.
- Allowing individual volume adjustment for each speaker.
- Providing audio profiles that boost voice frequencies.

**Related Patterns:** [Adjustable semantic audio profiles](#adjustable-semantic-audio-profiles), [Clean audio](#clean-audio)

---

## Accessibility Patterns

### Adjustable semantic audio profiles

By separating audio into profiles such as dialogue, music, sound effects (conveying meaning) and background  (providing atmosphere) these can then have their volumes independently adjustable. This enables a player to  increase the volume of audio that helps them while reducing the volume of other audio.  See also Clean audio.

#### Implementation Options

**Unity:**
- Use Audio Mixer to separate audio into groups (Dialogue, Music, SFX, Ambience)
- Create mixer groups for each audio category
- Expose volume parameters to settings menu
- Use Audio Mixer snapshots for different profiles

**Unreal Engine:**
- Organize sounds into hierarchical Sound Classes
- Use Sound Mix for dynamic volume adjustments
- Apply Sound Classes to sound cues
- Allow players to adjust volume per class in settings

#### Documentation & Resources

- Unity Audio Mixer documentation
- Unreal Sound Classes and Mix documentation

**Used by mechanics:** attack, cooldown, Perceive danger, Perceive environment state, voice chat

---

### Audio aiming

The relative position of a target from the crosshairs or reticule is communicated through audio cues such as  pitch, volume or rapidity of clicks. This gives a blind player the information they need to accurately aim at targets while preserving player agency.

#### Implementation Options

**Unity:**
- Custom implementation required using audio source positioning
- Calculate angle/distance between crosshair and target
- Modify audio parameters (pitch, volume, rate) based on proximity

**Unreal Engine:**
- Custom Blueprint implementation
- Use audio parameters to convey targeting information
- Implement using sound cues with parameter modulation

**Used by mechanics:** Aim

---

### Audio beacons

Audio beacons are sounds 'placed around' the user using immersive audio. They can act as a way to locate  objects in a virtual space, to annotate objects or to provide waypoints for navigation.

#### Implementation Options

**Unity:**
- Attach Audio Source to objects with 3D sound settings enabled
- Enable 'Spatialize' checkbox on Audio Source
- Use Microsoft Spatializer Plugin for cross-platform support
- Microsoft's Responsive Spatial Audio plugin provides drag-and-drop navigation beacons
- Use Audio Spatializer SDK for custom implementations

**Unreal Engine:**
- Add Ambient Sound actor to scene for beacon location
- Configure spatialization in Project Settings > Audio
- Use sound attenuation for distance-based effects
- Supports panning, soundfield, and binaural audio
- Third-party options: Resonance Audio, Steam Audio, Oculus Spatializer

#### Documentation & Resources

- Unity: https://docs.unity3d.com/Manual/AudioSpatializerSDK.html
- Unity: Microsoft Spatial Audio GitHub repository
- Unity: Microsoft Garage's Responsive Spatial Audio plugin (Unity Asset Store)
- Unreal: https://dev.epicgames.com/documentation/en-us/unreal-engine/spatialization-overview-in-unreal-engine

**Used by mechanics:** Aim, attack - continuous, block, locate opponant2D, move building, Movement2D, Perceive FoE, Perceive interactable, perceive marker, Perceive object state, Perceive objects, Perceive path, place building, place marker, questing/achievements, sell building, special attack, strategy, team identification, upgrade building

---

### Binaural audio

Binaural audio usually refers to replicating the way surround sound is encoded by our ears. This enables  surround sound to be delivered via headphones in a way that our brain can recreate the soundscape around us.

#### Implementation Options

**Unity:**
- Use Microsoft Spatializer Plugin with binaural rendering
- Enable spatialize on Audio Source components
- Configure for headphone output
- Oculus Spatializer plugin available

**Unreal Engine:**
- Built-in binaural rendering support
- Configure in Audio spatialization settings
- Microsoft Spatial Sound Plugin available for HoloLens 2 and mixed reality
- Oculus Spatializer plugin available

#### Documentation & Resources

- Unity: https://docs.unity3d.com/Manual/AudioSpatializerSDK.html
- Unreal: https://dev.epicgames.com/documentation/en-us/unreal-engine/spatialization-overview-in-unreal-engine

**Used by mechanics:** block, dodge, locate opponant2D, Perceive danger, perceive marker, Perceive path, voice chat

---

### CVD friendly communication

Colour Vision Deficiency (Colour Blindness) is a relatively common disability where people have trouble  distinguishing different colours. Information should not be communicated using colour alone but should  also use shape and pattern. CVD filters and can help but care should be taken not to create unnatural  colours (trees should be displayed as green but the uniforms of enemy soldiers in the trees should be  affected by the filter or be preselectable from a range of options or profiles). CVD is a spectrum so  unless a colour profile is tailored to a player it could make colours seem unnatural and break immersion.

#### Implementation Options

**Unity:**
- Color Blind Safe Palette API: Accessibility.VisionUtility.GetColorBlindSafePalette()
- Generates distinguishable colors for deuteranopia, protanopia, tritanopia
- ColorBlind Effect plugin (Project Wilberforce) from Asset Store
- Custom post-processing shaders using URP or Post-Processing Stack v2
- Apply post-processing filters to camera
- Use alternative color palettes in UI
- Combine color with shapes, patterns, icons
- Use Color Oracle desktop tool for real-time simulation

**Unreal Engine:**
- Built-in CVD Settings in Editor: Edit > Editor Preferences > Appearance > Accessibility
- Runtime support via SetColorVisionDeficiencyType Blueprint node
- Supports Deuteranope, Protanope, Tritanope types
- Custom colorblind correction using post-process materials and LUT
- Test visuals using editor preview modes
- Wanadev's unreal-colorblind-tool for LUT-based corrections

#### Documentation & Resources

- Unity: https://docs.unity3d.com/ScriptReference/Accessibility.VisionUtility.html
- Unity: Color Oracle (desktop tool)
- Unreal: https://dev.epicgames.com/documentation/en-us/unreal-engine/BlueprintAPI/Widget/Accessibility/SetColorVisionDeficiencyType

**Used by mechanics:** navigate menu 1D, object comparison, object description, perceive earnings, Perceive FoE, perceive marker, Perceive object state, place marker, radio button - mutex selection, team identification, unavailable

---

### Captions

Captions are lines of text within a users view that correspond to audio information. They can translate  between languages, provide a real-time transcript of speech for people who would struggle to hear or  understand spoken language or describe sounds for people with hearing loss. They may also encourage language  learning or reduce cognitive load by providing multi-channel communication.

#### Implementation Options

**Unity:**
- Chirp: XR Access Initiative's caption system for VR/AR (supports SRT format)
- A11YTK (Accessibility Toolkit): Context-aware subtitles with customization
- Unity Simple SRT: Basic SRT parser
- Custom implementations using Unity UI or TextMeshPro
- Include customizable font size, color, position
- Add speaker identification and sound effect captions
- Implement directional indicators for spatial sounds
- Provide scrim/background for readability

**Unreal Engine:**
- Built-in Subtitle System for basic functionality
- Better Captions Plugin: Fully replicated system with volume, attenuation, tone info
- Sound Subtitle System: Blueprint-based with directional indicators
- Add subtitle data to sound assets
- Configure subtitle display in Project Settings
- Use Subtitles and Closed Captions plugin API
- Follow BBC, Netflix, FCC standards
- Minimum 0.16s gap between subtitles
- Support speaker identification and customizable appearance

#### Documentation & Resources

- Unity: Chirp - https://github.com/XR-Access-Initiative/chirp-captions
- Unity: Unity Learn audio accessibility tutorial
- Unreal: Subtitles and Closed Captions documentation
- Best practices: BBC, Netflix, FCC subtitle standards

**Used by mechanics:** Perceive environment state, voice chat

---

### Clean audio

Dialogue and sound effects conveying information can have their volume boosted compared to other audio.  This could be a single toggle or a set of profiles (with non-information conveying audio being full,  reduced or muted). See also [Adjustable semantic audio profiles](#adjustable-semantic-audio-profiles).

#### Implementation Options

**Unity:**
- Use Audio Mixer with separate groups for dialogue and effects
- Implement ducking and side-chain effects
- Create mixer snapshots for clean audio profiles
- Expose parameters for runtime control

**Unreal Engine:**
- Use Sound Classes to categorize audio
- Implement Sound Mix for dynamic adjustments
- Create clean audio profiles that boost dialogue/effects
- Use Sound Attenuation for contextual volume control

**Used by mechanics:** voice chat

---

### Clear fonts and text

Avoid block capitals as these obscure the shape of words. Ensure easy to read fonts are available and are  preferably the default.

#### Implementation Options

**Unity:**
- Use TextMeshPro for better font rendering than legacy Text
- Recommended: Inter font family
- Set 12px base size minimum
- Avoid all-caps text
- Ensure high contrast against background
- Provide adequate line spacing

**Unreal Engine:**
- Support for TrueType and OpenType fonts
- Use Rich Text for styling options
- Avoid all-caps text
- Ensure readability with adequate sizing and spacing

#### Documentation & Resources

- Unity: TextMeshPro documentation
- Font recommendation: Inter font family at 12px minimum

**Used by mechanics:** character creation, character selection, checkbox - additive selection, levelling-up, navigate menu 1D, navigate menu 2D, object comparison, object description, perceive earnings, questing/achievements, radio button - mutex selection, slider - proportion selection, strategy, text chat, unavailable, upgrade building

---

### Coded audio

By designing sound effects for similar actions to have similar characteristics it is possible to  communicate actions that are happening through sound. This was done in Killer Instinct where a blind  player could tell whether an attack was high or low (for example) by the sound effect associated with  it. It is also used in God of War Ragnarok where there are sound effects for an unblockable or  undodgeable attacks.

#### Implementation Options

**Unity:**
- Design sound effect libraries with consistent characteristics
- Use Audio Mixer to apply consistent processing to sound categories
- Implement audio cue systems that map actions to distinctive sounds
- Use pitch, timbre, and rhythm to differentiate action types

**Unreal Engine:**
- Use Sound Cues to create consistent audio signatures
- Organize sounds into classes with shared characteristics
- Implement audio parameters that modify sounds consistently
- Use Sound Mix to maintain consistent audio profiles

**Used by mechanics:** Aim, attack, attack - continuous, block, character selection, checkbox - additive selection, combat mode, cooldown, crouch, dodge, enter menu, levelling-up, locate opponant2D, move building, Movement2D, navigate menu 2D, Perceive danger, perceive earnings, Perceive environment state, Perceive FoE, Perceive interactable, perceive marker, Perceive object state, Perceive objects, Perceive path, place building, place marker, questing/achievements, select-menu, sell building, slider - proportion selection, special attack, team identification, text chat, unavailable, upgrade building

---

### Customisable UI / HUD

Elements such as crosshairs and cursors should be customisable so they can be made large enough and high  contrast enough for partially sighted gamers but not too large for other gamers. Size, shape and colour  can all make a difference.

#### Implementation Options

**Unity:**
- Unity UI (uGUI): Canvas-based system with scaling options
- UI Toolkit: Modern UI system with styling and theming
- Canvas Scaler for resolution-independent UI
- Layout Groups for responsive layouts
- Custom shaders for UI effects
- Follow WCAG contrast requirements (3:1 minimum for focus)
- Implement resizable text and UI elements
- Use high contrast modes via themes

**Unreal Engine:**
- UMG (Unreal Motion Graphics): Widget-based UI system
- DPI scaling for different screen sizes
- Widget blueprints for custom UI
- Anchoring and canvas panels for responsive design
- Accessibility Toolkit available on Marketplace

#### Documentation & Resources

- Unity: https://www.foundations.unity.com/fundamentals/accessibility
- Unreal: UMG documentation
- WCAG contrast guidelines

**Used by mechanics:** Aim, combat mode, cooldown, Perceive environment state, Perceive interactable, Perceive object state, Perceive objects, team identification

---

### Digital control

Digital control is where any input can be performed with discrete button presses or actions. Analogue input  such as analogue joysticks or holding down keys to move a curser can make it hard for blind and partially  sighted people to follow where they are in an interface.

#### Implementation Options

**Unity:**
- Input System (New): Supports both analog and digital inputs
- Input Actions can be bound to multiple controls
- Processors for converting analog to digital
- Use Input Actions with 'Press' interaction
- Avoid requiring precise analog stick movements in menus

**Unreal Engine:**
- Enhanced Input System: Input Actions support both analog and digital
- Input Modifiers and Triggers for processing
- Use discrete button inputs for UI navigation
- Provide alternatives to analog controls

#### Documentation & Resources

- Unity: Input System documentation
- Unreal: Enhanced Input System documentation

**Used by mechanics:** attack, combat mode, crouch, emoji, enter menu, move building, Movement2D, navigate menu 1D, navigate menu 2D, place building, select-menu, slider - proportion selection, special attack

---

### High Contrast

Parts of a visual are made to 'stand out' by using contrasting colours. This is often used for text but  could also be used for symbols, the outlines of objects etc. WCAG contains a formula for determining the  contrast ratio between two colours.

#### Implementation Options

**Unity:**
- Use UI Toolkit theming for high contrast modes
- Apply post-processing effects for visual contrast
- Implement high contrast shaders for objects and UI
- Follow WCAG contrast guidelines (4.5:1 for normal text, 3:1 for large text)

**Unreal Engine:**
- Use UMG styling for high contrast UI
- Implement post-process materials for scene contrast
- Create high contrast widget themes
- Follow WCAG contrast guidelines

#### Documentation & Resources

- WCAG contrast ratio guidelines
- Unity UI Toolkit theming documentation

**Used by mechanics:** Aim, character creation, character selection, checkbox - additive selection, combat mode, cooldown, emoji, levelling-up, locate opponant2D, navigate menu 1D, navigate menu 2D, object comparison, object description, Perceive danger, perceive earnings, Perceive environment state, Perceive FoE, Perceive interactable, perceive marker, Perceive object state, Perceive objects, Perceive path, place building, place marker, questing/achievements, radio button - mutex selection, slider - proportion selection, strategy, team identification, text chat, unavailable, upgrade building

---

### Magnification

Part or all of the visuals are enlarged making them easier to see.

#### Implementation Options

**Unity:**
- Implement camera zoom functionality
- Use UI scaling for interface magnification
- Create magnifier glass effect with render textures

**Unreal Engine:**
- Implement camera zoom using field of view adjustments
- Use UMG scaling for UI magnification
- Create magnifier effects with scene capture components

**Used by mechanics:** strategy

---

### Opaque background

Transparent backgrounds behind text or icons can make them hard to read/perceive for partially sighted  people. Having an option to set opaque backgrounds (preferably as a default) can improve readability.

#### Implementation Options

**Unity:**
- Use UI Image Component with solid or semi-transparent backgrounds
- Custom shaders for consistent backgrounds
- Always provide opaque option, preferably as default

**Unreal Engine:**
- Use Border Brush with solid fill behind text
- Background Blur can help with readability
- Add background panels behind text elements

**Used by mechanics:** checkbox - additive selection, levelling-up, navigate menu 1D, navigate menu 2D, object description, perceive earnings, radio button - mutex selection, text chat

---

### Pre-recorded audio clips

Instead of using text-to-speech for audio access to immutable text such as menu options pre-recorded audio  can be nicer to listen to and give a better user experience.

#### Implementation Options

**Unity:**
- Import audio files: WAV, MP3, OGG formats supported
- Higher quality and better performance than runtime TTS
- Use for menu narration and fixed content

**Unreal Engine:**
- Import audio files: WAV, OGG formats supported
- Higher quality and better performance than runtime TTS
- Use for menu narration and fixed content

**Used by mechanics:** character creation, character selection, navigate menu 1D, object description, radio button - mutex selection

---

### Resizable UI

Onscreen interfaces can be made bigger to be easier to read and understand or smaller so they obscure less  of the screen.

#### Implementation Options

**Unity:**
- Use Canvas Scaler for resolution-independent UI
- Implement UI scale slider in settings
- Use Layout Groups for responsive layouts

**Unreal Engine:**
- DPI scaling in User Interface settings
- Implement UI scale settings for players
- Use anchors and size boxes for responsive design

**Used by mechanics:** cooldown, emoji, perceive earnings, slider - proportion selection, strategy

---

### Resizable text

Make sure that any text the player needs to read can be resized. Many partially sighted people benefit from  larger text and some people with extreme loss of peripheral vision may benefit from smaller text.

#### Implementation Options

**Unity:**
- Use Canvas Scaler with 'Scale With Screen Size'
- TextMeshPro: Vector-based text rendering with auto-sizing
- Minimum 12px font size, avoid fonts smaller than 9px
- Test at multiple resolutions

**Unreal Engine:**
- UMG Scaling: DPI Scale Rule in User Interface settings
- Size boxes and scale boxes for dynamic sizing
- Use size constraints and anchors for responsive text

#### Documentation & Resources

- Unity: TextMeshPro documentation
- Recommended minimum: 12px, avoid below 9px

**Used by mechanics:** levelling-up, navigate menu 1D, object comparison, object description, perceive earnings, questing/achievements, text chat, upgrade building

---

### Screenreader support

Many platforms (especially Android, iOS and PC) contain screenreaders. A screenreader is a piece of software  that parses metadata available in software and apps to provide verbal access to visual information. Enabling  a screenreader to provide accessibility for your game can be as easy as adding metadata to UI elements but  refer to documentation from platform providers to find out what you would need to do.

#### Implementation Options

**Unity:**
- Platform Integration: iOS UIAccessibility, Android TalkBack
- Windows: Limited NVDA/JAWS support
- Unity Accessibility Extensions: Open-source screen reader APIs
- UI Toolkit has basic accessibility support
- Requires platform-specific native code for comprehensive support
- Unity 6.3 mentioned to have expanded screen-reader support

**Unreal Engine:**
- Screen Reader Plugin: Base framework for custom implementations
- Slate Screen Reader Plugin: Production-ready for Slate UI
- Features: Accessible UI announcements, navigation, TTS integration, focus management
- Enable accessibility features in project settings

#### Documentation & Resources

- Unity: Unity Accessibility Extensions - https://unity-accessibility-extensions.readthedocs.io/
- Unreal: https://dev.epicgames.com/documentation/en-us/unreal-engine/blind-accessibility-features-overview-in-unreal-engine

**Used by mechanics:** character creation, checkbox - additive selection, emoji, levelling-up, navigate menu 1D, navigate menu 2D, object comparison, object description, questing/achievements, radio button - mutex selection, strategy, text chat

---

### Speech to text

Audio speech is converted into a stream of text.

#### Implementation Options

**Unity:**
- Platform-specific APIs: iOS Speech Framework, Android Speech Recognition
- Third-party plugins available on Asset Store
- Cloud services: Google Cloud Speech-to-Text, Azure Speech Services

**Unreal Engine:**
- Platform-specific implementations
- Third-party plugins available
- Cloud services integration possible

**Used by mechanics:** text chat, voice chat

---

### Surround sound

Providing audio through surround sound can help gamers with sight loss orient themselves.

#### Implementation Options

**Unity:**
- Native multi-channel audio output support
- Use Microsoft Spatializer, Oculus Spatializer, or Resonance Audio
- Configure Audio Source for 3D spatial audio
- HRTF support through spatializer plugins

**Unreal Engine:**
- Extensive native spatial audio features
- Supports multi-channel surround sound output
- Ambisonics: First Order Ambisonic support (Resonance Audio)
- Object-Based Audio via Wwise or other middleware

#### Documentation & Resources

- Unity: https://docs.unity3d.com/Manual/AudioSpatializerSDK.html
- Unreal: https://dev.epicgames.com/documentation/en-us/unreal-engine/spatialization-overview-in-unreal-engine

**Used by mechanics:** block, dodge, locate opponant2D, perceive marker, voice chat

---

### Text to speech

Written text is synthesised into speech and played audibly to the user.

#### Implementation Options

**Unity:**
- Platform-specific native plugins: iOS, Android, macOS using system TTS
- Windows: Limited native support via Windows Speech API
- ReadSpeaker AI: Professional TTS with 90+ voices in 30+ languages, no latency
- Eden AI Plugin: API-based TTS integration
- Unity Accessibility Extensions: Open-source TTS wrappers
- ReadSpeaker plugin offers runtime synthesis directly in Unity

**Unreal Engine:**
- Built-in TTS Plugin: Experimental Text-to-Speech plugin since UE 5.0
- Screen Reader Plugin: Expands TTS with richer accessibility features
- Slate Screen Reader Plugin: Built on base Screen Reader for Slate UI
- Use 'Add Default Channel' and 'Speak on Channel' nodes in Blueprints
- ReadSpeaker plugin available
- Wit.ai Voice SDK TTS (Meta)
- Runtime Text to Speech by Georgy Dev (900+ voices, 44 languages, offline)

#### Documentation & Resources

- Unity: https://unity-accessibility-extensions.readthedocs.io/
- Unity: ReadSpeaker - https://www.readspeaker.com/resources/unity/
- Unreal: https://dev.epicgames.com/documentation/en-us/unreal-engine/text-to-speech-quickstart-in-unreal-engine

**Used by mechanics:** attack - continuous, character creation, character selection, checkbox - additive selection, combat mode, cooldown, crouch, emoji, enter menu, levelling-up, move building, navigate menu 1D, navigate menu 2D, object comparison, object description, perceive earnings, Perceive environment state, Perceive FoE, Perceive interactable, perceive marker, Perceive object state, Perceive objects, Perceive path, place building, place marker, questing/achievements, radio button - mutex selection, select-menu, sell building, slider - proportion selection, special attack, strategy, team identification, text chat, unavailable, upgrade building, voice chat

---

### Visual safe zone

Players with a loss of peripheral vision may not be aware of important information placed around the edges  of the screen. They will likely know where to look for persistent UI elements but may miss temporarily  available information or information changes around the borders. A visual safe zone is the area from the  centre of the screen up to a virtual border where information the player may need to know should be placed.

#### Implementation Options

**Unity:**
- Define safe zone boundaries in UI design
- Use Canvas Safe Area component
- Test with various screen sizes and aspect ratios
- Place critical UI elements within safe zone

**Unreal Engine:**
- Define safe zone in UMG layouts
- Use safe zone widget for automatic adjustment
- Test across different display configurations
- Keep important information centralized

**Used by mechanics:** combat mode, team identification

---

### Visual sound effects

In a virtual space objects that make sounds can have captions or speech bubbles placed on them to make them  accessible for people with hearing loss.

#### Implementation Options

**Unity:**
- Custom implementation required
- Attach UI elements to sound sources
- Display directional indicators for off-screen sounds
- Show visual representations of audio events
- See closed caption tutorials with directional indicators

**Unreal Engine:**
- Sound Subtitle System: Marketplace asset with directional cones
- Custom Widgets triggered by sound cues
- Implement similar to caption systems with visual indicators
- Use UMG widgets positioned at sound source locations

#### Documentation & Resources

- Unity: Closed caption tutorials with directional indicators
- Unreal: Sound Subtitle System (Marketplace)

**Used by mechanics:** Perceive danger, Perceive environment state, Perceive interactable, voice chat

---

## General Resources

These resources provide additional guidance and tools for implementing accessibility features across different platforms.

### Unity Official Resources

- Audio Spatializer SDK: https://docs.unity3d.com/Manual/AudioSpatializerSDK.html
- Accessibility API: https://docs.unity3d.com/ScriptReference/Accessibility.VisionUtility.html
- Unity Foundations: https://www.foundations.unity.com/fundamentals/accessibility

### Unreal Engine Official Resources

- Blind Accessibility Overview: https://dev.epicgames.com/documentation/en-us/unreal-engine/blind-accessibility-features-overview-in-unreal-engine
- Text-to-Speech Quickstart: https://dev.epicgames.com/documentation/en-us/unreal-engine/text-to-speech-quickstart-in-unreal-engine
- Spatialization Overview: https://dev.epicgames.com/documentation/en-us/unreal-engine/spatialization-overview-in-unreal-engine
- Free Accessibility Course: Available through Unreal Online Learning

### Cross-Platform Resources

- Game Accessibility Guidelines: http://gameaccessibilityguidelines.com/
- XR Access Initiative: https://xraccess.org/
- IGDA Game Accessibility SIG: https://igda-gasig.org/

### Key Recommendations

- Plan early: Integrate accessibility from the start
- Use established patterns: Follow WCAG, BBC, Netflix standards
- Test with users: Include people with disabilities in testing
- Provide options: Let players customize accessibility features
- Document clearly: Ensure features are discoverable and well-documented

