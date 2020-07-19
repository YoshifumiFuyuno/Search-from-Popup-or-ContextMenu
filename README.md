# Search from Popup or ContextMenu (SPC)

This is a WebExtension for browsers.  
This Extension is a *fork* of "[Swift Selection Search (SSS)](#acknowledgment)".  

When you select text or image on a webpage, you can quickly search from the popup or contextmenu.

**By default, popup appears when you drag an image, selected text, or link, but you can choose from the following behaviors.**  
  "Popup/icons behaviour" -> "Opening behaviour":  
  (Off / Auto / Hold Alt / Keyboard-only / Middle mouse button / Click / Drag)

There are Firefox and Microsoft Edge(Chrome) versions.  
Microsoft Edge version also works with Chromium-based browsers such as Chrome, but there's no technical support.

## Download
  * [Firefox](https://addons.mozilla.org/firefox/addon/searchfrompopuporcontextmenu/)
  * [Microsoft Edge(Chrome)](https://microsoftedge.microsoft.com/addons/detail/hlikagndoiibjkblhopoajeonpkfgiko)

## Privacy policy
  * Search query are **not saved**.
  * You can use suggest(Google or DuckDuckGo or Qwant or Bing or Яндекс(Yandex) or 百度(Baidu)) in the popup search box, but you can disable it in the settings.  
    "Popup/icons behaviour" -> "Enable search box suggest"
  * If you set your favicon to data: scheme and disable suggest, this extension will not access the network at all.  
    Excludes processing performed by the browser (update and synchronization).

## Different
* Fork Changes (Based on SSS Version 3.33.0):
  * Now works with Microsoft Edge(Chrome).
  * The site's [Content Security Policy(CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy) does not change.  
    (Original Extension(SSS) rewrites CSP to "unsafe-inline" after Ver.3.40.0)
  * You can search on multiple search engines at once.
  * support POST Method search engine.
  * support search engine folder management.
  * added Popup Style ("Icon only" / "Icon and Name" / "Name only").  
    (At "Icon only", the display mode can be temporarily switched by double-clicking)
  * support [Bookmarklet](https://en.wikipedia.org/wiki/Bookmarklet). You can use [Bookmarklet APIs](https://github.com/YoshifumiFuyuno/Search-from-Popup-or-ContextMenu/wiki/Bookmarklet-APIs).  
    (It can also be executed automatically when the popup is displayed) / (You can also import bookmarklets from your Bookmarks)
  * added Search box to Popup. (Support for Google or DuckDuckGo or Qwant or Bing or Яндекс(Yandex) or 百度(Baidu) suggest)
  * added Hotkey search.
  * added a function to easily add a search engine from the text box context menu.
  * added search URL `{linkurl}`. `{linkurl}` is supports "[Advanced usage](https://github.com/YoshifumiFuyuno/Search-from-Popup-or-ContextMenu/wiki/Instructions#advanced-usage)".  
    (Used when you want to search by link URI. For Firefox, you can also do this by holding down the Ctrl key and selecting the context menu)
  * If no text is selected, the Clipboard Text is searched.
  * Context menu display options.
  * You can also search by link text or image URL.
  * added Popup Opening behaviour "click" / "drag"
  * added "Popup/icons behaviour" -> "Right mouse button click" / "Right mouse button Long-click" / "Left mouse button Long-click"
  * added "Context menu" -> "Middle mouse button click" / "Right mouse button click"
  * added Open in Window ("reuse new window" / "reuse new background window" / "new incognito (private) window" / "reuse new incognito(private) window" / "new background incognito(private) window" / "reuse new background incognito(private) window" / "new popup window" / "reuse new popup window" / "new background popup window" / "reuse new background popup window" / "sidebar (tab-specific)" / "sidebar (window-specific)" / "sidebar (global)")  
    (sidebar UserAgent can be changed) / (The Popup window can be closed automatically.(Off/LostFocus/Mouseleave)).
  * added Open in Tab ("reuse active tab" / "reuse new tab" / "reuse new background tab" / "reuse new tab (next to current tab)" / "reuse new background tab (next to current tab)")
  * added Ability to show last used engine first in popup.
  * added Hide Popup with ESC key etc.
  * Allow "open-popup" Command to display popup even if no string is selected.
  * support charset (UTF-8, RAW(GET method only), Shift_JIS(SJIS), EUC-JP, ISO-2022-JP(JIS), windows-1251, windows-1252(ISO-8859-1), Big5, GB18030).
  * When the OS is set to dark mode, the option page is displayed in dark mode.
* Import/Export Compatibility with the Original Extension Ver.3.33.0:
  * Import can also import file from the Original Extension.
  * File exported by SPC is not compatible with the Original Extension Search engines setting.
* Permissions different from Original Extension Ver.3.33.0:
  * removed permissions: downloads, webNavigation.
  * added permissions: clipboardRead(Clipboard text search), unlimitedStorage(data: scheme icons).
  * added optional_permissions: bookmarks(Import bookmarklet), webRequest(Sidebar user agent), webRequestBlocking(Sidebar user agent).
  * From normal permissions to optional_permissions: clipboardWrite(copyToClipboard As Html/Text).

## ChangeLog
https://addons.mozilla.org/firefox/addon/searchfrompopuporcontextmenu/versions/

## Contact
If you have any requests or issues, please [GitHub Issues](https://github.com/YoshifumiFuyuno/Search-from-Popup-or-ContextMenu/issues) in Japanese or your first language.  
It is easy to understand if there is a screenshot etc.

## License
### GNU GPLv3
Copyright (C) 2019  Yoshifumi Fuyuno

This program is free software: you can redistribute it and/or modify  
it under the terms of the GNU General Public License as published by  
the Free Software Foundation, either version 3 of the License, or  
(at your option) any later version.  

This program is distributed in the hope that it will be useful,  
but WITHOUT ANY WARRANTY; without even the implied warranty of  
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the  
GNU General Public License for more details.

You should have received a copy of the GNU General Public License  
along with this program.  If not, see <https://www.gnu.org/licenses/>.

## Acknowledgment
I would like to take this opportunity to express my appreciation to developers.

Original Extension:  
Swift Selection Search by Daniel Lobo  
https://addons.mozilla.org/firefox/addon/swift-selection-search/  
Original Extension License: MIT License
