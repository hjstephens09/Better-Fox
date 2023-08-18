![GitHub Maintained](https://img.shields.io/badge/open%20source-yes-orange)
![GitHub Maintained](https://img.shields.io/badge/maintained-yes-yellow)
[![Visitors](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fyokoffing%2FBetter-Fox&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=visitors&edge_flat=false)](https://hits.seeyoufarm.com)

# Betterfox :fox_face:
`about:config` tweaks to enhance [Mozilla Firefox](https://www.mozilla.org/en-US/firefox/new/ "Firefox Homepage"). Files are updated as needed for your [user.js](http://kb.mozillazine.org/User.js_file).

## Made for everyday browsing
**A secure, blazing fast browsing experience. Without breakage.**

Betterfox is an opinionated preference list inspired by the [law of diminishing returns](https://pmctraining.com/site/wp-content/uploads/2018/04/Law-of-Diminishing-Returns-CHART.png) and the [minimum effective dose](https://medium.com/the-mission/less-is-more-the-minimum-effective-dose-e6d56625931e).

## Simple goals
1) **Minimalism:** get what isn't needed out of the way
2) **Efficiency:** unleash Firefox's ability to be fast and performant
3) **Privacy:** protect your data without causing site breakage

## Simple configs

| List      | Description |
|:---------:|-------------|
| [Fastfox](https://github.com/yokoffing/Betterfox/blob/main/Fastfox.js)   | Immensely increase Firefox's browsing speed. Give Chrome a run for its money!|
| [Securefox](https://github.com/yokoffing/Betterfox/blob/main/Securefox.js) | [Global Privacy Control](https://blog.mozilla.org/netpolicy/2021/10/28/implementing-global-privacy-control/). [HTTPS-by-Default](https://blog.mozilla.org/security/2021/08/10/firefox-91-introduces-https-by-default-in-private-browsing/). [Total Cookie Protection](https://blog.mozilla.org/security/2021/02/23/total-cookie-protection/) with [site isolation](https://blog.mozilla.org/security/2021/05/18/introducing-site-isolation-in-firefox/). Enhanced [state](https://developer.mozilla.org/en-US/docs/Web/Privacy/State_Partitioning) and [network](https://blog.mozilla.org/security/2021/01/26/supercookie-protections/) partitioning. [Telemetry](https://github.com/yokoffing/Betterfox/blob/e66a549985f6b0db4b14226904b8c09eaaea998f/Securefox.js#L1262-L1265) disabled. |
| [Peskyfox](https://github.com/yokoffing/Betterfox/blob/main/Peskyfox.js)  | Unclutter the new tab page. Remove [Pocket](https://support.mozilla.org/en-US/kb/what-pocket). Restore [compact mode](https://support.mozilla.org/en-US/kb/compact-mode-workaround-firefox) as an option. Stop webpage notifications, pop-ups, and other annoyances. |
| [Smoothfox](https://github.com/yokoffing/Betterfox/blob/main/Smoothfox.js) | Get Edge-like smooth scrolling on your favorite browser — or choose something more your style. |
| [user.js](https://github.com/yokoffing/Betterfox/blob/main/user.js) | All the essentials. None of the breakage. This is your `user.js`. |

:bulb: `Fastfox`, `Securefox`, `Peskyfox`, and `Smoothfox` are guides to relevant prefs in Firefox. The `user.js` is curated from the options located in these documents. Please read the guides to understand the various options hidden in Firefox.

While Betterfox is designed to [set-and-forget](https://glosbe.com/en/en/set-and-forget), it contains plenty of options for those who like to tinker.

## about:Defaults
Apply preferences from the [common overrides](https://github.com/yokoffing/Betterfox/issues/87) sticky to adjust the following behavior:
* Firefox **Accessibility Service** is disabled to improve resource utilization and security. Override this if you use assistive software.
* **Firefox Sync** and **Firefox View** are disabled. Override if you use these features.
* The built-in **password manager** is disabled. We recommend using [Bitwarden](https://addons.mozilla.org/en-US/firefox/addon/bitwarden-password-manager/) or [1Password](https://addons.mozilla.org/en-US/firefox/addon/1password-x-password-manager) to manage your credentials on multiple devices.
* **Top sites** (pinned site shortcuts) are removed for a clean new tab page.
* **Location requests** and **site notifications** are blocked to minimize annoyances.

You can easily adjust these by [copying and pasting](https://github.com/yokoffing/Betterfox/issues/87) preferences to your personal file. :thumbsup:

## about:Privacy
While Betterfox is already a great balance of privacy and convenience, here are a few ways to further **harden** your setup:

<details>
  <summary><i>Click me for details!</i></summary><p></p>

1) Change your **default search engine**.
   * Alternatively, select a different search engine just for [Private Browsing](https://support.mozilla.org/en-US/kb/private-browsing-use-firefox-without-history) windows.
      1) Go to *Settings → Search → Default Search Engine*
      2) Change your default search engine to DuckDuckGo, or [add](https://github.com/yokoffing/Betterfox/blob/04c3184359c83d7b58411c3b68f40f3e9d95c373/Securefox.js#L600-L604) a premium search engine like [Kagi](https://kagi.com/).
2) **Clear browsing data** on shutdown ([sanitize on close](https://github.com/yokoffing/Betterfox/blob/99f2e860633f307781ddb73d792358ad1bec6af5/Securefox.js#L409-L434)).
   * You can **allow exceptions** if you want to stay logged in to some sites:
      1) Go to *Settings → Privacy & Security → Cookies and Site Data → Manage Exceptions*
      2) Check *Delete cookies and site data when Firefox is closed*.
3) Apply preferences from the [common overrides](https://github.com/yokoffing/Betterfox/issues/87) sticky to enforce the following behavior:
   * Block embedded **tweets, tiktoks, Instagram and Reddit posts** from loading on third-party sites.
   * **Hide the referrer** from different sites.
   * Enable **HTTPS-Only Mode** outside of [Private Browsing](https://support.mozilla.org/en-US/kb/private-browsing-use-firefox-without-history) windows.

We do not use [`privacy.resistFingerprinting`](https://old.reddit.com/r/firefox/comments/wuqpgi/are_there_any_aboutconfig_tweaks_to_get_smooth/ile3whx/?context=3). Fingerprinting is a high [threat model](https://thenewoil.org/en/guides/prologue/threatmodel/) issue that is only [addressed](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) reasonably by Tor.<sup>[1](https://youtu.be/5NrbdO4yWek?t=4334)</sup> Please use the [Tor Browser](https://www.torproject.org) if your context calls for **anonymity** and not just reasonable **privacy**.<sup>^[*what's the difference?*](https://thenewoil.org/en/guides/prologue/secprivanon/)</sup>

</details>

## Suggestions
After applying the `user.js` and restarting Firefox:
1) Use an **ad blocker** like [uBlock Origin](https://addons.mozilla.org/blog/ublock-origin-everything-you-need-to-know-about-the-ad-blocker/) with our [recommended filters](https://github.com/yokoffing/filterlists#guidelines). For a quick and easy solution, use [Ghostery](https://addons.mozilla.org/en-US/firefox/addon/ghostery/).
2) Add **DNS-level protection** like [NextDNS](https://nextdns.io/?from=xujj63g5), and check out our configuration [guide](https://github.com/yokoffing/NextDNS-Config).

## Recognition

### Browser Integration
* [Waterfox](https://github.com/WaterfoxCo/Waterfox/commit/735d8067b06cca00b9b04b5a6bcd0c1414118f95) | [files](https://github.com/WaterfoxCo/Waterfox/tree/future/waterfox/browser/app/profile) (August 2023)
* [Floorp](https://github.com/Floorp-Projects/Floorp#-betterfox) <sup>[1](https://github.com/Floorp-Projects/Floorp/issues/233#issuecomment-1543557167) [2](https://blog.ablaze.one/3135/2023-04-01/)</sup> | [files](https://github.com/Floorp-Projects/Floorp/blob/f63e87016d88535aafa2b57d690442b9a69cbaa5/toolkit/content/license.html#L200-L224) (April 2023)
* [Pulse](https://github.com/pulse-browser/browser#%EF%B8%8F-credits) | [files](https://github.com/pulse-browser/browser/tree/alpha/src/browser/app/profile) (Dec 2021)
* [Ghostery Private Browser](https://github.com/ghostery/user-agent-desktop#community) <sup>[1](https://web.archive.org/web/20210509171835/https://www.ghostery.com/ghostery-dawn-update-more/) [2](https://web.archive.org/web/20210921114333/https://www.ghostery.com/ghostery-dawn-product-update/)</sup> | [files](https://github.com/ghostery/user-agent-desktop/tree/main/brands/ghostery/branding/pref) (Feb 2021)

### YouTube
* [The ULTIMATE Browser Tier List](https://youtu.be/j5r6jFE8gic?t=560) (Mar 2023)
* [I Hate Firefox. But I'm Still Switching Back to It.](https://youtu.be/w0SJFED5xK0?t=220) (Nov 2022)
* [Español] [Optimize and Accelerate Firefox](https://www.youtube.com/watch?v=3XtoONmq5_Q) (Nov 2022) 
* [How To Improve Firefox Performance](https://www.youtube.com/watch?v=N8IOJiOFVEk) (Dec 2021)

### Podcasts
* [Italian] [Digitalia.fm](https://digitalia.fm/684/) | 1:41:35–1:42:41 (July 2023)
* [GhoSTORIES with Franz & Pete](https://anchor.fm/ghostories/episodes/S2E6-We-Talking-Ghostery-Dawn----Again-er0q02/a-a4o5vmh) | 17:05–18:40 (Feb 2021)

### Articles
* [German] [Pulse Browser Review: Firefox fork with Turbo tweaks and Opera sidebar](https://www.computerbild.de/artikel/cb-Tipps-Software-Pulse-Browser-Review-ein-Firefox-Fork-mit-Seitenleiste-wie-bei-Opera-35644139.html#:~:text=Noch%20mehr%20Speed%2DFeatures) (April 2023)
* [2023 Browser Showdown: Comparing Chrome, Brave, Firefox, Vivaldi, and Opera](https://www.appdate.lk/technology/2023-browser-showdown/) (Jan 2023)

### Guides
* [FMHY Browser Tools: Privacy Tweaks](https://www.reddit.com/r/FREEMEDIAHECKYEAH/wiki/storage/#wiki_privacy_based_browsers)
* [Firefox-UI-Fix](https://github.com/black7375/Firefox-UI-Fix/wiki/Tips#privacy)
* [Narsil/desktop_user.js](https://git.nixnet.services/Narsil/desktop_user.js#thanks)
* [pyllyukko/user.js](https://github.com/pyllyukko/user.js) [comparator](https://jm42.github.io/compare-user.js/)

### Reviews
* “I’ve been using it for awhile and it’s actually really, really good. The performance is actually crazy.” - [DIRIKtv](https://youtu.be/N8IOJiOFVEk?t=213)
* "... a good balance between privacy and convenience." - [Radplay](https://old.reddit.com/r/firefox/comments/115va7d/list_of_aboutconfiguserjs_privacy_tweaks/j9700bc/?context=2)
* "The best collection of tweaks available ... doesn't go crazy with privacy/security hardening that completely breaks the usability of Firefox for most users." - [AuRiMaS](https://old.reddit.com/r/MozillaFirefox/comments/15cc1vk/about_changes_in_aboutconfig/jtyx910/?context=3)
* "... the experience is so good now I don’t think I’ll go back to any of the chromium based browsers." - [Mr_Compromise](https://old.reddit.com/r/pcmasterrace/comments/zwioe1/what_browser_will_you_be_using_in_2023_please/j1wmbxo/)
* "FF is now much snappier! Thanks a lot for the suggestions!" - [whotheff](https://old.reddit.com/r/firefox/comments/z5auzi/firefox_not_properly_usingrecognizing_gpu_poor/iy36hyz/)
* "BetterFox ... will provide good-enough privacy and help with performance." - [Qdoit12Super](https://old.reddit.com/r/browsers/comments/139h4my/suggestion_for_finding_3_good_privacy_focus/jj3n3qn/?context=2)
* "... drastically changed the experience with Firefox for me. Improved speed, security, smoothness and removed clutter." - [AppDate](https://www.appdate.lk/technology/2023-browser-showdown/#:~:text=Used%20the%20BetterFox%20user%20config%20settings%20with%20some%20overrides%20which%20drastically%20changed%20the%20experience)
* “I use this one. I tested this out. The performance is absolutely amazing. There’s definitely a huge difference when it comes to loading sites… You definitely can notice a difference.” - [DIRIKtv](https://youtu.be/N8IOJiOFVEk?t=16)

## Support

If you like the project and benefit from it, leave a :star: (top right) and become a [stargazer](https://github.com/yokoffing/Betterfox/stargazers)!

[![Stargazers repo roster for @yokoffing/Betterfox](https://reporoster.com/stars/dark/yokoffing/Betterfox)](https://github.com/yokoffing/Betterfox/stargazers)  

## Credit
<div>
<img align="right" src="https://media.tenor.com/m_knf6IKaJwAAAAC/hi-fox.gif" width="110" height="120"/>
</div>

* This repository benefits from the ongoing research provided by [arkenfox](https://github.com/arkenfox/user.js).
* Appreciation goes to the [Firefox](https://www.mozilla.org/en-US/firefox/new/) team and the developers working on [Bugzilla](https://bugzilla.mozilla.org/home), fighting for the open web.
* A special thanks to [Alex Kontos](https://github.com/MrAlex94) of [Waterfox](https://github.com/WaterfoxCo/Waterfox) for his collaboration in v.116.
* Many thanks to the 2021 [Ghostery](https://github.com/ghostery) team for testing Betterfox at scale in its early days.

<div align='center'>
  <a href='https://www.websitecounterfree.com'><img src='https://www.websitecounterfree.com/c.php?d=9&id=19653&s=1' border='0' alt='Free Website Counter'></a><br / >
since 23 July 2022</div>
