
# git-intro
Introduktion till versionshantering i Git

## Versionshantering?

Följande videos (~5min / video) är en kort intro till versionshantering och Git.
* https://git-scm.com/video/what-is-version-control
* https://git-scm.com/video/what-is-git 
* https://git-scm.com/video/get-going (delar är redan sagt i del 1)
* https://git-scm.com/video/quick-wins (denna kan ni bara skumma, minst viktig av dessa 4) 

## Git-övningar

Git är ett distribuerat versionssystem vilket betyder att all data finns på alla klienter. Du arbetar med dina ändringar lokalt på din dator (`add` och `commit`) som sedan laddas upp (`push`). 

### 1. Skapa och ladda ner ett repository på Github

Logga in på Github och skapa ett nytt repository i webbgränssnittet. Döp det till `learning-vcs.git`. Du kan göra det privat. Lämna övriga saker.

Öppna en mapp där du brukar spara dina projekt i terminalen. Hämta hem ditt nya repo `git@github.com:olantig/learning-vcs.git` Glöm inte ersätta olantig med din användare.
Kör: `git status`

### 2. Lägg in en ny fil till i repository

Skapa filen `fil1.txt` (med `touch fil1.txt` eller en editor) i din projektmapp

Kör: `git status`

Kör: `git add .`

Kör: `git status`

Kör: `git commit -m “Skapade dokumentet”`

Kör: `git status`

Vad gör kommandona?

### 4. Uppdatera en fil

Öppna filen fil1.txt i din texteditor, lägg till innehåll, spara

Vad säger: `git status`?

Kör: `git commit -m "Skrev första stycket` Sparas dina ändringa till repositoriet? Vad säger: `git status`? 

Att spara ändringar i git är en tvåstegsraket. Först lägger du till vad som ska sparas (`add`) och sedan sparar du det (`commit`).

### 5. Ladda upp dina filer till Github

Ladda upp dina ändringar till Github med: `git push`. Försäkra dig om att de finns genom att öppna webbläsaren och se att ändringarna finns där.

Se historiken med `git log` eller överkursvarianten: `git log --graph --decorate --abbrev-commit --all --pretty=oneline`

## Delade repositories

## SSH och SSH-nycklar

## Strategier 
Tex hur ofta commitar och pushar man?


