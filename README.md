
# git-intro
Introduktion till versionshantering i Git.

Den officiella boken finns fritt på: https://git-scm.com/book/ En kortare cheat sheet: https://education.github.com/git-cheat-sheet-education.pdf

Fin, lång genomgång av massa git: https://www.youtube.com/watch?v=RGOj5yH7evk

## Versionshantering?

Följande videos (~5min / video) är en kort intro till versionshantering och Git.
* https://git-scm.com/video/what-is-version-control
* https://git-scm.com/video/what-is-git 
* https://git-scm.com/video/get-going (delar är redan sagt i del 1)
* https://git-scm.com/video/quick-wins (denna kan ni bara skumma, minst viktig av dessa 4) 

## Git-övningar

Git är ett distribuerat versionssystem vilket betyder att all data finns på alla klienter. Du arbetar med dina ändringar lokalt på din dator (`add` och `commit`) som sedan laddas upp (`push`) och ner (`pull`). 

### 1. Skapa och ladda ner ett repository på Github

Logga in på Github och skapa ett nytt repository i webbgränssnittet. Döp det till `learning-vcs.git`. Du kan göra det privat. Lämna övriga saker.

Öppna en mapp där du brukar spara dina projekt i terminalen. Hämta hem ditt nya repo `git clone git@github.com:olantig/learning-vcs.git` Glöm inte ersätta ***olantig*** med din användare.  

Kolla med: `git status`

För att senare uppdatera / ladda ner ändringar från samma repository används `git pull`

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

Att spara ändringar i git är en tvåstegsraket. Först lägger du till vad som ska sparas (`add`) och sedan sparar du det (`commit`). Det går att kombinera de två med `git commit -am "Här skriver du kommentaren"`

### 5. Ladda upp dina filer till Github

Ladda upp dina ändringar till Github med: `git push`. Försäkra dig om att de finns genom att öppna webbläsaren och se att ändringarna finns där.

Se historiken med `git log --oneline` eller överkursvarianten: `git log --graph --decorate --abbrev-commit --all --pretty=oneline`

## Delade repositories

Det finns (minst) två olika modeller för att samarbeta via Github. Ni kan antingen bjuda in alla som arbetar på projektet som collaborators via Github webbsidan. Detta funkar bäst till mindre projekt eller framförallt till projekt med färre deltagare.

I större projekt använder de oftast `fork` and `pull` där vem som helst kan göra en kopia på ett repository, arbeta i det och sedan be projektet lägga in in ändringarna (`merge`).

Läs: https://docs.github.com/en/github/collaborating-with-pull-requests/getting-started/about-collaborative-development-models 

## Branching och merging

Läs: 
* https://www.atlassian.com/git/tutorials/using-branches/git-checkout
* https://www.atlassian.com/git/tutorials/using-branches/git-merge 

När du lägger till en feature är ett vanligt sätt i Git-projekt att du skapar en branch, gör dina ändringar och sedan mergar tillbaka ändringarna till huvudkoden. Det finns flera fördelar. Bland annat skapas en isolerad miljö dit du kan testa dina ändringar i lugn och ro utan att riskera att röra något i övriga projektet.

Som standard på Github får alla repositories en branch som heter `main`.

Skapa en ny och byt aktiv branch till din nya med kommandot: `git checkout -b ny-branch`.
Se vilka branches som finns i repositoryt på din dator: `git branch`. 
Byter tillbaka till main: `git checkout main`. 

När du arbetat färdigt gör du som vanligt, `git commit -ma "Ny feature"`. Du behöver dessutom ladda upp din nya branch till servern (den finns än så länge bara på din dator) och då måste du berätta till var den ska pushas: `git push --set-upstream origin ny-branch`.

När du arbetat färdigt i din nya branch är det dags att merga den till main. 

Byt aktiv branch till main (`git checkout main`) och merga med: `git merge ny-branch`. Git försöker slå ihop filerna automatiskt men finns det ändringar på samma rad måste du hantera det manuellt. Då får du en sk. merge-konflikt (se bild).

![Exempel på mergekonflikt](img/git-merge-exempel-konflikt.png)

När du mergat din branch kan du ta bort den med `git branch -d ny-branch`. Den försvinner lokalt men finns kvar på Github. Titta under branches i ditt repository på github.com.

`git diff` viskar vilka ändringar som gjorts sedan commit. Går även att jämföra olika branches.

## SSH och SSH-nycklar

För att kunna använda Git helt från terminalen behöver du logga in med SSH-nycklar. Det är ett säkert sätt att autentisera dig. Du skapar en privat och en publik nyckel, den publika laddas upp till Github och den privata sparar du på din dator. När du loggar in förstår Github vem du är automagiskt.

Läs: https://en.wikipedia.org/wiki/Secure_Shell och https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh/about-ssh 

Om du använt Github desktop KANSKE den har skapat och lagt till nycklarna utan att du märkt det. Då kan du nog använda dem. Annars får vi skapa nya nycklar: https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent

## Strategier 

TODO: Tex hur ofta commitar och pushar man?
