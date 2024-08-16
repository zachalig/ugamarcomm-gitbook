---
description: A practical guide to web page basic accessibility review and improvement.
---

# Accessibility (A11y) Quality Assurance Process

### Before getting started <a href="#before-getting-started" id="before-getting-started"></a>

Have the following browser extensions installed (links are to Chrome web store. FF and Edge support all of them too):

* [WAVE](https://chromewebstore.google.com/detail/wave-evaluation-tool/jbbplnpkjmmeebjpijfedlgcdilocofh)
* [ARIA Dev Tools](https://chromewebstore.google.com/detail/aria-devtools/dneemiigcbbgbdjlcdjjnianlikimpck?hl=en)
* [AXE](https://chromewebstore.google.com/detail/axe-devtools-web-accessib/lhdoppojpmngadmnindnejefpokejbdd) (optional)
* [IBM Equal Access](https://chromewebstore.google.com/detail/ibm-equal-access-accessib/lkcagbfjnkomcinoddgooolagloogehp) (optional)
* [Jam](https://chromewebstore.google.com/detail/jam/iohjgamcilhbgmhbnllfolmkmmekfmci) (optional, Chrome/Edge only - My recommended issue reporting tool)

## General Remediation Process <a href="#general-remediation-process" id="general-remediation-process"></a>

For each of the site’s pages, do the following:

### Use WAVE to find and fix issues <a href="#use-wave-to-find-and-fix-issues" id="use-wave-to-find-and-fix-issues"></a>

1. Open the URL and activate WAVE
2. Click the **Details** tab and review
   1. For anything marked as an **Error**, **Alert**, or **Feature**:
      1. Ignore any **Contrast Errors** for now (we’ll come back to them)
      2. Click the icon for the reported issue and review it in the context of the page.
      3. If you are unsure of what an issue means, click the small “i” icon next to the error icon. This opens a reference that explains the error and recommends how to fix it.
      4. If you believe the issue is accurate, go ahead and fix the item so that it no longer gets flagged by WAVE.
      5. If you believe the issue is a false positive, make a note in the task comments and move on.
3. Anything marked as a **Structural Element** or **ARIA** is mostly provided as information. It’s worth reviewing and may help identify problems, but usually doesn’t require action.
4. Click the **Order** tab and review
   1. Imagine you’re navigating the page by repeatedly pressing the `tab` key and read through the list to assess the following:
      1. Does the item name and description make sense?
      2. Does the order match the intent of the page? Usually this means that the items are in the order that sighted users would encounter them reading top-to-bottom, left-to-right.
      3. If the answer is “no” to either of the above, make the necessary adjustments in the site’s code/content and re-run WAVE.
5. Click the **Structure** tab and review
   1. Review the heading levels and grouping of elements to make sure they are logical, semantic, and match the intent of the page.
      1. Proper levels and nesting of header tags are the most common problem you’re likely to find here.
      2. If anything looks wrong, make the necessary fixes and re-run WAVE
6. Click the **Contrast** tab and review
   1. Contrast errors are collected here, along with information and color sliders. WAVE has a lot of false positives with contrast issue detection, so use the provided tools to assess whether there’s really a problem.
   2. If you believe the issue is accurate, go ahead and fix the item so that it no longer gets flagged by WAVE.
   3. If you believe the issue is a false positive, make a note in the task comments and move on.

### Double-check and strengthen the page by repeating the process with other tools <a href="#double-check-and-strengthen-the-page-by-repeating-the-process-with-other-tools" id="double-check-and-strengthen-the-page-by-repeating-the-process-with-other-tools"></a>

Different tools highlight, catch, and explain accessibility issues in different ways. Using more than one tool can go a long way towards finding and fixing issues you may otherwise miss.

**Perform a cycle of testing and fixing the page like you did with WAVE with at least one more tool**

Some recommended tools are:

* [AXE](https://chromewebstore.google.com/detail/axe-devtools-web-accessib/lhdoppojpmngadmnindnejefpokejbdd) - If you turn on “Best Practices” mode, this tool gets very nitpicky and can find problems WAVE misses. It also does a good job of organizing and explaining the issues. It can be found alongside the other Chrome dev tools and is targeted towards power-users
* [ARIA Dev Tools](https://chromewebstore.google.com/detail/aria-devtools/dneemiigcbbgbdjlcdjjnianlikimpck?hl=en) - Ideally, pages are tested in an actual screen reader. If you don’t have time for that, the ARIA Dev Tools do a good job of showing how screen readers will group and interpret your content. Clicking the name of an ARIA tag provides additional information about how/why it’s being interpreted that way.
* [IBM Equal Access](https://chromewebstore.google.com/detail/ibm-equal-access-accessib/lkcagbfjnkomcinoddgooolagloogehp) - Another page scanner like WAVE and AXE. It defaults to IBM’s own accessibility standard, but can be switched to WCAG standards in the settings.

### If there are any issues you can’t fix easily or have recommendations <a href="#if-there-are-any-issues-you-cant-fix-easily-or-have-recommendations" id="if-there-are-any-issues-you-cant-fix-easily-or-have-recommendations"></a>

Sometimes you need more time to fix a complicated issue, or you need help from someone else. Create an task in Asana and assign it the appropriate party.

I recommend using the reporting tool called [Jam](https://chromewebstore.google.com/detail/jam/iohjgamcilhbgmhbnllfolmkmmekfmci). It’s easy to use and records browser logs alongside your screencast.
