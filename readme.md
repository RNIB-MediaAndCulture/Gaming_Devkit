# RNIB Best Practice in Accessible Gaming (BPAG) 2023 

This is a draft of accessibility guidance to be provided to studios, developers and publishers of videogames to provide insight on how to best make said titles accessible to players across the spectrum of sight loss, including a complete lack of vision.

## The CAPS test
When making a game accessible it’s important to remember that it still needs to be enjoyable. It needs to retain **Challenge**, **Ambience**, **Participation** and **Story**.
### Challenge 
The game needs to challenge a player, or they will lose interest. 
### Ambience
Many games are set in rich worlds. This ambience needs to be communicated to players or they will be missing out on an important feature.
### Participation
If a game allows communication between players, then this needs to be accessible to enable gamers with sight loss to feel included. This includes trophies and the ability to discuss the game.
### Story
Gamers with sight loss need to be able to follow the story so cutscenes, in game exposition and banter between characters needs to be accessible.
If a game can be playable from beginning to end but fails the CAPS test then gamers with sight loss may not want to play it anyway. 

## Designing upwards theory: 
This theory is where we’ll begin as this is a starting point that everything else can feed into as part of implementation. However, we also understand that there are limitations to being able to implement accessibility so every approach might be different (for instance due to engines not allowing for easy building in of menu narration) which could change as projects progress.  Identifying these barriers and the right people who can assist in solving them can then allow future projects to have accessibility built in from the ground up as early as possible in development, thus not incurring retrofitting costs. Any serious barriers should be recorded on a centralised document. This means that if a developer has resources, then they can appoint a separate team or member of staff to resolving them. If not, then they can seek to fix them with any spare staff capacity between projects. This list should be as centralised as possible so that if teams working on separate projects face the same issue it can be fixed once and benefit both projects. 

Gamers across the spectrum of sight loss should be able to enjoy the same titles as everyone else, including players with absolutely no sight whatsoever. The features that can be of assistance, (menu narration, use of haptics for information etc) will not only assist blind players but anyone with greater levels of usable vision as well as other challenges (for instance if they can’t hear a cue that has a haptic equivalent).

If you instead were to design features for people with usable vision (colour-blindness/contrast filters for instance) you’d have the issue that only those who can see at that level of vision or above are having improved agency, whereas anyone who has less vision can’t benefit from those elements.

As a result you should look, where you can, to design upwards from no vision whatsoever so that as many people as possible can benefit.
As an underlying principle, any information that needs to be communicated should be communicated with high contrast visuals, through audio and preferably through a text free option. This should help blind and partially sighted people and anyone who is reading impaired including people with dyslexia or with English as a second language (including many sign language users). Multi-channel communication (communicating visually and audibly at the same time) is often preferable but whether to communicate something with ‘standard’ visuals, high contrast visuals or audio can be a choice delivered through the settings menus. 

Colour coding is a good way to communicate information but it should not be the only mechanism used because it may be inaccessible to people who are colour blind. 

Consider where accessibility can be the default. A good example is using sound design to communicate information. If a player can tell what type of attack is coming (high, low, unblockable etc) from the sound it makes then a blind player can react accordingly without having to change any settings. This simplifies menus, gives blind players a better experience and may even benefit sighted players who don’t realise that they are also reacting to the audio as well as the visual information.

## Platform specific requirements 
The accessibility needs of users do not change much depending on platform but the tools available may do. These may also create situational accessibility needs. If a web-based game can be played through a PC browser or a mobile phone then the size of onscreen text will need to be larger for the mobile phone in proportion to the screen size. The gamer using a mobile phone could be considered situationally partially sighted because they will face much of the same challenges as a partially sighted gamer may face using a larger screen. 

### PC/Mac/Web based
Windows and OSX have screen readers that will try to read out highlighted text and magnification software that will enlarge a portion of the screen. Depending on the development environment you use you may be able to make use of the screen reader to read out menus. 

PC gamers and Mac gamers may use magnification software to zoom in to games. This may be useful for menus or in game text where a game does not require a timely response. For high levels of magnification it is important that menus have a logical layout otherwise users may not be able to find menu options.

### Mobile phones and tablets
Mobile phones provide both challenges and accessibility tools. A smaller screen means that accessibility tools for partially sighted people are even more important because more people may need to use them. 

Larger mobile phone operating systems include suites of accessibility tools as standard. Screenreaders, magnification, high contrast modes, colour inversion and colour blindness filters are common and whether you can make use of these will depend on the development environment you choose. When selecting a development environment find out how much it allows use of the accessibility frameworks available and how much you will need to do yourself. Tools such as magnification and colour inversion will likely work regardless of the development environment you choose so it is worth testing with these to see how well they work with your game and whether you can do anything to improve the experience.

### Consoles 
Consoles have a rich selection of options for input and output. For output, consoles often allow for large screens, immersive soundscapes (through headphones or speaker arrays), and tactile feedback through controllers. For input, they may have buttons, joysticks, d-pads, microphones, cameras, accelerometers and motion sensors. All of these have accessibility potential but could also raise accessibility barriers. 

## Designing for Zoom 
Zoom is a feature that takes a section of the screen and enlarges it so that it fills the whole screen. It makes images bigger which can help partially sighted people but since it is only showing part of the screen it means the rest of the screen will not be visible. It also requires a separate navigation mechanism to choose which part of the screen you want to see. You might build zoom into your game, especially if the gameplay is turn-based rather than real-time but some platforms will enable zoom even if you do not build it in itself. Zoom functions can often magnify screens up to 16 times and, in the case of specialist software, even up to 64 times. 

If you decide to build zoom in yourself then it is worth speaking with accessibility consultants or magnification users to understand common interaction patterns for zoom software. Creating your own zoom will allow you to follow the focus with the zoomed area. Coupled with d-pad navigation this can make it easier to follow menus. 

A much simpler option however is to try to ensure your game works well with the Zoom options that the platform provides. When zoomed in the user is viewing the screen through a small window so it can be easy to lose navigational context. Try to make the layout of menus etc logical and predictable. Left align options that are above each other and avoid putting options in ‘islands’ with no other options or text near them. If an option is separate from the rest of the on-screen information then you can use ruled lines above, below or to the side of it to tie it in with some other text on the screen. 


## Puzzle games
When deciding what to speak to the user or what to highlight through the accessibility API’s of Android and iOS it is important to think about what information a user needs and prioritise the information they want to hear first. 

A good example of giving users the information they need is sukodu. Sudoku is a game with a 9 by 9 grid which is broken down into nine 3 by 3 blocks. Some cells in the grid have numbers in and the player needs to put numbers in the other cells so that any particular number does not occur twice in the same row, column or block. A user needs to know which numbers are in the same row or column as a particular cell and which numbers are present in the block. You could require a user to move left and right to hear which other numbers are present in a row but this will feel very clunky. You can add a feature to read out the relevant numbers ie. “row, 2 5 7, column 5 8 6 1, block 9 6 4 2” which will help for easy sudoku. Some tactics need more information however. In a row spanning over three blocks where the number 2 hasn’t been filled in and all three of the cells in the centre block are full then if there is a 2 anywhere inside the left block you know that the row in the right block contains a 2. This is because the row must have a 2 in it but the 2 in that row isn’t in the left block (because then it would appear twice in the same block) or the centre block (because there isn’t an empty cell). To enable a screenreader user to use this tactic you need to communicate the information that the centre block is full while trying not to give too strong a hint. The aim of the game is to use logic and screenreader users should be allowed to realise that logic themselves. You could communicate this information by grouping the numbers together with pauses to denote the edge of blocks. If the user is in the left block and hears “row, 3, 4 7 9, 6 5, column, 4, 5 9, 1 3, block, 3 4 8 2 5 7” then then have enough information to deduce that the empty cell in the right hand block of that row is a 2. They have been given the information to solve that piece of the puzzle but without too heavy a hint (which reduces the challenge) or being required to move all along the row (which needlessly increases the challenge). When deciding what to speak try to include the information players will need for more advanced tactics but without dropping too heavy a hint.

Crosswords are another good example. A crossword is a word puzzle where words need to be placed in rows and columns of cells in a, usually, irregular lattice such that each cell contains one letter and some of the cells will be part of two different words. Rows and columns are usually numbered with a set of clues to solve that will tell you what word is needed for a row or column. As words are placed in the lattice this will inform the user of some of the letters that are parts of other words that the clues indicate. They may read a clue and already know that the second letter is t and the fifth one is r. A user may then want to cycle through the lattice to find words that already have some of the letters filled in. To do this they will want to hear the progress for each word ie. “6 letters, second letter t, fifth letter r” before having to listen to the clue. Another common tactic after hearing a clue is to get a hint by solving the clue of a word that intersects the one they want to solve. This means the accessible gameplay should attempt to enable behaviour whereby after hearing a clue a user can then hear the clues to words that intersect the first word, solve these and return to the first word. This may be done with bespoke commands such as “hear intersecting clues” but may also be done by allowing users to move up, down, left and right through the lattice and hearing the clues that apply to a given cell. For instance, when walking through 5 across and landing on an intersectional cell the user could be told it is the third letter of 7 down and be given the clue for 7 down. The user can then keep going left and right to hear more of 5 across or press up or down to move into 7 down. When designing accessibility for puzzle games with common gameplay patterns those gameplay patterns should be accommodated by the accessibility features and design.

## Menu/UI Narration 
Menu and User Interface (UI) narration, hereafter simply referred to as “narration”, is a feature that allows menu items and other elements in a game to be spoken, primarily via synthesised speech.  This means that those with no vision or who have trouble seeing the screen for whatever reason can navigate menus unaided.
Examples: Gears 5, Sea Of Thieves, The Last Of Us Parts I and II, God Of War Ragnarok  

### Adjustable Speech
Narration as defined above should be adjustable in terms of its speed.  After all, just like we all read at different paces, we also all listen and comprehend at different rates.  If a player needs information quickly and can understand the speech at a much faster rate, they should be able to speed up the rate at which the narration is being spoken. Many screen reader users will listen to speech at over 300 words per minute [ ] and sometimes as fast as 500 words per minute. With the amount of variability between users it’s best to offer as much granularity in speeds as is practical.
Examples: Diablo IV, Sea Of Thieves and any game that has screen reader compatibility on PC

### Across all screens
From the very first onboarding elements, accessibility features such as narration should be present to allow players to set up the game as they desire, without the need for additional assistance. This includes elements such as brightness sliders or screen calibration, which normally appear before any accessibility settings are shown. As demonstrated by God Of War Ragnarok, a voiced prompt could tell the user how to enable said narration functionality, so as not to turn away players who might be confused by the voice coming from their game.
Examples: The Last Of Us Parts I and II, Gears 5 Horde and Escape modes

## Menu and UI navigation

### DPad navigation:
Allowing players to use digital directional movement as opposed to a cursor-based system will not only allow gamers across the spectrum of sight loss to more efficiently navigate menus, maps and other elements, but also assist those outside of that demographic who have issues with cursor-based menus.

When you have no sight whatsoever, you have no sense of where the cursor is on the screen other than via a large amount of patience and practice that a sighted person wouldn’t have to put in, if the menu has audio cues that clearly indicate you’re focused on an item for example.

Accessing menus and interface elements using free moving cursers can cause problems for people with sight loss or dexterity issues. Blind users have no context for where a free moving curser is until it hits a menu iteman interactive element (and that’s only if the menu itemelement has an audible or tactile cue). If your game is accessible through magnification, then users with high magnification settings may also find they are lost with no visual markers near enough to the curser to tell them where they are. Users with dexterity issues or non-standard input devices may also have trouble with the precision of landing on a menu iteman element.

Enabling a user to move between menu items with a single button press can help in all these areas. In a menu Ffeedback to the user should also give enough context to navigate the menu. Speech should make it clear when the user is on a submenu and what type of control is highlighted. Toggles, sliders and radio buttons have different behaviours when selected and a blind user needs to know which one they are using. This could be explicitly stated in the speech by saying “toggle”, “slider” or “radio button” or indicated some other way as long as it is clear and consistent. 

### In-game navigation
Games that allow players to explore at will can be hard to navigate for players who cannot see the offered paths easily (or at all). Though some games can allow players to move through the world by pressing a button and have the camera turn, there are also other ways to make this work, including audio cues (see below). Enabling players to roam freely in an open world while still being able to follow both main and side quests is a difficult balance and, at the time of writing this advice, one that has not been achieved to our knowledge. Players will need to be able to select which quest to pursue and the game will need to communicate path markers and quest items appropriately, including ‘hidden’ or discoverable items where the player must find the location themselves. Maps should be made as accessible as possible using contrast, magnification and potentially simplification or colour coding. If a map window tells you information about that region such as which quests and quest objects are available in that region, then this should be read out. 

**Audio cues:**

Audio cues are a key part of gaming with sight loss. They are both the medium in which information is delivered and that the game is experienced and understood. Audio cues should be clear and distinct but should also fit within the game’s universe so as not to break immersion. You don’t always have to use accessibility specific cues either, for instance an enemy’s attack audio could give enough of an audio cue to parry it in an action setting without being able to see it coming and without needing an extra accessibility cue, as can be seen in God Of War 2018 and Star Wars Jedi Survivor .

Making it clear when a player can do things like jump or traverse or when a status changes such as when they are low on health can vastly improve the level of agency a player has and reduce the need for sighted assistance. An accessible mechanism for interrogating status, such as health or ammo, may also benefit gamers.  This should be player triggered and should speak out any important status elements and/or show them with high contrast or magnification. The game may or may not pause on this screen to enable a player to read through or listen to their status without dying. 

Audio cues can also be used for navigation as an alternative to having the camera turn to point the player at the next objective. This gives a greater feeling of space and freedom to the player rather than complete linearity. Examples of this can be seen in Gears 5’s Navigation Ping: Escape Mode feature, which also includes high contrast visual elements to let even more people take advantage of the trail it leaves to lead players through areas.

**Audio Description**

Audio description is a medium that’s long been present in film, TV and theatre, but has only recently become recognised as a core part of the gaming space as of 2020. Though trailers from companies like Ubisoft, Activision Blizzard and Sony Santa Monica are examples of where this has been applied with reference to trailers, videogames still haven’t caught up as of 2023 other than a couple examples, namely The Last Of Us Part I for cinematics and Stories Of Blossom having audio description integrated throughout.

Implementing these to relay descriptions of character actions, gestures or sequences allows players to understand your story where otherwise they will miss key details or plot points.

**Descriptions viewable in-game as official channel**

If someone can’t see the visuals of the worlds you’ve created, the characters, the locations, the weapons, the items, a lot can be lost in terms of immersion. Having a way to view descriptions of key characters, items, locations etc as a player progresses, as well as audio glossaries for enemies and their attacks, could massively help with the increased level of understanding a player without sight can have of your world. Consider whether information is needed synchronously while a gamer is playing the game or asynchronously through glossaries, bestiaries and other sources of information that a player can look up later. Including artistic context while a player is playing will likely increase enjoyment but full descriptions of environments, enemies, objects, NPCs etc may be better suited to an asynchronous in-game reference.

## Aiming:
If your game requires use of a reticle for aiming, for whatever purpose (i.e. even if your game is not combat-focused), though lock-on aiming is an option, explore the possibilities of utilising audio and haptic feedback to allow players with no sight to aim with more freedom and know what they’re targeting.  For instance, in a target rich environment where differing enemies can take priority, allow players to distinguish what enemy they want to lock onto and target.

### Haptic feedback
Haptic feedback from controllers has historically just been used for immersion.  However, recent advances like the PlayStation 5 DualSense haptic feedback capabilities have allowed for increased accessibility-related information to be conveyed.

Used not just for immersion but for information relay (how much health you have, when a bar is filling up for an attack etc). There are currently few examples of best practice, so it is worth testing with users to ensure that mechanisms are useful and not distracting.

### High Contrast Filter
Low vision players may find it difficult to distinguish key elements such as interactive objects or non-player characters from the rest of the environment. This can be addressed by implementing a high-contrast mode in which the game environment and other static objects are displayed in a greyscale colour palette, while important or interactive objects are displayed in bright colours that stand out to low vision players. 

Consistent colour-coding of game elements with similar properties can be used to further help low vision players. For example, representing all hazards as red allows the low vision player to quickly identify them in the environment. This can be done through coloured outlines or halos or the whole object can be coloured as a block. Players should be given options to which colours are used so that they can choose those that best suit their vision. Allow a lot of variance in the colours available. Green and red are typically used for safety and danger but red/green colour blindness is one of the most common types so if you just allowed different shades or green and red then they may not stand out to some people.

Large Text Size with Clear, Readable Font/Readable Text
On-screen text can be a barrier to low vision players being able to play or access all parts of a video game. 

Text that is too small for the low vision player to read will cause those players to either strain to read it or miss it entirely. This can be addressed by making the default text size large enough for low vision players to read comfortably, or by giving the player the option to make the text larger. 

Text size is important, but large text with poor readability can also be a barrier to low vision players. Use a clear, wide font like Ariel or Verdana, and avoid using ornate, cursive, narrow or otherwise difficult to read fonts. If a more decorative font is used then there should be an option to revert to a simpler more readable font.

Use both upper-case and lower-case letters where possible. Using only upper-case letters works well for titles or main headings, but it will have a significant negative impact on the readability on longer sections of text. The shape of words (ie when bits of letters stick up or hang down from the word) gives usable information for partially sighted people to recognise the word. Block capitals have a rectangular shape which makes them harder to read.

The contrast between text and background affects how easy it is to read. Avoid overlaying text on images or video without a contrasting box behind them and provide options for this background to be opaque (or make it opaque by default). The WCAG guidelines have a metric for colour contrast which can tell you how different two colours are.    Allowing the player to choose the text and background colour scheme will make it more accessible to some low vision players.

Colourblindness filters
Colourblindness is a condition where parts of the eye that discern colours are missing or not working as standard. Colourblindness filters applied across the whole game (including menus) can ensure that colours have as much contrast as possible and can make the game easier to play for people who are colourblind. 

Large Text Size with Clear, Readable Font/Readable Text
On-screen text can be a barrier to low vision players being able to play or access all parts of a video game. 

Text that is too small for the low vision player to read will cause those players to either strain to read it or miss it entirely. This can be addressed by making the default text size large enough for low vision players to read comfortably, or by giving the player the option to make the text larger. 

Text size is important, but large text with poor readability can also be a barrier to low vision players. Use a clear, wide font like Ariel or Verdana, and avoid using ornate, cursive, narrow or otherwise difficult to read fonts. If a more decorative font is used then there should be an option to revert to a simpler more readable font.

Use both upper-case and lower-case letters where possible. Using only upper-case letters works well for titles or main headings, but it will have a significant negative impact on the readability on longer sections of text. The shape of words (ie when bits of letters stick up or hang down from the word) gives usable information for partially sighted people to recognise the word. Block capitals have a rectangular shape which makes them harder to read.

The contrast between text and background affects how easy it is to read. Avoid overlaying text on images or video without a contrasting box behind them and provide options for this background to be opaque (or make it opaque by default). The WCAG guidelines have a metric for colour contrast which can tell you how different two colours are.    Allowing the player to choose the text and background colour scheme will make it more accessible to some low vision players.

Designing for Zoom 
Zoom is a feature that takes a section of the screen and enlarges it so that it fills the whole screen. It makes images bigger which can help partially sighted people but since it is only showing part of the screen it means the rest of the screen will not be visible. It also requires a separate navigation mechanism to choose which part of the screen you want to see. You might build zoom into your game, especially if the gameplay is turn-based rather than real-time but some platforms will enable zoom even if you do not build it in itself. Zoom functions can often magnify screens up to 16 times and, in the case of specialist software, even up to 64 times. 

If you decide to build zoom in yourself then it is worth speaking with accessibility consultants or magnification users to understand common interaction patterns for zoom software. Creating your own zoom will allow you to follow the focus with the zoomed area. Coupled with d-pad navigation this can make it easier to follow menus. 

A much simpler option however is to try to ensure your game works well with the Zoom options that the platform provides. When zoomed in the user is viewing the screen through a small window so it can be easy to lose navigational context. Try to make the layout of menus etc logical and predictable. Left align options that are above each other and avoid putting options in ‘islands’ with no other options or text near them. If an option is separate from the rest of the on-screen information then you can use ruled lines above, below or to the side of it to tie it in with some other text on the screen. 

Scalable User Interfaces
A well designed and informative user interface (UI) plays an important role of conveying information to the player. However, the size and placement of UI elements can present accessibility barriers to low vision players. 

Small UI elements are a common accessibility issue for low vision players. Scalable user interfaces can resolve this. Allow the player to increase the size of UI elements to make them more readable during gameplay. If there is a maximum value at which the layout and functionality are maintained, consider allowing the player to increase the UI scale beyond this. Though this may cause UI elements to overlap and some useful information to be lost, these increased UI sizes may be useful to some low vision players. 

Allowing the player to adjust the scale and position of individual UI elements is another way to improve their readability by low vision players. Including this level of customisation allows players to enlarge and increase the visibility of UI elements they find most difficult to see without increasing the size of less useful elements or those for which no scaling is needed. 
Examples: Warframe, Tom Clancy’s The Division 2

Cooperative play
The aim of making a game accessible should be to enable a blind and partially sighted person to play it completely independently. The heart of the matter however is to enable a blind and partially sighted player to enjoy the game and allowing cooperative play can do this. This could be where different members of a team take on different tasks such as in Sea of Thieves or where two players could control the same character with a sighted player handling the tasks that require vision. 
Notes Section (add)
1.	Sight loss conditions and manifestations
2.	
3.	Glossary:
-	Screen readers
-	Magnification
-	High contrast modes
-	Colour inversion 
-	Colour blindness filters, 
-	Accessibility framework, 
-	Development environment, 
-	Asynchronous in-game reference


[link to CAPS test](https://github.com/RNIB-MediaAndCulture/Gaming_Devkit/blob/main/readme.md#the-caps-test)

 
Tentative timeline:
20 September:  Share with internal stakeholders
4 October: Share draft with external stakeholders
18 October: Share draft with industry after review 
1 Nov: Final comments from all involved
15 Nov: Final draft after reviewing comments 

(Acceptable delay 4 weeks – wrap editorial work before Christmas break).
 


