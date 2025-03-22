ls - listanje na site datoteki na rabotniot imenik
ls -a site datoteki od rabotniot imenik vklucuvajki gi i skrieni
ls -s ja prikazuva sodrzinata na rtabotniot imenk i goleminite na datotekite vo KB
ls | more ako ima povekoje datoteki vo imenikot da gi prikaze strana po strana
ls -l gi prkazuva datotekite od rabotniot imenik vo tn dolg format


ls -l

### Explanation of Columns:
| Column | Description |
|--------|-------------|
| (1) | File type and permissions |
| (2) | Number of hard links |
| (3) | Owner of the file |
| (4) | File size in bytes |
| (5) | Last modification date/time |
| (6) | Filename |

[File Type] [Owner] [Group] [Others] - SINTAKSA

### (1) File Type & Permissions:
The first column shows file type and access permissions:

- **File Type:**
  - `-` : Regular file  
  - `d` : Directory  
  - `l` : Symbolic link  

- **Permissions:**  
  - `r` : Read permission  
  - `w` : Write permission  
  - `x` : Execute permission  
  - `-` : No permission  

Example:  
`drwxr-xr-x`  
- `d` → Directory  
- `rwx` → Owner has **read, write, execute** permissions  
- `r-x` → Group has **read, execute** permissions  
- `r-x` → Others have **read, execute** permissions  

### (2) Number of Hard Links:
Indicates how many hard links point to the file.

### (3) Owner:
Displays the user who owns the file.

### (4) File Size:
Shows the file size in **bytes**.

### (5) Last Modification Date:
- If modified **this year** → shows **date and time**  
- If modified **previous years** → shows **date and year**  

### (6) Filename:
The name of the file or directory.

## Example Usage:
```bash
ls -l
ls -lh  # Human-readable sizes
ls -la  # Show hidden files


ls -l DOPOLNUVANJE

type: tip na datoteka

'-' obicna; d - imenik' l - vrska (link)
user prava na pristap do datotekata za sopstvenikot na datotekata
gruop - prava na prstap za korisnicite od istata grupa na korisnici na koja pripagja sopstvenikot na datotekata
other - prava na prostap do datotekata za site ostanati korisnici na sistemot

DOZVOLI ZA PRISTAP DO DATOTEKATA
r - dozvola za ctanje
w - dozvola za zapisuvanje
x - dozvola za izvrsuvanje


PROMENA NA PRIVILEGII - chmod

chmod - gi menuva privilegiite na datotekite i imenicite
sintaksa: chmod [options] mode file

PRIMERI:
chmod ug+rw sample
chmod +r file
chmod -x file
chmod u=rw, go=file
chmod +rw file chmod -R u+w, go-w docs/
chmod 666 file chmod 755 file
chmod -R u+rwX,g-rwX,g-rwx,o-rwx <directory>

NUMERIC MODE
r = 4
w = 2
x = 1

KREIRANJE DATOTEKI

nano dat.txt - se otvara

KOPIRANJE NA DATOTEKI -cp
opcii:

-i, interaktiven rezim koj vazi za superkorisnik
-f, forsirran rezim
-l namesto kopija se kreira hard link
-s namesto kopija se kreira simbolicen link
-r rekurzivno kopiranje za obicni datoteki
-p opcija preserve
-b se kreira rezervna kopija

PREMESTUVANJE NA DATOTEKI I IMENICI -mv
mv izvor odrediste - IZVOROT MOZE DA BIDE I DATOTEKA I IMENIK
destinacijata e pateka(apsolutna ili relativa) do noviot imenik kade se vrzi premestuvanjeto 
Ако се наведе ново име на датотеката (именикот), таа ќе биде преместена под новото име

mv moj.txt /users/student - moj.txt se premestuva vo /users/student pod istoto ime
mv moj.txt /users/student/mojnov.txt se premestuva vo /users/student pod novo ime mojnov.txt
mv student/users/admin - imenikot student se premestuva vo /users/admin pod istoto ime
mv proba.txt proba.txt se preimenuva vo moj.txt

BRISENJE NA DATOTEKI I IMENICI -rm

rm ime - za datoteki i prazni imenici
rm moj.txt - moj.txt se brise
rm - r imeimenik - za ovaa komanda e potrebno da se naogjame vo imenikot roditel na onoj sto se brise. So ova ke se izbrisat i site podimenici i datoteki na konkretniot imenik
rm -r student - se brise imenikot student, so celate svoja sodrzina -r e za rekurzivno brisenje
rm res.01 res.02 - gi brise dvete datoteki

PRIKAZUVANJE NA DATOTEKA NA EKRAN
cat file
cat proveri.p

MOZNI OPCII:
-b gi ignirira praznite linii i  go numerira sekoj red
-n fi numerira site linii ( i praznite)
-s gi otfrla dvojnite prazni redovi

cat
ovaa komanda iam povekje nacini na koristenje
ke pokazeme deka mo\e da ja iskoristime za dodavanje na sodrzinata na krajot na datotekata, so koristenje na operatorot>>


