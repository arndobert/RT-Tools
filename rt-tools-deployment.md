# RT Tools – Deployment auf iPhone (GitHub Pages, danach offline)

Stand: 28.09.2026

## Dateien (alle in die oberste Ebene des Repos)
- index.html – App (Direkteinstellung, Handrechnung, BED/EQD2), Monitortabellen eingebettet
- sw.js – Offline-Cache (cache-first), aktuelle Version: `rt-tools-v2`
- manifest.webmanifest – App-Name/Icon für den Home-Bildschirm
- icon-180.png, icon-512.png – App-Icon (Variante D: Strahlerkopf mit Gantry-Arm)

## Einrichten
1. GitHub: neues öffentliches Repo, Dateien hochladen.
2. Settings → Pages → Source „Deploy from a branch“, Branch `main` / `/ (root)` → Save.
3. iPhone: Adresse in **Safari** öffnen (nicht Firefox/Edge – dort kein App-Icon) → Teilen → „Zum Home-Bildschirm“.
4. App einmal online vom Home-Bildschirm starten, dann im Flugmodus testen.
5. Pages wieder deaktivieren (Branch „None“) oder Repo löschen. App läuft weiter offline.

## Updates
- Pages kurz wieder aktivieren, neue Dateien hochladen, in sw.js die CACHE-Version hochzählen.
- App online öffnen, schließen, erneut öffnen → neue Version aktiv.

## Hinweise
- Wird das Icon vom Home-Bildschirm gelöscht, ist die App weg → zum Neuinstallieren kurz wieder online stellen.
- Rechenwege: ÄQ = 2ab/(a+b); MU/Gy bilinear interpoliert (Tiefe × ÄQ), keine Extrapolation; BED = n·d·(1+d/(α/β)), EQD2 = BED/(1+2/(α/β)).
