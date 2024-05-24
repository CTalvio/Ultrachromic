# Ultrachromic

The final form, the true evolution of the chromic theme saga! The old trilogy of chromic themes are deprecated, as their appearances can be replicated using Ultrachromic.

This is a custom theme for Jellyfin mediaserver created using CSS overrides. Note that I maintain this theme to be compatible with whatever version of Jellyfin I am currently using. Which is usually the latest stable release. You can therefore assume that using the theme on older versions may not work, but also that if a new release breaks something, that I will fix it. If you encounter unthemed elements or something broken, open an issue.

![Untitled](https://user-images.githubusercontent.com/4365015/127774204-03957527-7178-4ea2-8674-d83fe6a97d1c.png)

<br />

## Features
- Themes **EVERYTHING**
- Three types of styles to choose from
- Extensive additional options
- Customizable accent color
- Choose how blurry you want your backdrops
- Squared or rounded UI
- Options for progress bars, title pages, backdrops, logos...
- Works well on mobile, more compact and aligned UI
- Various small tweaks and fixes to the stock UI

<br />

<a href='https://ko-fi.com/mentaledge' target='_blank'><img height='35' style='border:0px;height:46px;' src='https://az743702.vo.msecnd.net/cdn/kofi3.png?v=0' border='0' alt='Buy Me a Coffee at ko-fi.com' />

# How to
To use the theme copy paste one of the presets, or follow the instructions to create a custom combination, paste that into "Dashboard>General>Custom CSS" and click save, it will apply immediately server-wide to all users on top of any theme they may be using. To remove the theme, clear the "Custom CSS" field and then click save.

**Adding modules after a preset may or may not work**, do not open an issue if you try to do things this way and it doesn't work. Either use a preset or a custom combination, not a mix of both, as that is not a use case I will be testing and guaranteeing to work.

**NOTE: Theme may not work when using reverse proxy**, check the bottom section of this readme for more info.

<br />

## Single line presets

These let you use Ultrachromic using a couple presets. These follow the same look as the old chromic themes.

```css
@import url('https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/presets/monochromic_preset.css');
```
OR
```css
@import url('https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/presets/kaleidochromic_preset.css');
```
OR
```css
@import url('https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/presets/novachromic_preset.css');
```
Only one line is needed, nova and kaleido support custom accents.

<br />
<br />

## Customization using multiple import lines

Ultrachromic is composed of multiple "parts" allowing you to theme only the parts you want, and to have some choice in how you want things themed. Simply add one import after another, in the order they are listed here. Simply omit the options you do not want to use.

<br />

### 1. Recommended

fixes.css contains various small tweaks all over the JF UI, an alignment here, a size tweak there. That kind of thing. jf_font.css will make JF use the same font as its logo, for everything. You can use both, one, or none of these.

```css
@import url('https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/fixes.css');
@import url('https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/jf_font.css');
```

<br />

### 2. Required

These lines are required.

```css
@import url('https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/base.css');
@import url('https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/accentlist.css');
```

<br />

### 3. Rounding

If you want to modify the rounding of corners in the UI, include one of these, circlehover keeps the stock circle accent when hovering over things, otherwise the accent will be a rounded square like everythig else.

```css
@import url('https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/rounding.css');
```
OR
```css
@import url('https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/rounding_circlehover.css');
```

<br />

### 4. Smaller cast list

![image](https://user-images.githubusercontent.com/4365015/127768495-3f211a57-3147-4b11-a9e0-5c9bdebc32b0.png)

A smaller, square aspect ratio style cast list.

```css
@import url('https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/smallercast.css');
```

<br />

### 5. Compact episode list

![image](https://user-images.githubusercontent.com/4365015/127768733-c86aee2c-3bff-4b78-be54-003823d60276.png)

A more easily scrolled episode list, there is the option to keep it as a list that is more compact, or turning the episode list into a grid menu.

```css
@import url('https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/episodelist/episodes_compactlist.css');
```
OR
```css
@import url('https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/episodelist/episodes_grid.css');
```

<br />

### 6. Transparent top bar

![image](https://user-images.githubusercontent.com/4365015/127768778-056a68eb-402f-49d0-8277-c11a71edbbe5.png)

Transaparent top bar.

```css
@import url('https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/header/header_transparent.css');
```

<br />

### 7. Login screen

![image](https://user-images.githubusercontent.com/4365015/127768970-e827c7e4-f4ce-4229-a68a-b2e87a723ef0.png)

Login screen styles. The minimalistic option has no frame or prompt text. You can also set a custom background, see further below.

```css
@import url('https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/login/login_minimalistic.css');
```
OR
```css
@import url('https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/login/login_frame.css');
```

<br />

### 8. Input fields

![image](https://user-images.githubusercontent.com/4365015/127769216-1d04cd30-14e0-4fda-9b2c-e0bfdb3514f6.png)

Input field styles, with borders that highlight when selected, or with no borders, and the background highlights, when selected.

```css
@import url('https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/fields/fields_border.css');
```
OR
```css
@import url('https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/fields/fields_noborder.css');
```

<br />

### 9. Watched/Unwatched indicators

![image](https://user-images.githubusercontent.com/4365015/127769354-f7a0c402-0c9a-4a8e-a347-e6c352ecabbf.png)

Two options, should the indicator be floating, or attached to the corner of the title card.

```css
@import url('https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/cornerindicator/indicator_floating.css');
```
OR
```css
@import url('https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/cornerindicator/indicator_corner.css');
```

<br />

### 10. Choose type

![Untitled](https://user-images.githubusercontent.com/4365015/127774204-03957527-7178-4ea2-8674-d83fe6a97d1c.png)

Dark, light, and colorful type. You must use one of these. If you wish to use an accent color with the dark style, use the "_withaccent" line.

```css
@import url('https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/type/dark.css');
```
OR
```css
@import url('https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/type/light.css');
```
OR
```css
@import url('https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/type/colorful.css');
```
OR
```css
@import url('https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/type/dark_withaccent.css');
```

<br />

### 11. Title page

![image](https://user-images.githubusercontent.com/4365015/127778994-ddee8235-6bb2-42ae-a8b1-f9023dc69398.png)


Four options, two versions, each version can be used with or without a logo replacing title text.

```css
@import url('https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/titlepage/title_simple.css');
```
OR
```css
@import url('https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/titlepage/title_simple-logo.css');
```
OR
```css
@import url('https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/titlepage/title_banner.css');
```
OR
```css
@import url('https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/titlepage/title_banner-logo.css');
```

<br />

### 12. Progress bar

![Screenshot_20210817_003507](https://user-images.githubusercontent.com/4365015/129632467-b545bcfc-3dbe-430d-8d3c-e89355eae29e.png)

Default, overlay or floating style progress indicator for library items.

```css
@import url('https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/overlayprogress.css');
```
OR
```css
@import url('https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/bottombarprogress.css');
```
OR
```css
@import url('https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/progress/floating.css');
```


<br />

### 13. Effects

![image](https://user-images.githubusercontent.com/4365015/127781073-c2a2a1f1-4c60-4c57-afa9-13a4775489bb.png)

Additional eye candy. Make items glow on hover, make some UI elements glassy see-through. Pan animation animates the backdrop with a slow pan. The last one is a hacky way to turn the cover art into a backdrop on mobile, as it was removed in 10.7.0.

Known issues: Pan-animation can cause flickering on chromium based browsers when the backdrop is also modified.

```css
@import url('https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/effects/hoverglow.css');
```
AND/OR
```css
@import url('https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/effects/glassy.css');
```
AND/OR
```css
@import url('https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/effects/pan-animation.css');
```
AND/OR
```css
@import url('https://ctalvio.github.io/Monochromic/backdrop-hack_style.css');
```

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

### Extras

[Check out these custom icons by @prayag17!](https://github.com/prayag17/Jellyfin-Icons)

Also a general thanks to prayag17, I've joinked some code from him for this project. (grid episodes, title logo)

<br />
<br />

### Fix for use with some reverse proxy setups

When using the Nginx Reverse proxy config from the [Jellyfin docs](https://jellyfin.org/docs/general/networking/nginx.html) the theme will not work by default. (If you are using the subpath config, you can ignore this.)

Because the config includes Content-Security-Policy which reduces risk of XSS, you need to add the URL's from this repo and the fonts to the list of allowed external sources.

In the nginx config you should change the

```
add_header Content-Security-Policy ....
```
to:

```
add_header Content-Security-Policy "default-src https: data: blob:; style-src 'self' 'unsafe-inline' https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/accentlist.css https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/base.css https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/bottombarprogress.css https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/fixes.css https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/jf_font.css https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/overlayprogress.css https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/rounding.css https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/rounding_circlehover.css https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/smallercast.css https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/rounding_circlehover.css https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/cornerindicator/indicator_floating.css https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/cornerindicator/indicator_corner.css https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/effects/glassy.css https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/effects/pan-animation.css https://ctalvio.github.io/Monochromic/backdrop-hack_style.css https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/effects/hoverglow.css https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/effects/scrollfade.css https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/episodelist/episodes_compactlist.css https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/episodelist/episodes_grid.css https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/fields/fields_border.css https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/fields/fields_noborder.css https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/header/header_transparent.css https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/header/header_transparent-dashboard.css https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/login/login_frame.css https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/login/login_minimalistic.css https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/login/login_frame.css https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/presets/monochromic_preset.css https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/presets/kaleidochromic_preset.css https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/presets/novachromic_preset.css https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/titlepage/title_banner.css https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/titlepage/title_banner-logo.css https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/titlepage/title_simple.css https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/titlepage/title_simple-logo.css https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/type/light.css https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/type/dark.css https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/type/colorful.css https://cdn.jsdelivr.net/gh/CTalvio/Ultrachromic/type/dark_withaccent.css https://fonts.googleapis.com/css2; script-src 'self' 'unsafe-inline' https://www.gstatic.com/cv/js/sender/v1/cast_sender.js worker-src 'self' blob:; connect-src 'self'; object-src 'none'; frame-ancestors 'self'";
```

If you don't do this the theme will simply not load (reverts back to default theme) and the browser console will spit out an error. Even if you paste in all the CSS, the font will still not load since it is loaded from an external source.
