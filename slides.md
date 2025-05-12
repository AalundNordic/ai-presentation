---
# You can also start simply with 'default'
theme: the-unnamed
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
#background: https://cover.sli.dev
background: https://cdn.jsdelivr.net/gh/slidevjs/slidev-covers@main/static/REjuIrs2YaM.webp
image: https://cdn.jsdelivr.net/gh/slidevjs/slidev-covers@main/static/REjuIrs2YaM.webp
favicon: '/favicon.ico'
# some information about your slides (markdown enabled)
title: Aalund AI
author: René Sinnbeck
info: false
# apply unocss classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-up
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true

themeConfig:
  color: "#F3EFF5"
  background: "#161C2C"

  code-background: "#0F131E"
  code-border: "#242d34"
  code-color: var(--slidev-theme-code-color)
  code-font-size: 1.1em

  accents-teal: "#44FFD2"
  accents-yellow: "#e1d38b"
  accents-red: "#cd6767"
  accents-lightblue: "#15C2CB"
  accents-blue: "#009EE0"
  accents-vulcan: "#0E131F"

  header-shadow: rgba(0, 0, 0, 0.15) 1.95px 1.95px 2.6px;

  default-headingBg: var(--slidev-theme-accents-blue)
  default-headingColor: var(--slidev-theme-accents-yellow)
  default-background: var(--slidev-theme-background)
  default-font-size: 1.1em

  center-headingBg: var(--slidev-theme-accents-blue)
  center-headingColor: var(--slidev-theme-accents-yellow)
  center-background: var(--slidev-theme-background)
  center-font-size: 1.1em

  cover-headingBg: var(--slidev-theme-accents-blue)
  cover-headingColor: var(--slidev-theme-accents-yellow)
  cover-background: var(--slidev-theme-background)
  cover-font-size: 1.1em

  section-headingBg: var(--slidev-theme-accents-lightblue)
  section-headingColor: var(--slidev-theme-accents-vulcan)
  section-background: var(--slidev-theme-background)
  section-font-size: 1.1em

  aboutme-background: var(--slidev-theme-color)
  aboutme-color: var(--slidev-theme-background)
  aboutme-helloBg: var(--slidev-theme-accents-yellow)
  aboutme-helloColor: var(--slidev-theme-background)
  aboutme-nameColor: var(--slidev-theme-accents-red)
  aboutme-font-size: 1.1em

---

# AI hos Aalund

---
layout: center
---

<style>
.peaks {
    width: 70%;
    text-align: center;
}
</style>

# Implementering af wav peaks fil generator
<img src="/peaks.png" alt="peaks" class="peaks"/>


---
layout: center
---

# SPSS eksporter til Websurvey

SPSS direkte i php
```php
$lines[] = "SET LOCALE='UTF-8'.";
$lines[] = "NEW FILE.";

$esc = addcslashes($csvFile, "'");
$lines[] = "GET DATA"
    . " /TYPE=TXT"
    . " /FILE='$esc'"
    . " /DELCASE=LINE"
    . " /DELIMITERS=\",\""
    . " /QUALIFIER='\"'"
    . " /ARRANGEMENT=DELIMITED"
    . " /VARIABLES";
foreach ($this->variables as $n => $i) {
    $fmt = $i['type'] === 'numeric' ? 'F8.2' : "A{$i['width']}";
    $lines[] = "  $n $fmt";
}
$last = array_pop($lines);
$lines[] = trim($last) . ".";

$lines[] = "EXECUTE.";
```

---
layout: two-cols
---
<style>
.whisper {
    width: 280px;
    margin-left: 20px;
}
</style>

# Transkribering af optagelser
Til brug ved f.eks. dybde interviews
::right::
<img src="/whisper.png"  alt="peaks" class="whisper"/>
