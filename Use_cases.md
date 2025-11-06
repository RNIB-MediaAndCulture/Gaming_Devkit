# Gaming Use cases
This document aims to encompass the types of games that exist in order to identify accessibility barriers and offer suggested solutions. It is broadly inspired by object based programming where something can 'inherit' properties from parents. In this way it offers 'aspects of experience' which will embody aspects of a game. A first person shooter game will inherit the [Combat (first person)](#combat-first-person) aspect but may also inherit the [Exploration](#exploration) and [Team communication](#team-communication) aspect.   
The document then lists relevant mechanics for each aspect of experience. These are actions you might expect to perform as part of this aspect or ways in which you might expect to interact with it. These describe potential accessibility barriers and ways in which you might overcome those barriers. The suggestions of ways to overcome the barriers may point to accessibility design patterns.

## Aspects of Experience

### Menu (textual)
A menu is a part of almost every game and enables the player to set preferences, set game difficulty, choose which level to play 

Mechanics [checkbox - additive selection] , [enter menu] , [navigate menu 1D] , [navigate menu 2D] , [radio button - mutex selection] , [select-menu] , [slider - proportion selection]
### Character Progression
Players improve their character’s stats, skills, or gear over time. Can be tied to experience points, quests, or achievements.

Mechanics [levelling-up] ,  [object description] , [object comparison] ,  , [questing/achievements]  
### Class-Based Play /Role-play
Players take on specific roles with unique abilities (e.g., healer, tank, scout), often in team-based games. 

Mechanics [character creation] , [character selection]
### Combat (1v1)
A player uses a combination of attacks, blocks, jumps, crouches and horizontal movement to attack an opponent (either computer controlled or player controlled). 

Mechanics [attack]  , [block]  ,  [locate opponant2D] , [Movement2D]  , [Perceive attack]  

### Combat (beat 'em up)
The player fights through waves of enemies often in a side-scrolling or platform style game. Other characters may be friendly, neutral or unaligned (alliance can shift).

Mechanics [attack]  , [block]  ,  [locate opponant2D] , [Movement2D]  , [Perceive attack]  

### Combat (first-person) 
The player navigates a map attacking enemies which may be NPCs or other players. Other characters may be friendly, neutral or unaligned (alliance can shift).

Mechanics  [Assistant] , [attack]  , [block]  , [crouch] ,  [dodge] ,  [locate opponant2D] , [Movement2D]  , [Perceive attack]  , [Perceive FoE]

### Combat (menu driven)
Combat is turn based although the player or opponent may miss turns or have extra turns. Often the player may choose between 2 or more levels of attack, to block or to use inventory items such as healing potions.

Mechanics [checkbox - additive selection] , [enter menu] , [navigate menu 1D] , [navigate menu 2D] , [Perceive attack] , [radio button - mutex selection] , [select - atomic selection] , [slider - proportion selection] , [unavailable]

### Combat (multi-character synchronous)
Other characters may be friendly, neutral or unaligned (alliance can shift).

Mechanics  [attack - continuous]  , [combat mode],  [cooldown], [special attack] ,  [locate opponant2D] , [Movement2D]  , [Perceive attack]  , [Perceive FoE]

### Combat (multi-character turn-based)
Other characters may be friendly, neutral or unaligned (alliance can shift).

Mechanics [attack]  , [combat mode] ,  [locate opponant2D] , [Movement2D]  , [Perceive attack]  , [Perceive FoE]

### Construction
Players place, remove, or modify elements in the game world to create structures or solve spatial challenges. Common in sandbox and survival games.

Mechanics 

### Co-op Mechanics
Players work together with another player to achieve shared goals, often requiring coordination and complementary skills.

Mechanics [Team communication] , [place marker] , [perceive marker]


### Environmental Interaction
Players manipulate the environment directly—moving objects, activating switches, or using physics-based mechanics to solve problems or progress.

Mechanics [Perceive interactable] , [Perceive object state] , [Perceive environment state] 

### Exploration
The player has a large map to explore and movement through this environment is largely unrestricted.

Mechanics [Perceive collision] ,  [Perceive danger]  , [Perceive objects]  , [Perceive path]  , [Perceive direction](#perceive-direction)

> [!NOTE]
> Should Environmental Interaction and Exploration be merged?

### Management / Tycoon
Players oversee systems like cities, businesses, or ecosystems, making decisions to optimize performance or growth. Often involves resource balancing and strategic planning.

Mechanics [move building], [perceive earnings],  [place building], [sell building],  [upgrade building]

### Narrative Choice / Branching Paths
Players make decisions that affect the story or game world. These choices may lead to different outcomes or endings.

### Racing 
Players compete to cover a track faster than other players or faster than a set time limit.  

Mechanics 

###  Rhythm / Timing
Players interact with the game in sync with music or timed prompts. Found in rhythm games or mini-games within larger titles.


### Survival
Players must manage health, hunger, stamina, and other survival metrics while avoiding threats. Often includes crafting and exploration.



### Adventure
eg. Neverwinter nights, Zelda etc

todo:
 - merge with class-based play

### Simulation
The player can participate in a simulated world or activity. This could be through computer generated characters that the player controls or a first or third person simulated activity such as driving a train or powerwashing an area.

Mechanics

### Sports [stub]
Simulation of 

Mechanics [team identification]


### Stealth
Player guides their character to move around a map without alerting computer controlled enemies. This often involves knowing which way an enemy is facing and timing the players movements to avoid alerting them. Player may need to get their character to crouch. The enemies position may be communicated via visual or audio means or require the player to time their action.

Mechanics

### Strategy


Mechanics [Strategy](#strategy)

### Team communication

Mechanics [text chat] , [voice chat] , [emoji] , 

### Puzzle 
This refers to games which are entirely puzzle based rather than games such as adventure games that feature puzzles.

Mechanics








### Sandbox
Mechanics
> [!NOTE]
> While this is definately a gaming genre I'm not sure this is a gaming aspect. Sandbox games are defined as not having defined goals but the mechanics are the same as those of other game types such as survival games.





## Mechanics

### Perceive direction
In a virtual world the user needs to be able to navigate to a particular direction. This could be because they need to 'go north' or because they are being told that a quest item is in that direction. This is separate to knowing which 'path' to take.
#### Potential accessibility barriers
##### Direction is communicated visually and is not accessible to people with sightloss
 - Consider enabling the player to set a steady sonar ping in the direction that needs to be perceived. Consider [audio beacons](#audio-beacons)
 - Consider providing a ping only when the user is facing the direction to be perceived. Consider [audio beacons](#audio-beacons)


### Strategy

#### Potential accessibility barriers
##### Player is unable to enact effective strategies because they are missing some information needed to carry them out
 - Consider the information a player will need and ensure it is available visually and audibly. 
 - Consider common gameplay strategies and check that someone with a sensory loss has access to all the information needed to carry them out
##### Strategy is not a defining part of the game but is required for progress and players with cognitive difficulties may struggle to come up with effective strategies
 - Consider whether to offer hints or suggested strategies to move forward. The player should be able to turn off hints and care must be taken not to compromise gameplay by removing challenge.
##### Effective strategies require users to remember information which can be a problem for some people with cognitive difficulties 
 - Unless memory puzzles are core gameplay for the game avoid requiring players to memorise information
 - If memory is not part of the puzzle then allow players to lookup the information needed (the game creates a log or journal of important information). Ensure this is accessible to people with sight and hearing loss. 

## Accessible design patterns

### Adjustable contrast

### Adjustable semantic audio profiles
By separating audio into profiles such as dialogue, music, sound effects (conveying meaning) and background (providing atmosphere) these can then have their volumes independently adjustable. This enables a player to increase the volume of audio that helps them while reducing the volume of other audio. See also [Clean audio].

### Audio beacons
Audio beacons are sounds 'placed around' the user using immersive audio. They can act as a way to locate objects in a virtual space, to annotate objects or to provide waypoints for navigation.

### Audio description
Audio description or AD is a spoken soundtrack that describes visual information people with sight loss would otherwise miss. They are typically available of pre-recorded immutable content.

<!---
### Automated language translation
AI based software that can translate between two languages in realtime. Effectiveness may be hampered by strong accents or speech impediments, multiple voices talking at once or low bandwidth or unreliable internet connections. Accuracy is often higher between languages with more speakers or between languages in the same language families (ie French and Spanish, Turkish and Arabic, Dutch and German). Translation between written text may be more accurate.
--->
### Binaural audio
Binaural audio usually refers to replicating the way surround sound is encoded by our ears. This enables surround sound to be delivered via headphones in a way that our brain can recreate the soundscape around us. 

### Captions
Captions are lines of text within a users view that correspond to audio information. They can translate between languages, provide a real-time transcript of speech for people who would struggle to hear or understand spoken language or describe sounds for people with hearing loss. They may also encourage language learning or reduce cognitive load by providing multi-channel communication. 

### Clean audio
Dialogue and sound effects conveying information can have their volume boosted compared to other audio. This could be a single toggle or a set of profiles (with non-information conveying audio being full, reduced or muted). See also [Adjustable semantic audio profiles](#adjustable-semantic-audio-profiles).

### Clear fonts and text
Avoid block capitals as these obscure the shape of words. Ensure easy to read fonts are available and are preferably the default.  

<!---
### Clear Language
Using simple language. This means choosing simpler words (for instance 'use' rather than 'utilise'), shorter sentences and simpler sentence construction. People whose first language is not the same as the language presented or have cognitive issues or learning difficulties may benefit from simple language. Some Deaf people have sign language as a first language and can find written text difficult to understand or intimidating.  
--->
### Coded audio
By designing sound effects for similar actions to have similar characteristics it is possible to communicate actions that are happening through sound. This was done in Killer Instinct where a blind player could tell whether an attack was high or low (for example) by the sound effect associated with it. It is also used in God of War Ragnarok where there are sound effects for an unblockable or undodgeable attacks.

<!---
### Computer Vision
AI that takes an image as input and attempts to describe the image in text. This is a difficult task for AI to perform and can be improved if the context is narrowed. AI is expected to improve in performing this task but currently may focus on the wrong visual elements to describe, use strange or out of place language or hallucinate visual elements that are not present in the picture.
--->
### CVD friendly communication
Colour Vision Deficiency (Colour Blindness) is a relatively common disability where people have trouble distinguishing different colours. Information should not be communicated using colour alone but should also use shape and pattern. CVD filters and can help but care should be taken not to create unnatural colours (trees should be displayed as green but the uniforms of enemy soldiers in the trees should be affected by the filter or be preselectable from a range of options or profiles). CVD is a spectrum so unless a colour profile is tailored to a player it could make colours seem unnatural and break immersion.

... also UI elements ... 

### Customisable UI / HUD
Elements such as crosshairs and cursors should be customisable so they can be made large enough and high contrast enough for partially sighted gamers but not too large for other gamers. Size, shape and colour can all make a difference.

### Digital control 
Digital control is where any input can be performed with discrete button presses or actions. Analogue input such as analogue joysticks or holding down keys to move a curser can make it hard for blind and partially sighted people to follow where they are in an interface.

### High Contrast
Parts of a visual are made to 'stand out' by using contrasting colours. This is often used for text but could also be used for symbols, the outlines of objects etc. WCAG contains a formula for determining the contrast ratio between two colours.
<!---
### Human assistance
By using telecommunication links a human assistant can be brought in to aid a blind user. This could be to select items based on criteria ("Which of these pens is red?"), describe a document ("What is this letter about?") or to orient a user ("Which way is the seminar area? Can you tell me when I am facing towards it?"). The human assistant could be a paid employee of the platform, a support worker who is paid for by a person's work or government assistance scheme or an unpaid volunteer. Professional support workers are often bound by confidentiality agreements in their contracts.
--->
### Magnification
Part or all of the visuals are enlarged making them easier to see. 

### Mono audio
People who have hearing loss in one ear can benefit from stereo audio being flattened to mono audio so that no audio information is going just to the ear with hearing loss. 

### Pre-recorded audio clips
Instead of using text-to-speech for audio access to immutable text such as menu options pre-recorded audio can be nicer to listen to and give a better user experience.

<!---
### Remote spoken language interpreter
An interpreter who translates between two spoken languages via a telecommunications link. They may be funded by a user's workplace, by a service provider through a paid service covering multiple languages or may be funded by the user themselves.
--->
### Resizable text
Make sure that any text the player needs to read can be resized. Many partially sighted people benefit from larger text and some people with extreme loss of peripheral vision may benefit from smaller text.

### Resizable UI
Onscreen interfaces can be made bigger to be easier to read and understand or smaller so they obscure less of the screen.

<!---
### Respeaking
Users with speech impediments may use a respeaker to repeat their words after them. Respeakers are often familiar with the user and train on their voice so they can understand what they are saying. AI based automated respeakers may exist.
--->




### Screenreader support
Many platforms (especially Android, iOS and PC) contain screenreaders. A screenreader is a piece of software that parses metadata available in software and apps to provide verbal access to visual information. Enabling a screenreader to provide accessibility for your game can be as easy as adding metadata to UI elements but refer to documentation from platform providers to find out what you would need to do.  

### Speech to text
Audio speech is converted into a stream of text 

### Surround sound
Providing audio through surround sound can help gamers with sight loss orient themselves. 

<!---
### Tasklist
A list of actions which may help someone with cognitive disabilities keep track of actions they need to do or plan to do.
--->

### Text to speech
Written text is synthesised into speech and played audibly to the user

<!---
### Unambiguous language
Language where the intended meaning matches the literal meaning. Language used can sometimes have meanings that are at odds with the literal translation. Common examples are sarcasm, irony, and idioms. It is often assumed that readers and listeners can fill in the gaps using cultural knowledge or inference from context or tone of voice. This may not be the case for people from other languages or cultures or people who are neurodiverse and struggle to interpret social cues.
--->

<!---
### Video Sign Language Interpreter
A sign language interpreter who is presented to a Deaf sign language user over a telecommunications link and can hear the room and speak to it. They will translate speech into sign language for a user and translate the users sign language back into speech for other users. This can be tiring to do so sign language interpreters often work in pairs, switching over regularly.
--->
### Visual safe zone
Players with a loss of peripheral vision may not be aware of important information placed around the edges of the screen. They will likely know where to look for persistent UI elements but may miss temporarily available information or information changes around the borders. A visual safe zone is the area from the centre of the screen up to a virtual border where information the player may need to know should be placed. 

### Visual sound effects
In a virtual space objects that make sounds can have captions or speech bubbles placed on them to make them accessible for people with hearing loss. 



Also add:
 - https://gameaccessibilityguidelines.com/avoid-vr-simulation-sickness-triggers/ 
 - https://gameaccessibilityguidelines.com/if-the-game-uses-field-of-view-3d-engine-only-set-an-appropriate-default-for-the-expected-viewing-environment/
 - https://gameaccessibilityguidelines.com/ensure-interactive-elements-virtual-controls-are-large-and-well-spaced-particularly-on-small-or-touch-screens/
 - https://gameaccessibilityguidelines.com/ensure-sound-music-choices-for-each-key-objects-events-are-distinct-from-each-other/
 - https://gameaccessibilityguidelines.com/avoid-or-provide-option-to-disable-any-difference-between-controller-movement-and-camera-movement/
 - https://gameaccessibilityguidelines.com/if-the-game-uses-field-of-view-3d-engine-only-allow-a-means-for-it-to-be-adjusted/
 - https://gameaccessibilityguidelines.com/use-distinct-sound-music-design-for-all-objects-and-events/
