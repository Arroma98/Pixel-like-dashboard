###### Pixel-like-dahsboard
## What's that?
This is an “Android 13 Pixel-like” dashboard based on [Rounded Dashboard by Leon](https://community.home-assistant.io/t/rounded-dashboard-guide/543043).
###### NB - I'm not a developer or anything, I'm a mere mortal who until recently was unknown to this whole world and is getting to know it from scratch.

# theme.yaml
It has to look like the pixel interface, so we need to use the exact colors first.

![QSPanel_white](https://github.com/Arroma98/Pixel-like-dahsboard/assets/118556527/f81d98c5-544e-4cb6-94f2-eddcb22a0168)![QSPanel_dark](https://github.com/Arroma98/Pixel-like-dahsboard/assets/118556527/20b80081-3d4a-49b3-89f2-189c08137a33)

## colors
As you can see here, the header always stays black while the panel varies light/dark, and as can be seen, the background of the notifications is brighter than that of the panel, both in the dark and in the light mode.

So, let's add these variables to the theme:
###### Assuming you already have the rounded theme
```
## White mode:
white0: "#f2f0f4" #darker
white00: "#fbf8fd" #brighter

## Dark mode:
black0: "#1b1b1f" #darker
black00: "#303034" #brighter
```
So then we can add:
```
  modes:
    dark:
      contrast0: var(--black0)
      contrast00: var(--black00)
    light:
      contrast0: var(--white0)
      contrast00: var(--white00)
 ```
## font
We need to use the Google Sans font, so let's import the url we find [here](https://www.cdnfonts.com/google-sans.font).
###### [How to import a font](https://community.home-assistant.io/t/trying-to-add-font/400236/2?u=arroma).
