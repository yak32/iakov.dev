---
title: CEGUI vs IMGUI
subtitle: Bloated UI
description: "Creating one button in CEGUI takes five lines of setup code. An immediate-mode GUI does the same job in a single if statement."
date: 2012-12-24 10:58
tags: [engine, gui]
---
This is the code to create a button in CEGUI:

```cpp
// Create window
wnd = CEGUI::WindowManager::getSingleton().createWindow("TaharezLook/Button", "JumpPushButton");
wnd->setPosition(CEGUI::UVector2(CEGUI::UDim(0.75,0),CEGUI::UDim(0.50,0)));
wnd->setSize(CEGUI::UVector2(CEGUI::UDim(0,50),CEGUI::UDim(0,50)));
wnd->setText("Jump!");
CEGUI::System::getSingleton().getGUISheet()->addChildWindow(gJumpBtnWindow);
```

It's ugly. It reminds me of a joke by Charles Bloom: [how to lose game developer love](http://cbloomrants.blogspot.kr/2012/12/12-15-12-how-to-lose-game-developer-love.html).

Here is how creating and using a button should look:

```cpp
if ( gui.button("Cancel")  )
   cancel_job();
```
