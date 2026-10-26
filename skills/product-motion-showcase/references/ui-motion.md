# Subtle UI motion on static screens

I prefer to get static screens and animate them myself: I bring the interface to life. The product still has to look like the real product, so it stays subtle. If the user cannot do that and sends screen recordings instead, those stay as they are and I do not touch them.

## How I do it

**Every move has a reason.** It explains something, confirms a tap, shows that a state changed or guides the eye. If the only reason is "it looks cool", I leave it out. I never animate everything, because then nothing stands out.

**Nothing comes out of nothing.** An element never starts at scale 0. It starts at around 90 to 95 percent with its opacity at 0 and eases up to full size.

**Things grow from what caused them.** A menu opens from its button, a pill grows from the tip of its line, a card from the item that was tapped. I set the origin of the scale there, not in the middle.

**Buttons answer a tap.** A pressed button dips slightly, to about 97 percent, and comes back with my ease. It is small, but it makes the interface feel like it is listening.

**Groups arrive staggered.** In a list or a row of cards, each item starts when the previous one is about halfway, so they come in half after each other. Never all at once, and never a slow queue.

**State changes flow, they do not flip.** A toggle, a tab or a selection changes colour with a transition, not with a cut. For tabs I copy the row in its active style and reveal it with a mask, which gives one clean colour change. When a crossfade still looks off, I add a very light blur, around 2 px, during the swap. Then two states read as one object instead of two overlapping ones.

**One ease for everything.** My 80/80 ease (see `timing-and-easing.md`). Some elements get a subtle bounce, others do not, and I alternate them. Leaving is always shorter than entering.

**Match the brand.** A playful brand gets a bit more bounce. A calm or serious brand stays crisp and restrained.

**Overlap with the rest.** UI motion starts while the camera or the frame is still moving. It does not wait for the previous move to finish.

## How I check it

I look at every transition frame by frame, and at 2 to 5 times slower than normal. Then I look again the next day with fresh eyes. Small timing problems show up then that I missed while building.
