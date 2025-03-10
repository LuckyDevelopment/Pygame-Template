Things to note:
- Render everything to a surface (300x400), then just scale that up to the window size (600x800), then blit JUST that on the screen. ``self.screen.blit(pygame.transform.scale(self.display, self.screen.get_size()), (0, 0))``
- For deltaTime, just add this line before you call ``pygame.display.update()``, add this: ``self.deltaTime = max(0.0001, min(0.1, self.clock.tick(self.targetFrameRate) / 1000))``. You will need a target frame rate and delta time variable.

Recommend watching these videos:

https://www.youtube.com/watch?v=2gABYM5M0ww&t=13s&ab_channel=DaFluffyPotato
https://www.youtube.com/watch?v=blLLtdv4tvo&ab_channel=DaFluffyPotato
