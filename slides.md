---
# You can also start simply with 'default'
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
#background: https://cover.sli.dev
background: https://cdn.jsdelivr.net/gh/slidevjs/slidev-covers@main/static/zRkBOOpKRhs.webp
# some information about your slides (markdown enabled)
title: Aalund AI
info: |
  ## Aalund AI af René Sinnbeck
# apply unocss classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-up
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
---

# AI hos Aalund

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---
transition: slide-up
---

# Implementering af wav peaks fil generator
<img src="/peaks.png"  alt="peaks"/>

<style>
img {
    width: 80%;
}
</style>


---
transition: slide-up
---

# SPSS eksporter der bruger SPSS syntax
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
transition: slide-up
---

# Transkribering af optagelser
Til brug ved f.eks. dybde interviews
<img src="/whisper.png"  alt="peaks"/>
<style>
img {
    width: 280px;
}
</style>