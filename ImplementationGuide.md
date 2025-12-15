# Accessibility Design Patterns - Unity & Unreal Implementation Guide

This document provides implementation guidance from Unity and Unreal Engine for each accessibility design pattern identified in your game accessibility catalogue.

---

## Audio Beacons / Spatial Audio

### Unity
- **Built-in Support**: Unity provides spatial audio through Audio Source components with 3D sound settings
- **Microsoft Spatializer Plugin**: Cross-platform spatializer for Windows and Android with efficient DSP processing
- **Implementation**:
  - Attach Audio Source to objects
  - Enable "Spatialize" checkbox
  - Use Audio Spatializer SDK for custom implementations
  - Microsoft's "Responsive Spatial Audio for Immersive Gaming" plugin provides drag-and-drop accessibility features including navigation beacons and spatial audio clouds
- **Documentation**: 
  - https://docs.unity3d.com/Manual/AudioSpatializerSDK.html
  - Microsoft Spatial Audio GitHub repository
  - Microsoft Garage's Responsive Spatial Audio plugin (Unity Asset Store)

### Unreal Engine
- **Built-in Support**: Comprehensive spatialization system including panning, soundfield, and binaural audio
- **Microsoft Spatial Sound Plugin**: Available for HoloLens 2 and mixed reality, includes hardware offload support
- **Third-Party Options**: Resonance Audio, Steam Audio, Oculus Spatializer
- **Implementation**:
  - Add Ambient Sound actor to scene
  - Configure spatialization in Project Settings > Audio
  - Use sound attenuation for distance-based effects
- **Documentation**: https://dev.epicgames.com/documentation/en-us/unreal-engine/spatialization-overview-in-unreal-engine

---

## Text-to-Speech (TTS)

### Unity
- **Native TTS Options**:
  - Platform-specific native plugins for iOS, Android, macOS (using system TTS)
  - Windows: Limited native support via Windows Speech API
- **Third-Party Plugins**:
  - **ReadSpeaker AI**: Professional TTS plugin with 90+ voices in 30+ languages, embedded engine with no latency
  - **Eden AI Plugin**: API-based TTS integration
  - **Unity Accessibility Extensions**: Open-source project providing TTS wrappers
- **Implementation Approaches**:
  - Use platform screenreaders where available
  - Implement custom TTS for UI narration
  - ReadSpeaker plugin offers runtime synthesis directly in Unity
- **Documentation**: 
  - Unity Accessibility Extensions: https://unity-accessibility-extensions.readthedocs.io/
  - ReadSpeaker: https://www.readspeaker.com/resources/unity/

### Unreal Engine
- **Built-in TTS Plugin**: Experimental Text-to-Speech plugin included since UE 5.0
- **Screen Reader Plugin**: Expands TTS with richer accessibility features
- **Slate Screen Reader Plugin**: Built on base Screen Reader, specifically for Slate UI
- **Implementation**:
  - Enable Text To Speech plugin in Project Settings
  - Use "Add Default Channel" and "Speak on Channel" nodes in Blueprints
  - Screen Reader plugin provides accessible announcements and UI element vocalization
- **Third-Party Options**:
  - ReadSpeaker plugin (also available for Unreal)
  - Wit.ai Voice SDK TTS (Meta)
  - Runtime Text to Speech by Georgy Dev (900+ voices, 44 languages, offline)
- **Documentation**: https://dev.epicgames.com/documentation/en-us/unreal-engine/text-to-speech-quickstart-in-unreal-engine

---

## High Contrast / CVD-Friendly Communication

### Unity
- **Color Blind Safe Palette API**: `Accessibility.VisionUtility.GetColorBlindSafePalette()` - generates distinguishable colors for deuteranopia, protanopia, tritanopia
- **Post-Processing Filters**:
  - ColorBlind Effect plugin (Project Wilberforce) - Asset Store
  - Custom post-processing shaders using URP or Post-Processing Stack v2
- **Third-Party Tools**:
  - Color Oracle (desktop tool for real-time simulation)
  - Multiple GitHub repositories for colorblind simulation shaders
- **Implementation**:
  - Apply post-processing filters to camera
  - Use alternative color palettes in UI
  - Combine color with shapes, patterns, icons
- **Asset Store**: Multiple colorblind simulation packages available

### Unreal Engine
- **Built-in CVD Settings**: 
  - Editor has colorblind preview modes (Edit > Editor Preferences > Appearance > Accessibility)
  - Runtime support via `SetColorVisionDeficiencyType` Blueprint node
- **Types Supported**: Deuteranope, Protanope, Tritanope
- **Post-Processing**: Can implement custom colorblind correction using post-process materials and LUT (Look-Up Tables)
- **Implementation**:
  - Use Color Vision Deficiency settings in Project Settings
  - Apply runtime adjustments through Blueprint
  - Test visuals using editor preview modes
- **Tools**: 
  - GitHub repositories with colorblind simulation materials
  - Wanadev's unreal-colorblind-tool for LUT-based corrections
- **Documentation**: https://dev.epicgames.com/documentation/en-us/unreal-engine/BlueprintAPI/Widget/Accessibility/SetColorVisionDeficiencyType

---

## Captions / Subtitles

### Unity
- **Open-Source Solutions**:
  - **Chirp**: XR Access Initiative's caption system for VR/AR (supports SRT format)
  - **A11YTK (Accessibility Toolkit)**: Context-aware subtitles with customization options
  - **Unity Simple SRT**: Basic SRT parser
- **Custom Implementations**: Many tutorials available for building subtitle systems
- **Features to Include**:
  - Support for SRT or other subtitle formats
  - Customizable font size, color, position
  - Speaker identification
  - Sound effect captions (not just dialogue)
  - Directional indicators for spatial sounds
- **Best Practices**:
  - Follow CVAA requirements for multiplayer games
  - Provide scrim/background for readability
  - Allow player customization
- **Resources**: 
  - Unity Learn audio accessibility tutorial
  - Chirp: https://github.com/XR-Access-Initiative/chirp-captions

### Unreal Engine
- **Built-in Subtitle System**: Basic subtitle functionality included
- **Enhanced Options**:
  - **Better Captions Plugin**: Fully replicated system with volume, attenuation, and tone information
  - **Sound Subtitle System**: Blueprint-based with directional indicators
  - **UMG Cinematics**: For text overlays and cinematic subtitles
- **Implementation**:
  - Add subtitle data to sound assets
  - Configure subtitle display in Project Settings
  - Use Subtitles and Closed Captions plugin API
- **Best Practices** (from "Making Subtitles That Don't Suck"):
  - Follow BBC, Netflix, FCC standards
  - Minimum 0.16s gap between subtitles
  - Support for speaker identification
  - Customizable appearance
  - Small caps for sound effects
- **Marketplace**: Multiple subtitle plugins available

---

## Screen Reader Support

### Unity
- **Platform Integration**:
  - iOS: UIAccessibility integration
  - Android: TalkBack support
  - Windows: Limited NVDA/JAWS support
- **Unity Accessibility Extensions**: Open-source project providing screen reader APIs
- **UI Toolkit**: Has some basic accessibility support for screen readers
- **Implementation Challenges**: Unity lacks comprehensive built-in support; developers must use platform-specific native code
- **Upcoming**: Unity 6.3 mentioned to have expanded screen-reader support

### Unreal Engine
- **Screen Reader Plugin**: Base framework for custom implementations
- **Slate Screen Reader Plugin**: Production-ready for Slate UI
- **Features**:
  - Accessible UI element announcements
  - Navigation through interface elements
  - Text-to-speech integration
  - Focus management
- **Requirements**: Must enable accessibility features in project settings first
- **Documentation**: https://dev.epicgames.com/documentation/en-us/unreal-engine/blind-accessibility-features-overview-in-unreal-engine

---

## Customizable UI / HUD

### Unity
- **UI Systems**:
  - **Unity UI (uGUI)**: Canvas-based system with scaling options
  - **UI Toolkit**: Modern UI system with styling and theming
- **Features**:
  - Canvas Scaler for resolution-independent UI
  - Layout Groups for responsive layouts
  - Custom shaders for UI effects
- **Accessibility Considerations**:
  - WCAG contrast requirements (3:1 minimum for focus)
  - Resizable text and UI elements
  - Clear fonts (Inter recommended at 12px base)
  - High contrast modes via themes

### Unreal Engine
- **UMG (Unreal Motion Graphics)**: Widget-based UI system
- **Slate**: Low-level UI framework
- **Features**:
  - DPI scaling for different screen sizes
  - Widget blueprints for custom UI
  - Anchoring and canvas panels for responsive design
- **Accessibility Toolkit**: Marketplace asset with pre-made customizable accessibility features

---

## Coded Audio / Adjustable Semantic Audio Profiles

### Unity
- **Audio Mixer**: 
  - Separate audio into groups (Dialogue, Music, SFX, Ambience)
  - Exposed parameters for runtime volume control
  - Ducking and side-chain effects
- **Implementation**:
  - Create mixer groups for each audio category
  - Expose volume parameters to settings menu
  - Use Audio Mixer snapshots for different profiles

### Unreal Engine
- **Sound Classes and Mix**:
  - Organize sounds into hierarchical classes
  - Sound Mix for dynamic volume adjustments
  - Sound Attenuation for spatial audio control
- **Implementation**:
  - Define Sound Classes in Project Settings
  - Apply classes to sound cues
  - Allow players to adjust volume per class
  - Use "Adjustable semantic audio profiles" pattern

---

## Binaural Audio / Surround Sound

### Unity
- **Native**: Unity Audio supports multi-channel audio output
- **Spatializers**: Microsoft Spatializer, Oculus Spatializer, Resonance Audio
- **HRTF Support**: Through spatializer plugins
- **Implementation**: Same as Audio Beacons section above

### Unreal Engine
- **Native Support**: Extensive spatial audio features including binaural rendering
- **Ambisonics**: First Order Ambisonic support (Resonance Audio)
- **Object-Based Audio**: Via Wwise or other middleware
- **Documentation**: Comprehensive spatialization documentation in UE

---

## Resizable Text / UI

### Unity
- **Dynamic Scaling**: Use Canvas Scaler with "Scale With Screen Size"
- **TextMeshPro**: 
  - Vector-based text rendering
  - Auto-sizing options
  - Better quality at different scales
- **Best Practices**:
  - Minimum 12px font size
  - Avoid fonts smaller than 9px
  - Test at multiple resolutions

### Unreal Engine
- **UMG Scaling**: 
  - DPI Scale Rule in User Interface settings
  - Size boxes and scale boxes for dynamic sizing
- **Rich Text**: Support for styled text with size variations
- **Implementation**: Use size constraints and anchors for responsive text

---

## Digital Control

### Unity
- **Input System (New)**: 
  - Supports both analog and digital inputs
  - Input Actions can be bound to multiple controls
  - Processors for converting analog to digital
- **Implementation**:
  - Use Input Actions with "Press" interaction
  - Avoid requiring precise analog stick movements in menus

### Unreal Engine
- **Enhanced Input System**:
  - Input Actions support both analog and digital
  - Input Modifiers and Triggers for processing
- **Implementation**:
  - Use discrete button inputs for UI navigation
  - Provide alternatives to analog controls

---

## Clear Fonts and Text

### Unity
- **Recommended**: Inter font family
- **TextMeshPro**: Better font rendering than legacy Text
- **Best Practices**:
  - No all-caps (reduces word shape recognition)
  - 12px base size
  - High contrast against background
  - Adequate line spacing

### Unreal Engine
- **Font Assets**: Support for TrueType and OpenType fonts
- **Rich Text**: Styling options for improved readability
- **Best Practices**: Same as Unity - avoid all-caps, ensure readability

---

## Opaque Background

### Unity
- **UI Image Component**: Use solid color or semi-transparent backgrounds behind text
- **Shader Options**: Custom shaders for consistent backgrounds
- **Best Practice**: Always provide opaque option, preferably as default

### Unreal Engine
- **Border Brush**: Use border widgets with solid fill
- **Background Blur**: Can help with readability
- **Implementation**: Add background panels behind text elements

---

## Pre-recorded Audio Clips

### Unity & Unreal Engine
- **Both engines fully support audio asset import**
- **Formats**: WAV, MP3, OGG (Unity); WAV, OGG (Unreal)
- **Use Case**: For menu narration and fixed content instead of TTS
- **Benefits**: Higher quality, better performance than runtime TTS

---

## Visual Sound Effects

### Unity
- **Custom Implementation Required**: No built-in system
- **Approach**:
  - Attach UI elements to sound sources
  - Display directional indicators
  - Show visual representations of audio
- **Examples**: See closed caption tutorials with directional indicators

### Unreal Engine
- **Sound Subtitle System**: Marketplace asset with directional cones
- **Custom Widgets**: Can be triggered by sound cues
- **Implementation**: Similar to caption systems with added visual indicators

---

## Additional Accessibility Resources

### Unity
- **Official**: Limited dedicated accessibility documentation
- **Community**: Unity Accessibility Extensions (open-source)
- **Support Article**: "Can I implement accessibility features in my Unity game?"
- **Learning Resources**: Unity Learn audio accessibility pathway

### Unreal Engine
- **Official Accessibility Course**: Free 43-minute course covering key features
- **Documentation**: Comprehensive blind accessibility features guide
- **Marketplace**: Growing number of accessibility-focused assets
- **Resources**: https://dev.epicgames.com/documentation/en-us/unreal-engine/blind-accessibility-features-overview-in-unreal-engine

---

## Key Findings Summary

### Unity Accessibility Status
- **Strengths**: Flexible, many third-party solutions, good community resources
- **Weaknesses**: Limited built-in accessibility features, requires more custom implementation
- **Best For**: Projects with development time for custom solutions, mobile platforms (good native TTS support)

### Unreal Engine Accessibility Status
- **Strengths**: More built-in accessibility features (especially UE5+), official accessibility course, better screen reader foundation
- **Weaknesses**: Some features still experimental, fewer third-party specific solutions
- **Best For**: Projects requiring robust built-in features, PC/console development

### General Recommendations
1. **Plan early**: Integrate accessibility from the start, not as an afterthought
2. **Use established patterns**: Follow WCAG, BBC, Netflix standards for UI/captions
3. **Test with users**: Include people with disabilities in testing
4. **Provide options**: Let players customize accessibility features to their needs
5. **Document clearly**: Ensure accessibility features are discoverable and well-documented

---

## Links to Official Documentation

### Unity
- Audio Spatializer SDK: https://docs.unity3d.com/Manual/AudioSpatializerSDK.html
- Accessibility API: https://docs.unity3d.com/ScriptReference/Accessibility.VisionUtility.html
- Unity Foundations (includes accessibility guidelines): https://www.foundations.unity.com/fundamentals/accessibility

### Unreal Engine
- Blind Accessibility Overview: https://dev.epicgames.com/documentation/en-us/unreal-engine/blind-accessibility-features-overview-in-unreal-engine
- Text-to-Speech Quickstart: https://dev.epicgames.com/documentation/en-us/unreal-engine/text-to-speech-quickstart-in-unreal-engine
- Spatialization Overview: https://dev.epicgames.com/documentation/en-us/unreal-engine/spatialization-overview-in-unreal-engine
- Free Accessibility Course: Available through Unreal Online Learning

### Cross-Platform Resources
- Game Accessibility Guidelines: http://gameaccessibilityguidelines.com/
- XR Access Initiative: https://xraccess.org/
- IGDA Game Accessibility SIG: https://igda-gasig.org/
