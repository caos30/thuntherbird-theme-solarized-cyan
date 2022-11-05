# Thunderbird theme: Solarized Cyan by caos30

This is an attempt to transform color look of Thunderbird to the "solarized" palette. It's quite easy: 

1. customize the colors on the file manifest.json
2. create a zip with only that file and put it a name like: solarized-cyan-caos30-001@sample.themes.thunderbird.net.zip
3. install it on Thunderbird section for plugins/themes
4. customize manually on Settings of Thunderbird some colors (see instructions below): tags, redaction text and background.

What does it look? Something like this:

![First screenshot](/screenshot-01.png?raw=true "INBOX screenshot with color tags")
![Second screenshot](/screenshot-02.png?raw=true "Redaction window of new emails")
![Third screenshot](/screenshot-03.png?raw=true "Third party plugin CardBook")

### Official documentation

- https://developer.thunderbird.net/add-ons/web-extension-themes
- https://webextension-api.thunderbird.net/en/latest/theme.html#theme-themetype

### Instructions to generate the .xpi file (theme/plugin file)

You can download and install the XPI file in this repo, or you can:

1. Edit the manifest.json file
2. Zip it with this command on linux console:

```
zip solarized_caos30-1.2-tb.xpi manifest.json
```

Alternative: zip the manifest.json file and change its extension to xpi


### Color scheme to put on manifest.json

    "colors":{
      "frame": "#00141a", //<--- background-color for tabs bar, bookmark bar (under tabs bar) and bottom bar
      "frame_inactive": "#152428", //<-- INACTIVE above elements
      "tab_selected": "transparent", //<-- background color ACTIVE tab on tabs bar
      "tab_text": "#2aa198", 98afaf //<--- text color for ACTIVE tab on tabs bar
      "tab_line": "#2aa19888", //<--- 2px top border of the ACTIVE tab on tabs bar
      "tab_loading": "#dddddd", //<--- for circle-icon on tab text (i think only useful for web browser)
      "tab_background_text": "#829696", //<--- text color for tabs bar and menu bar 
      "bookmark_text": "#2aa198", //<--- text color for bookmark bar
      "button_background_active":"#82969666",
      "button_background_hover":"#ffffff18",
      "toolbar": "#001f28", //<-- background color for the bookmark bar
      "toolbar_field": "#00141a", //<--- background search box NOT FOCUSED
      "toolbar_field_text": "#2aa198", //<--- text color for search box NOT FOCUSED 
      "toolbar_field_highlight": "#00141a", //<--- border of FOCUSED search box 
      "toolbar_field_highlight_text": "#2aa198", //<--- text color for search box FOCUSED
      "toolbar_field_border": "#4ac1b888", //<--- border of NOT FOCUSED search box
      "toolbar_field_focus": "#00141a", //<--- background search box FOCUSED
      "toolbar_field_text_focus": "#2aa198", //<--- text color FOCUSED search box 
      "toolbar_field_border_focus": "#4ac1b888", //<--- border color FOCUSED search box
      "toolbar_top_separator": "#002b36", //<--- TOP border between bookmark bar and tab bar 
      "toolbar_bottom_separator": "#002b36", //<--- BOTTOM border between bookmark bar and tab bar 
      "toolbar_vertical_separator": "#002b36", //<--- VERTICAL border between bookmark bar and tab bar 
      "sidebar": "#002b36", //<--- background color for the vertical left panel (mailboxes/folders tree)
      "sidebar_text": "#829696", //<--- text color for the vertical left panel
      "sidebar_highlight": "rgba(255,255,255,.2)", //<--- bg color for THE highlighted element on tree
      "sidebar_highlight_text": "#ccc", //<--- text color for THE highlighted element on tree
      "sidebar_border": "#001f28", //<--- border color for the vertical left panel
      "popup": "#001217", //<--- background color for popup messages and main menu popup (right-top-corner button)
      "popup_text": "#7d9b9b", //<--- text color
      "popup_border": "#002d3a", //<--- border color
      "popup_highlight": "#e06502", //<--- background color for mouse over effect on element
      "popup_highlight_text": "#111111" //<---  text color for mouse over effect on element
}



### Suggested TAG colors to set on general settings of Thunderbird

They must be set manually:

- important #FE6364 (red)
- work      #EB8B16 (orange)
- personal  #1AB188 (green)
- to do     #6C71C4 (lile)
- later     #D33682 (pink)

### Suggested colors for new email redaction (on Thunderbird settings)

- background: #00141A
- text: #829696

### Language and appearance (look, also on Thunderbird settings) 

- font-family: sans-serif
- font-size: 15

### Todo

- Sometimes some of the receivers of the mails see background dark and text dark !? 
I suppose that this is caused by a BAD management of the colors their email clients.
But i would like to be sure that this is not a heavy problem. You know, we need sometimes 
that some emails be REDEABLE yes or yes (customers, potential customers,...). 
