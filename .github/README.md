![Nordic Door logo](https://user-images.githubusercontent.com/27065646/192570400-5977d069-1a3f-454c-bc20-74969d42c755.png)

## Før du kjører programmet:
* Lag en database i MariaDB
    * Du kan installere enten lokalt eller i Docker, følg gjerne en tutorial på det
    * Kjør kommandoene i `PDSA_System.Server/Database/Create.sql` i en egen database
    * Opprett en testbruker i tabellen `Bruker` etter gjeldende instruksjoner (TBA)
* Sett inn en connection string i filen `appsettings.json`, der du ser `ConnectionString.DefaultConnection`. Denne skal følge dette formatet:
  * `server={DIN_IP_ADRESSE};user={BRUKERNAVN};database={DATABASENAVN};port={PORT};password={PASSORD}`
  * Dersom du kjører database og server på samme maskin, kan du bruke `localhost` eller `127.0.0.1` som IP-adresse
  * Det er anbefalt å bruke port 3306, da dette er standard for MySQL og MariaDB

## Hvordan starte serveren?
### Kjøre programmet:
```console
$ cd nordicdoor/PDSA_System/Server/ 
$ dotnet run
```

### Kjøre programmet med Hot Reload:
Dette vil automatisk laste inn nye endringer når du lagrer filer, noe som gjør at du ikke trenger å restarte programmet for hver endring

```console
$ cd nordicdoor/PDSA_System/Server/ 
$ dotnet watch run
```

### Kjøre testene:
*Ikke implementert*
