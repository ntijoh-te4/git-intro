# git-intro
Introduktion till versionshantering i Git

## Versionshantering?

Följande videos (~5min / video) är en kort intro till versionshantering och Git.
* https://git-scm.com/video/what-is-version-control
* https://git-scm.com/video/what-is-git 
* https://git-scm.com/video/get-going (delar är redan sagt i del 1)
* https://git-scm.com/video/quick-wins (denna kan ni bara skumma, minst viktig av dessa 4) 

## Git-övningar


TODO: Vänd på steken. Dvs. skapa repot i github först, clona osv, sedan jobba mot det i övningarna

Git är ett distribuerat versionssystem vilket betyder att all data finns på alla klienter. Du arbetar med din data lokalt på din dator som sedan laddas upp. I första övningarna arbetar du med ett repository som bara finns lokalt på din dator. I nästföljande övningar skapar du ett repository på Github som du arbetar mot.

### 1. Skapa ett (lokalt) repository

Kör: `git init learning-vcs`

Undersök mappen learning-vcs (i terminalen). Vad finns i mappen?

Kör: `git status`

Vad gör de två kommandona?

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

### 5. 

`git remote add origin git@github.com:olantig/learning-vcs.git`
`git remote -v`


### 3. Historik
Kör: `git log --graph --decorate --abbrev-commit --all --pretty=oneline`


