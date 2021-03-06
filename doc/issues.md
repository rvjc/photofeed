# Photofeed Gadget Issues and Workarounds


## Dynamic height adjustment failure following edit/save cycle.

This is a well-known Classic Google Sites issue which affects all gadgets that
use the Gadget API's dynamic height feature. However, it only manifests itself
in the current browser tab/window immediately after an edit/save cycle. Normal
dynamic height functionality can be restored by performing a page refresh (F5).
This problem does **not** affect normal page viewing. 


## Blank content after back/forward navigation in Chrome/Windows 

This generic problem with embedded IFRAME content has been reported elsewhere
in a number of guises. Ironically, for Google Sites users, it has only been
noticed in Chrome. Other mainstream browsers such as IE, Firefox, Safari and
Opera do not exhibit this problem. It appears to be an IFRAME caching bug on
pages containing multiple gadget instances. If you navigate to a previously
viewed page using the *Back* or *Forward* button, only the LAST gadget instance
displays correctly. It does NOT arise on pages with single gadget instances.

Chrome should either reproduce the cached IFRAME state or reload its cached
source, but, in some cases, it does neither. The gadget frame is present and
correctly dimensioned but the content is blank. In the case of the Photofeed
gadget, even the fallback "loading" status is *not* visible. The clue lies in
the fact that the last gadget instance on the page always displays correctly.
Until this bug is fixed by Google, it can be resolved by a page refresh (F5)
which will successfully reload all gadget instances.
