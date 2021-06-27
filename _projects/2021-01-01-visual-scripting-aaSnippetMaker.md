---
layout: post
title: Maya - Capture your actions inside Maya - Visual scripting
img: /assets/project/snippetMaker.jpg
tag: [Maya, python, PyQt]
---

This tool captures everything you do on Maya to automatically have it converted to `Python`/`MEL`. You can also script visually!

You can also modify the commands parameters from the UI.

Useful for people who want to:
 - Quickly have their prototypes ready in a script.
 - Automate their workflow without the need to script.

 On top of my mind, this is especially useful for rigging artists who constantly
 prototype and then have to recreate their actions forleft/right side,
 different characters. etc.

{% include vimeo-player.html id="490539028" %}

 

---

 

## Functionality

  

![Desktop View](/assets/img/aaSnippetMaker/capturing_sideToSide_UI.gif)


While being open, it will capture every relevant action and have it saved on the UI.

Some action examples:
- Create/Delete/Rename nodes
- Create/Connect/Disconnect/Set attributes
- Runtime Maya commands
- Among others

#### Node stack:

For the visual scripting part, there is a node stack that allows you to:
- See the current flags for the selected command
- See all available flags for the selected command
- Add/Edit/Remove flags
- Search and replace the names of the used objects.

![Desktop View](/assets/img/aaSnippetMaker/flags2.gif){: width="500" .normal}

#### Python & MEL Script Editor:


As well, there is a `Python` and `MEL` script editor that allows you to
see your latest changes reflected on Maya and
the tool's UI.

![Desktop View](/assets/img/aaSnippetMaker/multipleLanguages.gif)

---
 

## Future plans:

 

Some pending to-do's:
- [ ] From an already existing graph/scene, convert it to commands on the UI.
- [ ] Undo actions/Stack traces can be tricky to actually reflect the end result.
- [ ] Release it to the public!