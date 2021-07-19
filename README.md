# Ultrachromic
The final form, the true evolution of the chromic theme saga!

# CURRENTLY BEING TESTED, FEEL FREE TO TRY IT OUT AND REPORT ISSUES


### Single line presets

These let you use Ultrachromic using a couple presets. These follow the same look as the old chromic themes.

```css
@import url('https://ctalvio.github.io/Ultrachromic/presets/monochromic_preset.css');
@import url('https://ctalvio.github.io/Ultrachromic/presets/kaleidochromic_preset.css');
@import url('https://ctalvio.github.io/Ultrachromic/presets/novachromic_preset.css');
```
Only one line is needed, nova and kaleido support custom accents.



## Customization using multiple import lines

To use the theme copy paste the lines below to "Dashboard>General>Custom CSS" and click save, it will apply immediately server-wide to all users on top of any theme they may be using. To remove the theme, clear the "Custom CSS" field and then click save. **NOTE: Theme may not work when using reverse proxy**, check the bottom section of this readme for more info.

Ultrachromic is composed of multiple "parts" allowing you to theme only the parts you want, and to have some choice in how you want things themed. Simply add the one after the other, in the order they are listed here. Simply omit the options you do not want to use.

### 1. Required

These lines are required.

```css
@import url('https://ctalvio.github.io/Ultrachromic/base.css');
@import url('https://ctalvio.github.io/Ultrachromic/accentlist.css');
```

### 2. Recommended

fixes.css contains various small tweaks all over the JF UI, an alignment here, a size tweak there. That kind of thing. jf_font.css will make JF use the same font as it's logo, for everything. You can use both, one or none of these.

```css
@import url('https://ctalvio.github.io/Ultrachromic/fixes.css');
@import url('https://ctalvio.github.io/Ultrachromic/jf_font.css');
```

### 3. Rounding

If you want to modify the rounding of corners in the UI, include this option.

```css
@import url('https://ctalvio.github.io/Ultrachromic/drounding.css');
```

### 4. Smaller cast list

A smaller, square aspect ratio style cast list.

```css
@import url('https://ctalvio.github.io/Ultrachromic/smallercast.css');
```

### 5. Compact episode list

A more easily scrolled episode list.

```css
@import url('https://ctalvio.github.io/Ultrachromic/compactepisodes.css');
```

### 6. Transparent banner

Transaparent top banner, use one of these. The "-dashboard" option, also makes the banner transparent in the dashboard.

```css
@import url('https://ctalvio.github.io/Ultrachromic/transparentbanner-dashboard.css');
@import url('https://ctalvio.github.io/Ultrachromic/transparentbanner.css');
```


### 7. Login screen

Login screen styles.

```css
@import url('https://ctalvio.github.io/Ultrachromic/transparentbanner-dashboard.css');
@import url('https://ctalvio.github.io/Ultrachromic/transparentbanner.css');
```

### 7. Input fields

Input field styles.

```css
@import url('https://ctalvio.github.io/Ultrachromic/fields_1.css');
@import url('https://ctalvio.github.io/Ultrachromic/fields_2.css');
```

### 8. Input fields

Input field styles.

```css
@import url('https://ctalvio.github.io/Ultrachromic/fields_1.css');
@import url('https://ctalvio.github.io/Ultrachromic/fields_2.css');
```

### X. Choose type

Dark, light, and colorful type. You must use one of these.

```css
@import url('https://ctalvio.github.io/Ultrachromic/type/dark.css');
@import url('https://ctalvio.github.io/Ultrachromic/type/light.css');
@import url('https://ctalvio.github.io/Ultrachromic/type/colorful.css');
```



