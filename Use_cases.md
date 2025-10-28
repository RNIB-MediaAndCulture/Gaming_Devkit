# Gaming Use cases
This document aims to encompass the types of games that exist in order to identify accessibility barriers and offer suggested solutions. It is broadly inspired by object based programming where something can 'inherit' properties from parents. In this way it offers 'aspects of experience' which will embody aspects of a game. A first person shooter game wil inherit the [First-person shooter](link) aspect but may also inherit the [Exploration] (link) and [Team communcation](link) aspect.   
The document then lists relevant mechanics for each aspect of experience. These are actions you might expect to perform as part of this aspect or ways in which you might expect to interact with it. These describe potential accessibility barriers and ways in which you might overcome those barriers. The suggestions of ways to overcome the barriers may point to accessibility design patterns.

## Aspects of Experience

### Class-Based Play
 Players take on specific roles with unique abilities (e.g., healer, tank, scout), often in team-based games. This can overlap with RPG but is distinct in multiplayer contexts.
### Character Progression
Players improve their character’s stats, skills, or gear over time. Can be tied to experience points, quests, or achievements.
### Co-op Mechanics
Players work together to achieve shared goals, often requiring coordination and complementary skills.
### construction
Players place, remove, or modify elements in the game world to create structures or solve spatial challenges. Common in sandbox and survival games.
### Management / Tycoon
 Players oversee systems like cities, businesses, or ecosystems, making decisions to optimize performance or growth. Often involves resource balancing and strategic planning.
### Environmental Interaction
Players manipulate the environment directly—moving objects, activating switches, or using physics-based mechanics to solve problems or progress.
### Survival
Players must manage health, hunger, stamina, and other survival metrics while avoiding threats. Often includes crafting and exploration.
### Narrative Choice / Branching Paths
Players make decisions that affect the story or game world. These choices may lead to different outcomes or endings.
###  Rhythm / Timing
Players interact with the game in sync with music or timed prompts. Found in rhythm games or mini-games within larger titles.


### Racing 
Players compete to cover a track faster than other players or faster than a set time limit.  
#### Relevant Mechanics

### Fighting (Beat 'em up)
A player uses uses a combination of attacks, blocks, jumps, crouches and horizontal movement to attack an opponant (either computer controlled or player controlled). 
#### Relevant Mechanics
[Perceive attack]  , [attack]  , [block]  , [Movement2D]  , [locate opponant2D] 
### Exploration
The player has a large map to explore and movement through this environment is largely unrestricted.
#### Relevant Mechanics
[Perceive collision] ,  [Perceive danger]  , [Perceive objects]  , [Perceive path]  , [Perceive direction](#perceive-direction)
### RPG
The player controls a character which may either be fully created for them or may be highly customisable often from a given set of races, classes and alignments. Focus is on advancing a storyline and developing their chosen character. 
### Simulation
The player can participate in a simulated world or activity. This could be through computer generated characters that the player controls or a first or third person simulated activity such as driving a train or powerwashing an area.
#### Relevant Mechanics

### Sports

#### Relevant Mechanics

### Strategy
#### Relevant Mechanics

### Stealth
Player guides their character to move around a map without alerting computer controlled enemies. This often involves knowing which way an enemy is facing and timing the players movements to avoid alerting them. Player may need to get their character to crouch. The enemies position may be communicated via footsteps.
#### Relevant Mechanics

### Team communication

#### Relevant Mechanics

### Puzzle Game
#### Relevant Mechanics


### First-person shooter  <- Combat (single character)
The player navigates a map attacking enemies which may be NPCs or other players. 
#### Relevant Mechanics

### Combat (multiple character synchronous)

### Combat (multiple character turn-based)

### Combat (menu driven)

### Sandbox
#### Relevant Mechanics

## Mechanics

### Perceive direction
In a virtual world the user needs to be able to navigate to a particular direction. This could be because they need to 'go north' or because they are being told that a quest item is in that direction. This is seperate to knowing which 'path' to take.
#### Potential accessibility barriers
##### Direction is communicated visually and is not accessible to people with sightloss
 - Consider enabling the player to set a steady sonar ping in the direction that needs to be perceived. Consider [audio beacons](#audio-beacons)
 - Consider providing a ping only when the user is facing the direction to be perceived. Consider [audio beacons](#audio-beacons)





## Accessible design patterns

### Audio beacons
Audio beacons are sounds 'placed around' the user using immersive audio. They can act as a way to locate objects in a virtual space, to annotate objects or to provide waypoints for navigation.
<!---
### Automated language translation
AI based software that can translate between two languages in realtime. Effectiveness may be hampered by strong accents or speech impediments, multiple voices talking at once or low bandwidth or unreliable internet connections. Accuracy is often higher between languages with more speakers or between languages in the same language families (ie French and Spanish, Turkish and Arabic, Dutch and German). Translation between written text may be more accurate.
--->
### Captions
Captions are lines of text within a users view that correspond to audio information. They can translate between languages, provide a real-time transcript of speech for people who would struggle to hear or understand spoken language or describe sounds for people with hearing loss. They may also encourage language learning or reduce cognitive load by providing multi-channel communication. 
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
### High Contrast
Parts of a visual are made to 'stand out' by using contrasting colours. This is often used for text but could also be used for symbols, the outlines of objects etc. WCAG contains a formula for determining the contrast ratio between two colours.
<!---
### Human assistance
By using telecommunication links a human assistant can be brought in to aid a blind user. This could be to select items based on criteria ("Which of these pens is red?"), describe a document ("What is this letter about?") or to orient a user ("Which way is the seminar area? Can you tell me when I am facing towards it?"). The human assistant could be a paid employee of the platform, a support worker who is paid for by a person's work or government assistance scheme or an unpaid volunteer. Professional support workers are often bound by confidentiality agreements in their contracts.
--->
### Magnification
Part of the visuals are enlarged making them easier to see. 

### Mono audio
People who have hearing loss in one ear can benefit from stereo audio being flattened to mono audio so that no audio information is going just to the ear with hearing loss. 
<!---
### Remote spoken language interpreter
An interpreter who translates between two spoken languages via a telecommunications link. They may be funded by a user's workplace, by a service provider through a paid service covering multiple languages or may be funded by the user themselves.

### Respeaking
Users with speech impediments may use a respeaker to repeat their words after them. Respeakers are often familiar with the user and train on their voice so they can understand what they are saying. AI based automated respeakers may exist.
--->
### Speech to text
Audio speech is converted into a stream of text 

<!---
### Tasklist
A list of actions which may help someone with cognitive disabilities keep track of actions they need to do or plan to do.
--->

### Text to speech
Written text is synthesised into speech and played audibly to the user

<!---
### Unambigouous language
Language where the intended meaning matches the literal meaning. Language used can sometimes have meanings that are at odds with the literal translation. Common examples are sarcasm, irony, and idioms. It is often assumed that readers and listeners can fill in the gaps using cultural knowledge or inference from context or tone of voice. This may not be the case for people from other languages or cultures or people who are neurodiverse and struggle to interpret social cues.
--->

<!---
### Video Sign Language Interpreter
A sign language interpreter who is presented to a Deaf sign language user over a telecommunications link and can hear the room and speak to it. They will translate speech into sign language for a user and translate the users sign language back into speech for other users. This can be tiring to do so sign language interpreters often work in pairs, switching over regularly.
--->

### Visual sound effects
In a virtual space objects that make sounds can have captions or speech bubbles placed on them to make them accessible for people with hearing loss. 


