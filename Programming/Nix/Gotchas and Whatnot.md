---
tags:
  - nix
---


Since Nix doesn't follow how package usually works, it's no use to force the mindset of using regular package into it. Here are some things that I learned

### Don't install everything using Nix
While it may sound like the best thing in the world, having a 100% reproducible work environment, I don't think everything should be installed through Nix. There are several issues I had with it.
- GUI Apps sometimes feels like it's not integrated. 
	Weird issue start to appear like not applying the system theme and whenever I hover my cursor above the window it resets to the default cursor as opposed to the bocchi cursor that I have lol. Even though this is the case, I still much prefer installing stuff using Nix than something like [AppImage](https://appimage.org/) or [Flatpak](https://flatpak.org/) because of course they both came with their own issues. Nix is still a little bit better on this regard.
- I find it only suitable for apps that is mostly used in the terminal because I view them as utility tool and they're usually small and I want them to be portable / always installed on whatever machine I'm currently on.

### GPU-related stuff
Nix doesn't have access to [[OpenGL]] or [[Vulkan]] installed on the system, hence it needs to use a wrapper called [nixGL](https://github.com/nix-community/nixGL). It works great though once you figured it out, I have no complaints about it.