Polyglot für Android / Termux (ARM64)

Dieses Repository enthält eine für Android ARM64 unter Termux angepasste Fassung von Polyglot.

Grundlage ist der Polyglot-Quelltext von Ulf Thiel. Die Android-Portierung beseitigt die unter Termux auftretenden Inkompatibilitäten und ermöglicht eine native ARM64-Kompilierung.

Fertiges Portierungspaket

Unter

"archive/Polyglot_Android_arm64_2026-08-27.zip"

liegt das vollständige Portierungspaket.

Es enthält die für eine erneute Kompilierung erforderlichen Quellen und Android-Anpassungen, insbesondere:

- Polyglot-Quelltext
- "Android-pipex-wordexp.patch"
- "Android-util-timeb.patch"
- "config.guess-Android-aarch64"
- "config.sub-Android-aarch64"
- "build-polyglot-Android-arm64-native.sh"
- bereits erzeugtes ARM64-Kompilat

Erneut unter Android/Termux kompilieren

Voraussetzung ist ein aktuelles Termux mit den üblichen Entwicklungswerkzeugen, insbesondere "clang", "make", "autoconf" und "automake".

Archiv entpacken, in das entpackte Verzeichnis wechseln und das mitgelieferte Buildskript ausführen:

bash build-polyglot-Android-arm64-native.sh

Das Skript enthält den für diese Portierung festgelegten Buildablauf und verwendet die mitgelieferten Android-Anpassungen.

Damit muss die Portierung nicht erneut entwickelt werden: Das Archiv dient als reproduzierbarer Ausgangsstand für einen erneuten nativen ARM64-Build unter Termux.

Ziel

Das erzeugte Polyglot dient unter Android insbesondere als Schnittstelle zwischen XBoard und einer Schachengine sowie zur Nutzung und Erzeugung von Polyglot-Binärbüchern.
