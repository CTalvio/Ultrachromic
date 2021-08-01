# Ultrachromic
The final form, the true evolution of the chromic theme saga!

# CURRENTLY BEING TESTED, FEEL FREE TO TRY IT OUT AND REPORT ISSUES


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

To use the theme copy paste the lines below to "Dashboard>General>Custom CSS" and click save, it will apply immediately server-wide to all users on top of any theme they may be using. To remove the theme, clear the "Custom CSS" field and then click save. **NOTE: Theme may not work when using reverse proxy**, check the bottom section of this readme for more info.

Ultrachromic is composed of multiple "parts" allowing you to theme only the parts you want, and to have some choice in how you want things themed. Simply add the one after the other, in the order they are listed here. Simply omit the options you do not want to use.

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

### 12. Effects

![image](https://user-images.githubusercontent.com/4365015/127769354-f7a0c402-0c9a-4a8e-a347-e6c352ecabbf.png)

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
