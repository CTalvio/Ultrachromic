# Ultrachromic

The final form, the true evolution of the chromic theme saga! The old trilogy of chromic themes are deprecated, as their appearances can be replicated using Ultrachomic.

This is a custom theme for Jellyfin mediaserver created using CSS overrides. Note that I maintain this theme to be compatible with whatever version of Jellyfin I am currently using. Which is usually the latest stable release. You can therefore assume that using the theme on older versions may not work, but also that if a new release breaks something, that I will fix it. If you encounter unthemed elements or something broken, open an issue.

![Untitled](https://user-images.githubusercontent.com/4365015/127774204-03957527-7178-4ea2-8674-d83fe6a97d1c.png)

To use the theme copy paste one of the presets, or follow the instructions to create a custom combination, paste that into "Dashboard>General>Custom CSS" and click save, it will apply immediately server-wide to all users on top of any theme they may be using. To remove the theme, clear the "Custom CSS" field and then click save.

## Features
- Themes **EVERYTHING**
- Three types of styles to choose from
- Extensive additional options
- Customizable accent color
- Decide yourself, exactly how you want your backdrops blurred
- Squared or rounded UI style, you decide
- Two options for progress bars
- Works well on mobile, more compact and aligned UI
- Various small tweaks and fixes to the stock UI


### Single line presets

These let you use Ultrachromic using a couple presets. These follow the same look as the old chromic themes.

```css
@import url('https://ctalvio.github.io/Ultrachromic/presets/monochromic_preset.css');
```
OR
```css
@import url('https://ctalvio.github.io/Ultrachromic/presets/kaleidochromic_preset.css');
```
OR
```css
@import url('https://ctalvio.github.io/Ultrachromic/presets/novachromic_preset.css');
```
Only one line is needed, nova and kaleido support custom accents.

<br />
<br />

## Customization using multiple import lines

Ultrachromic is composed of multiple "parts" allowing you to theme only the parts you want, and to have some choice in how you want things themed. Simply add one import after another, in the order they are listed here. Simply omit the options you do not want to use.

<br />
<br />

### 1. Recommended

fixes.css contains various small tweaks all over the JF UI, an alignment here, a size tweak there. That kind of thing. jf_font.css will make JF use the same font as its logo, for everything. You can use both, one, or none of these.

```css
@import url('https://ctalvio.github.io/Ultrachromic/fixes.css');
@import url('https://ctalvio.github.io/Ultrachromic/jf_font.css');
```

<br />
<br />

### 2. Required

These lines are required.

```css
@import url('https://ctalvio.github.io/Ultrachromic/base.css');
@import url('https://ctalvio.github.io/Ultrachromic/accentlist.css');
```

<br />
<br />

### 3. Rounding

If you want to modify the rounding of corners in the UI, include one of these, circlehover keeps the stock circle accent when hovering over things, otherwise the accent will be a rounded square like everythig else.

```css
@import url('https://ctalvio.github.io/Ultrachromic/rounding.css');
```
OR
```css
@import url('https://ctalvio.github.io/Ultrachromic/rounding_circlehover.css');
```

<br />
<br />

### 4. Smaller cast list

![image](https://user-images.githubusercontent.com/4365015/127768495-3f211a57-3147-4b11-a9e0-5c9bdebc32b0.png)

A smaller, square aspect ratio style cast list.

```css
@import url('https://ctalvio.github.io/Ultrachromic/smallercast.css');
```

<br />
<br />

### 5. Compact episode list

![image](https://user-images.githubusercontent.com/4365015/127768733-c86aee2c-3bff-4b78-be54-003823d60276.png)

A more easily scrolled episode list, there is the option to keep it as a list that is more compact, or turning the episode list into a grid menu.

```css
@import url('https://ctalvio.github.io/Ultrachromic/episodelist/episodes_compactlist.css');
```
OR
```css
@import url('https://ctalvio.github.io/Ultrachromic/episodelist/episodes_grid.css');
```

<br />
<br />

### 6. Transparent top bar

![image](https://user-images.githubusercontent.com/4365015/127768778-056a68eb-402f-49d0-8277-c11a71edbbe5.png)

Transaparent top bar, use one of these. The "-dashboard" option, also makes the bar transparent in the dashboard.

```css
@import url('https://ctalvio.github.io/Ultrachromic/header/header_transparent-dashboard.css');
```
OR
```css
@import url('https://ctalvio.github.io/Ultrachromic/header/header_transparent.css');
```

<br />
<br />

### 7. Login screen

![image](https://user-images.githubusercontent.com/4365015/127768970-e827c7e4-f4ce-4229-a68a-b2e87a723ef0.png)

Login screen styles. The minimalistic option has no frame or prompt text. You can also set a custom background, see further below.

```css
@import url('https://ctalvio.github.io/Ultrachromic/login/login_minimalistic.css');
```
OR
```css
@import url('https://ctalvio.github.io/Ultrachromic/login/login_frame.css');
```

<br />
<br />

### 8. Input fields

![image](https://user-images.githubusercontent.com/4365015/127769216-1d04cd30-14e0-4fda-9b2c-e0bfdb3514f6.png)

Input field styles, with borders that highlight when selected, or with no borders, and the background highlights, when selected.

```css
@import url('https://ctalvio.github.io/Ultrachromic/fields/fields_border.css');
```
OR
```css
@import url('https://ctalvio.github.io/Ultrachromic/fields/fields_noborder.css');
```

<br />
<br />

### 9. Watched/Unwatched indicators

![image](https://user-images.githubusercontent.com/4365015/127769354-f7a0c402-0c9a-4a8e-a347-e6c352ecabbf.png)

Two options, should the indicator be floating, or attached to the corner of the title card.

```css
@import url('https://ctalvio.github.io/Ultrachromic/cornerindicator/indicator_floating.css');
```
OR
```css
@import url('https://ctalvio.github.io/Ultrachromic/cornerindicator/indicator_corner.css');
```

<br />
<br />

### 10. Choose type

![Untitled](https://user-images.githubusercontent.com/4365015/127774204-03957527-7178-4ea2-8674-d83fe6a97d1c.png)

Dark, light, and colorful type. You must use one of these.

```css
@import url('https://ctalvio.github.io/Ultrachromic/type/dark.css');
```
OR
```css
@import url('https://ctalvio.github.io/Ultrachromic/type/light.css');
```
OR
```css
@import url('https://ctalvio.github.io/Ultrachromic/type/colorful.css');
```

<br />
<br />

### 11. Title page



Four options, two versions, each version can be used with or without a logo replacing title text.

```css
@import url('https://ctalvio.github.io/Ultrachromic/titlepage/title_simple.css');
```
OR
```css
@import url('https://ctalvio.github.io/Ultrachromic/titlepage/title_simple-logo.css');
```
OR
```css
@import url('https://ctalvio.github.io/Ultrachromic/titlepage/title_banner.css');
```
OR
```css
@import url('https://ctalvio.github.io/Ultrachromic/titlepage/title_banner-logo.css');
```

<br />
<br />

### 12. Progress bar



Default or an overlay style progress indicator for library items.

```css
@import url('https://ctalvio.github.io/Ultrachromic/overlayprogress.css');
```
OR
```css
@import url('https://ctalvio.github.io/Ultrachromic/bottombarprogress.css');
```

<br />
<br />

### 13. Effects



Additional eye candy. Make items glow on hover, make some UI elements glassy see-through, and/or fade items in and out on scroll.

```css
@import url('https://ctalvio.github.io/Ultrachromic/effects/hoverglow.css');
```
AND/OR
```css
@import url('https://ctalvio.github.io/Ultrachromic/effects/glassy.css');
```
AND/OR
```css
@import url('https://ctalvio.github.io/Ultrachromic/effects/scrollfade.css');
```

<br />
<br />

### 14. Manual options

There are some manual options you can define if you want, after the import lines add this short snippet of code, you can edit it to set anything you want as a login background, or modify how blurry or dark/light your backdrops are, as well as to set a custom accent color.

```css
/*Style backdrop*/
.backdropImage {filter: blur(18px) saturate(120%) contrast(120%) brightness(40%);}

/*Login background*/
#loginPage {background: url(https://i.imgur.com/9vL4iNf.png) !important;}

/*Accent and roundingd*/
:root {--accent: 98, 121, 205;}
:root {--rounding: 12px;}
```

<br />
<br />

### X. Extras

Chaeck out these custom icons by @prayag17: github.com/prayag17/Jellyfin-Icons
Also thanks to prayag17, I've joinked some code from him for this project. (grid episodes)
