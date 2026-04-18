# mobile-terminal-preview

Visueller Prototyp der **Mobile Terminal** iOS-App — single-file HTML, damit man sie am Handy im Browser anschauen kann, ohne sie zu installieren.

Die echte App ist eine native SwiftUI-App für **iOS 26+** (Liquid Glass, SwiftTerm, Citadel SSH) und lebt unter [`schenkei/mobile-terminal`](https://github.com/schenkei/mobile-terminal). SwiftUI lässt sich nicht im Browser ausführen — daher dieser Preview.

## Was drin ist

- iPhone-14-Pro-Frame (393×852) mit Dynamic Island, fake Status-Bar
- **Sessions-Tab**: Terminal-Ansicht mit stream-json Output (thinking, Bash tool-use, tool-result, Edit-Diff, result-Summary), Session-Tab-Strip, Keyboard-Accessory (esc/tab/ctrl/Pfeile/⌃C/⌃D/⌃L/⌃Z), Chat-Input
- **Hosts-Tab**: 3 fake Hosts (nexa-prod, nexa-vps/NOX, homelab) mit Tailnet- + CC-Badges
- **Themes-Tab**: Live-Preview-Karten für Tokyo Night & Solarized Dark + Palette-Swatches
- **Einstellungen-Tab**: Hardware-Keyboard (CapsLock→Esc, Meta-as-Ctrl, tmux-Prefix), Claude stream-json overlay, Schrift, About

Tab-Wechsel funktioniert per Tap auf die Liquid-Glass-Tab-Bar unten.

## Tech

- Single-file `index.html`
- Tailwind via CDN, vanilla JS, inline SVG
- Kein Build, kein Framework, nichts zu installieren

## Lokal anschauen

`index.html` im Browser öffnen. Am Handy am besten aufs Deployment gehen — unter 430px Viewport wird die Phone-Chrome entfernt und der Inhalt füllt den ganzen Screen.
