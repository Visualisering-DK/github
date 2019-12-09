# Initialisering af et git repository
Skridt til gennemgang. Oprettelse af lokalt repository og tilføjelse af fil. Gennemgang kan også optages på video så eleverne kan gense det i eget tempo.

## Oprette git repository
Oprettelse eller initialisering af et lokalt git repository.

1. Opret mappe til projekt
    * `mkdir MAPPENAVN`
2. Åben mappe i VS Code
    * `code MAPPENAVN`
3. I det nye VS Code vindue. Åben terminal (Ctrl + æ) og sæt sidebar til git-visning (Ctrl + Shift + G)
4. Initialisering af et git repository i terminal. Git-visningen ændre sig i VS Code og der kommer et 'master' i terminal.
    * `git init`
5. Der er nu oprettet en mappe `.git/` som består af informationer til det nye repository
    * `ls -la`

## Oprette fil og tilføje til repository
Oprette den første fil og begynd at få git til at følge med ændringer.

1. Opret en README.md fil
    * `touch README.md`
2. Git kan se at filen er der men, git tracker den endnu ikke
    * `git status` viser at den er untracked.
    * I VS Code står der et lille `U` ud for filen for at indikere at den er untracked
3. Filen er i det git kalder `working directory`. Det er her hvor filer vi har ændret eller tilføjet ligger
4. Næste skridt i et git-flow er at flytte filen til `staging area`. Flyt README.md
    * `git add README.md`
    * I VS Code git-visning. Hold musen over filen og tryl på plus
5. Vis med `git status` hvordan filen er flyttet til `staging area`
6. For at git kan tage et snapshot af hvordan README.md ser ud lige nu, skal den flyttes til sidste state `local repository`. Filen flyttes når vi binder, eller committer os til de nuværende ændringer med `git commit`
7. En god commit har en præcis og kort (maks 50 tegn) beskrivelse af ændringen. Den skal kommunikere kontekst til os selv og vores medudviklere. For at skrive beskeden tilføjes flaget `-m` efterfuldt af citationstegn med beskeden i.
    * `git commit -m "Oprettet README.md"`
8. Vis med `git status` at der ikke længere er nogle untracked eller staged filer.
    * `git status`
9. I stedet er vores commit blevet tilføjet til loggen
    * `git log`
10. I takt med at et git repository udvikler sig bliver loggen også det længere. Loggen skal hjælpe med at forstå projektets historie, forstå hvilke ændringer der førte til hvad og hvorfor. 