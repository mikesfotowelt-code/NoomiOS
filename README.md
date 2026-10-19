# NoomiOS – Build-Entwurf 0.1

Dieses Archiv ist ein **Build-Entwurf**, keine startfähige ISO. Es verändert keine Festplatten.

## Hardware
AMD Ryzen 5 4500, Radeon RX 6800, Gigabyte B550M DS3H R2; Bazzite KDE.

## Bereits enthalten
`recipes/recipe.yml` – BlueBuild-Rezept, das die Bazzite-Basis mit einem Satz Flatpak-Desktopanwendungen ergänzt. Flatpaks werden bei der Einrichtung installiert, nicht als vollständige Anwendungsdaten in der ISO gespeichert.

## Aktuell bewusst nicht automatisch enthalten
- **AION 2**: Linux-Login/Anti-Cheat-Kompatibilität zuerst testen.
- **OBSBOT Meet 4K Steuerprogramm**: Community-Code wird nicht ungeprüft mit Systemrechten installiert; Standard-USB-Videobetrieb zunächst über OBS testen.
- **DaVinci Resolve**: Linux-Installation und AMD-Unterstützung gesondert testen.
- **StarMoney / Office LTSC**: durch Browser-Banking bzw. ONLYOFFICE ersetzt.
- **BIOS und AMD Windows-Treiber**: nicht in ein Linux-Image kopieren. Bazzite liefert Kernel-/Mesa-/Firmware-Treiber.

## Tatsächlicher ISO-Build (Linux-Build-Host erforderlich)
Gemäß https://blue-build.org/how-to/generate-iso/ :

    sudo bluebuild generate-iso --iso-name noomios.iso recipe recipes/recipe.yml

Vorher müssen die verwendeten Image-Tags/Flatpak-IDs und die BlueBuild-CLI gegen den aktuellen Upstream verifiziert werden. Ein erfolgreicher Build und ein Boot-/Installations-Test stehen aus.

## Wichtig
Nicht ohne Prüfung der Datenträgerauswahl installieren. Der bisherige Rufus-Stick bleibt ein unverändertes offizielles Bazzite-Medium. Für den AION-2-Test muss Windows vorerst erhalten bleiben.
