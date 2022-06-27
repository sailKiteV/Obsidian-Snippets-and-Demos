# Other Little Things
A collection of snippets and things that don't quite need their own directory. Entries prefixed by an asterisk `*` have an implementation for the [Style Settings](https://github.com/mgmeyers/obsidian-style-settings) plugin by mgmeyers. Instructions for using these snippets may be found [below](#instructions).

---
- \**[Text Selection Colors](https://github.com/sailKiteV/Obsidian-Snippets-and-Demos/blob/master/OtherLittleThings/TextSelectionColors.css)*: Change the color of the text, background, and caret for selected text. Optionally increase the width of the caret. Credit to Murf#2728 on the [Obsidian Members Group](https://obsidian.md/community) Discord server for the original snippet; i just dressed it up a bit.
- \**[Link Colors](https://github.com/sailKiteV/Obsidian-Snippets-and-Demos/blob/master/OtherLittleThings/LinkColors.css)*: Change the colors of the text for internal, unresolved, and external links.
- \**[View Mode Icons](https://github.com/sailKiteV/Obsidian-Snippets-and-Demos/blob/master/OtherLittleThings/ViewModeIcons.css)*: Swaps the default Editing and Reading View icons (to be indicative of *state* rather than an *action*). Only has one Style Settings option right now, which is to toggle on a custom icon for Source Mode Editing View. Icons cannot be changed with Style Settings (due to limitations of how `url()` works in CSS), but *can* be changed manually in the snippet itself.

---
## Instructions
1. Copy the snippet text into your own snippet, or download the snippet.
2. Place or make sure that the snippet is in your vault's snippets folder (which can be accessed from Obsidian's Appearance settings).  
    a. Refresh your snippets if it does not appear.
3. Enable the snippet (also in Appearance settings).
4. Change properties as desired.  
    a. If using Style Settings: Go to the "Plugin options" entry for Style Settings, and there should be a new section for the associated snippet. Modify settings as desired.  
    b. Else: Change the assigned values for properties in the CSS snippet to be whatever you like.
