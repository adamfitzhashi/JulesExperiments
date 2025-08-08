# Bardic Inspiration Macro for Roll20

This document provides the code for a Roll20 macro for the D&D 5e Bardic Inspiration feature, along with instructions on how to use it.

## A Note on D&D Editions

This macro is based on the rules for Bardic Inspiration as presented in the D&D 5th Edition Player's Handbook. At the time of creation, specific rules for the "2024 Edition" were not available, so this macro uses the widely-known and established 5e rules for level progression of the inspiration die (d6, d8, d10, d12).

## Macro Code

Copy the entire block of code below to use in Roll20:

```
/em @{selected|character_name} plays a stirring tune for @{target|token_name}!
&{template:default} {{name=Bardic Inspiration}} {{inspiration=?{Inspirational Phrase?|A song of courage for the fighter|"Fear not the shadow, swift and keen"|A mystic chant of powers unseen|"By gods' own might, your spirit burns"|"The hunter's focus now returns"|A tale of heroes, bold and grand}}}
/w "@{target|character_name}" You feel inspired! You can add a [[?{Bard Level?|Level 1-4,d6|Level 5-9,d8|Level 10-14,d10|Level 15+,d12}]] die to one ability check, attack roll, or saving throw in the next 10 minutes.
```

## How to Create the Macro in Roll20

1.  **Open the Collections Tab:** In your Roll20 game, navigate to the sidebar and click on the "Collections" tab (it looks like a bulleted list).
2.  **Add a New Macro:** In the "Macros" section, click the "+ Add" button.
3.  **Name the Macro:** Give your macro a name, for example, `Bardic-Inspiration`.
4.  **Paste the Code:** In the "Actions" text box, paste the macro code you copied from above.
5.  **Save the Macro:** Click the "Save Changes" button at the bottom of the editor.
6.  **(Optional) Show in Macro Bar:** If you want a quick-access button for your macro, check the "Show in macro bar" option. This will place a button at the bottom of your screen.

## How to Use the Macro

1.  **Select Your Bard's Token:** Click on your character's token on the map to select it.
2.  **Run the Macro:** Either type `#Bardic-Inspiration` (or whatever you named it) in the chat, or click the button in your macro bar.
3.  **Choose an Inspirational Phrase:** A pop-up will appear with a dropdown menu of inspirational phrases. Choose one that fits the moment.
4.  **Select Your Target:** The cursor will change, and you will be prompted to select a target. Click on the token of the ally you want to inspire.
5.  **Choose Your Bard's Level:** A second pop-up will appear asking for your Bard's level range. Select the correct range.
6.  **Done!** The macro will now execute. It will post a public message in the chat with your chosen phrase, and send a private message (a "whisper") to the targeted player with the details of their new Bardic Inspiration die.
