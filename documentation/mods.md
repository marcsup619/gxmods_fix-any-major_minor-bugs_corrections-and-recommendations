# Disclaimer

Both Opera GX Mods and documentation are still actively developed. 

# Quick intro:

[Mod_Template](Mod_Template) is created to give you a quick start into creating mods. It showcases all capabilities and is a convenient starting point to create your own mods. Load it in Opera GX, look around, modify things and have fun. Most of the side-part information has been extrapolated from the main guidlines file, forked by me, for self esteem* and to provife ease of acces to anyone who has the guts to read every singlie word in this .md file.

![Loaded Mod Template](images/loaded_mod_template.png)

# Anatomy of GX Mod:

Each mod consists of:-

1. manifest.json - defines what's included in mod as well as name, author, version etc.
2. resources - sounds, images, videos, css, shaders etc. 

## manifest.json:

See [manifest.json](Mod_Template/manifest.json) from Mod_Template. It should be self explanatory. In case you make a mistake, Opera GX will show you an error when trying to load such a mod. Many issues and pull request are pushed every sing time, and all that for your refference. You can find our latest issue, pull request, for and many more on the original GXmods home page available on GitHub.

### Background music:

Opera GX uses [vertical remixing](https://gamemaker.io/en/blog/compose-video-game-music) to achieve dynamic music in the browser. However it doesn't mean you need to provide multiple music files. If only one is provided it will work as well. In such a case you can do a little trick and list the same file more than once. This will result in an increased volume when users are active in the browser. Provide at least one music track that is perfectly looped. If possible, use vertical remixing to achieve a dynamic music effect.

### Keyboard soundsP:

You can provide a single sound for a key or a list of sounds that will be played in the provided order. You can keep keys empty which means that no sound will be played or remove key and in that case default sound will be played. Provide sounds for ENTER, BACKSPACE, SPACE, and other keys. If possible, have more than one sound for each type, varying pitch/volume, etc. Make sure that typing is enjoyable. Sounds need to be short and start immediately to feel responsive. Make sure there's no silence at the beginning. It's important for keyboard sounds, as any delay will feel laggy. 

The sample [manifest.json](Mod_Template/manifest.json) shows all the keyboard sounds that can be added.

### Browser sounds:

The same rules apply as in keyboard sounds. The sample [manifest.json](Mod_Template/manifest.json) shows all the browser sounds that can be added.
Provide sounds for all categories. If possible, have more than one sound for each type, varying pitch/volume, etc. Be mindful of sounds that are played more frequently. Opening and closing tabs, clicks, and hovers will be heard often. Make sure it's an enjoyable experience. Sounds need to be short and start immediately to feel responsive. Make sure there's no silence at the beginning.

### Wallpaper:

Provide light and dark versions. Mods can't block users from switching between light and dark mode. The resolution should be at least 1920x1080. Keep images in JPG format to limit the size of the mod. Provide light and dark versions.Be mindful of content that is shown over the wallpaper. Ensure that it's not distracting. Move key objects to sides that are not going to be covered with content. Think about lower resolutions and different aspect ratios. Pick color and shadow color (for light and dark themes) for elements displayed on the start page. For animated wallpapers, please stick with a maximum 1920x1080 resolution; otherwise, it might be too resource-hungry. Keep them short and perfectly looped to keep mod size under control. Use VP9 video format if possible for best performance.

### Theme:

Provide both light and dark versions. Mods can't block users from switching between light and dark mode. Provide light and dark versions. If a wallpaper is included, make sure it creates an enjoyable composition. Note that too light or too dark colors are not available. It's advised to use the built-in color picker.

### Shaders:

More than one shader can be provided in a single mod. [Read more about shaders](shaders.md). Only one shader can be active at a time, which is controlled by the user. Optimize your shaders to use as little GPU as possible. If you create an animated shader, make sure to limit the framerate as much as possible to avoid useless GPU usage. For example, a clock that changes display every second doesn't need to run at 60fps. Use as few uniforms as possible. Don't use iMouse uniform unless you need it

it has performance implications. Consider including a non-animated version of the shader to limit GPU usage
(mods can include more than one shader).

### Web modding:

These are CSS styles that can be applied to web pages. Multiple pages can be modified with a single mod. Opera GX exposes
primary and secondary color if you want to make web pages follow UI colors (see [opera.css](Mod_Template/webmodding/opera.css))

## Guildelines:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Follow our [guidelines](guidelines.md) when creating mods.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

------------------------------------------------------------------------------------------------------------------------------------------------------------------------
