# wp-rediteris
Snažíme sa zaprocovať na novom plugine pre Slovensku Wordpress komunity


**Upozornenie:** Tento článok a tento nástroj slúžia výhradne na technickú diskusiu a zdieľanie poznatkov. Akékoľvek nelegálne použitie je prísne zakázané.

---

## DetectDee: Vyhľadávanie účtov na sociálnych sieťach podľa používateľského mena, e-mailu alebo telefónneho čísla

**DetectDee** je nástroj, ktorý umožňuje vyhľadávať účty na rôznych sociálnych sieťach na základe používateľského mena, e-mailovej adresy alebo telefónneho čísla. Je obľúbený najmä medzi odborníkmi na kybernetickú bezpečnosť, ktorí ho využívajú na analýzu digitálnej stopy, OSINT (Open Source Intelligence) alebo pri vyšetrovaní.

### Hlavné funkcie DetectDee

- **Podpora viacerých platforiem:** Nástroj prehľadáva množstvo populárnych sociálnych sietí a platforiem, ktoré často využívajú aj bezpečnostní analytici.
- **Vyhľadávanie podľa viacerých údajov:** Môžete zadať používateľské meno, e-mail alebo telefónne číslo a nástroj sa pokúsi nájsť zodpovedajúce účty.
- **Presná kontrola požiadaviek:** DetectDee umožňuje detailné nastavenie požiadaviek (napr. vlastné HTTP hlavičky), čím sa minimalizuje riziko detekcie zo strany ochranných mechanizmov (WAF – Web Application Firewall).
- **Jednoduché rozšírenie a úprava:** Šablóny sú jednoduché na úpravu, takže si môžete pridať vlastné platformy alebo upraviť existujúce podľa potreby.
- **Podpora mobilných verzií stránok:** Nástroj dokáže pracovať aj s mobilnými verziami sociálnych sietí, čo zvyšuje šancu na úspešné vyhľadanie účtov.
- **Jednoduchá inštalácia a použitie:** Stačí stiahnuť repozitár, nainštalovať závislosti a spustiť nástroj.

### Inštalácia

1. Stiahnite si repozitár DetectDee (napr. cez GitHub).
2. Otvorte terminál a prejdite do priečinka s nástrojom:
   ```
   cd DetectDee
   ```
3. Nainštalujte potrebné závislosti:
   ```
   go mod tidy
   ```
4. Spustite nástroj:
   ```
   go run .
   ```

### Použitie

- Po spustení zadáte požadované údaje (používateľské meno, e-mail alebo telefón).
- Nástroj automaticky prehľadá podporované sociálne siete a zobrazí, kde sa daný údaj vyskytuje.
- Výsledky môžete využiť na technickú analýzu, testovanie bezpečnosti alebo OSINT účely.

---

**Poznámka:**  
DetectDee je určený výhradne na legálne a etické použitie, napríklad pri testovaní vlastných účtov, analýze bezpečnosti alebo v rámci výskumu. Akékoľvek zneužitie na nelegálne účely je zakázané a môže byť trestné.

---

Ak chceš podrobnejší návod alebo ukážku použitia, daj vedieť!


Samozrejme, tu je prepracovaný a rozšírený slovenský preklad s dlhšími vetami a vysvetleniami:

---

### DetectDee – Vyhľadávanie účtov na sociálnych sieťach podľa používateľského mena, e-mailu alebo telefónneho čísla

Nástroj **DetectDee** slúži na vyhľadávanie účtov na rôznych sociálnych sieťach na základe zadaného používateľského mena, e-mailovej adresy alebo telefónneho čísla. Tento nástroj je veľmi užitočný najmä pre odborníkov na kybernetickú bezpečnosť, analytikov, ale aj pre bežných používateľov, ktorí chcú zistiť, kde všade sa ich údaje môžu nachádzať na internete.

#### Základné použitie príkazu Detect

Na spustenie vyhľadávania účtov podľa zadaných údajov použite príkaz:

```
DetectDee detect
```

Pri tomto príkaze môžete využiť viacero voliteľných parametrov (tzv. „flags“), ktoré vám umožnia prispôsobiť vyhľadávanie podľa vašich potrieb:

- **-c, --check** – vykoná samokontrolu nástroja, aby ste sa uistili, že všetko funguje správne.
- **-e, --email** – umožňuje zadať jeden alebo viac e-mailov, podľa ktorých sa budú účty vyhľadávať.
- **-f, --file** – určíte súbor s údajmi o stránkach, ktoré sa majú prehľadávať (predvolený je „data.json“).
- **-g, --google** – zobrazí výsledky vyhľadávania aj z Google, čo môže rozšíriť vaše možnosti analýzy.
- **-h, --help** – zobrazí nápovedu k príkazu detect.
- **-n, --name** – zadáte jedno alebo viac používateľských mien, napríklad: `-n janko,ferko,niekto`.
- **--nsfw** – zahrnie do vyhľadávania aj stránky s obsahom pre dospelých (NSFW) z predvoleného zoznamu.
- **-o, --output** – určíte názov súboru, do ktorého sa uložia výsledky (predvolený je „result.txt“).
- **-p, --phone** – zadáte jedno alebo viac telefónnych čísel, napríklad: `-p 0905123456,0911123456`.
- **--precisely** – aktivuje presné vyhľadávanie, ktoré je dôkladnejšie, ale môže trvať dlhšie.
- **--proxy** – umožňuje vykonávať požiadavky cez proxy server, napríklad: `--proxy socks5://127.0.0.1:1080`.
- **-r, --retry** – nastavíte, koľkokrát sa má požiadavka zopakovať v prípade neúspechu (predvolené sú 3 pokusy).
- **-s, --site** – obmedzíte vyhľadávanie len na konkrétne stránky, ktoré zadáte (môžete zadať viac stránok naraz).
- **-t, --timeout** – určíte čas v sekundách, ako dlho sa má čakať na odpoveď od stránok (predvolené je 10 sekúnd).
- **--token** – zadáte ChatGPT API token, ak chcete využiť automatické označovanie výsledkov pomocou umelej inteligencie.

Globálne parametre:
- **-v, --verbose** – zapne podrobnejší výstup, vďaka čomu uvidíte viac informácií o priebehu vyhľadávania.

#### Prvé spustenie a aktualizácia údajov

Pri prvom použití nástroja je potrebné aktualizovať databázu stránok, ktoré sa budú prehľadávať. Urobíte to príkazom:

```
./DetectDee update
```

#### Príklady použitia

- Ak chcete vyhľadať účty len pre jedného používateľa, použite:
  ```
  ./DetectDee detect -n janko
  ```
- Ak chcete vyhľadať účty pre viacerých používateľov naraz, použite:
  ```
  ./DetectDee detect -n janko,ferko
  ```
- Ak chcete využiť ChatGPT na automatické označovanie výsledkov (potrebujete token):
  ```
  ./DetectDee detect -n janko,ferko --token {váš_ChatGPT_token}
  ```
- Ak chcete vyhľadávať podľa e-mailu:
  ```
  ./DetectDee detect -e niekto@email.com
  ```
- Ak chcete vyhľadávať podľa telefónneho čísla:
  ```
  ./DetectDee detect -p 0905123456
  ```
- Ak chcete zobraziť výsledky aj z Google:
  ```
  ./DetectDee detect -n janko,ferko -g
  ```
- Ak chcete obmedziť vyhľadávanie len na konkrétne stránky (napr. github a v2ex):
  ```
  ./DetectDee detect -n janko -s github,v2ex
  ```

#### Funkcia Screenshot

DetectDee umožňuje aj vytváranie snímok obrazovky (screenshotov) výsledkov vyhľadávania. Táto funkcia je užitočná, ak potrebujete zdokumentovať nájdené účty alebo uložiť vizuálny dôkaz.

**Na použitie tejto funkcie potrebujete:**
- Nainštalovaný prehliadač Chrome
- Dostatočný čas na spracovanie
- Trochu voľnej pamäte

Príkaz na vytvorenie screenshotov:
```
DetectDee screenshot [parametre]
```

Dôležité parametre pre screenshot:
- **--chrome** – zobrazí Chrome počas vytvárania screenshotov
- **-d, --dir** – určíte priečinok, kam sa screenshoty uložia (predvolený je „screenshots“)
- **-f, --file** – určíte súbor s URL adresami, ktoré sa majú screenshotovať (predvolený je „result.txt“)
- **--path** – zadáte cestu k spustiteľnému súboru Chrome
- **--proxy** – použijete proxy server na vytváranie screenshotov
- **-t, --thread** – nastavíte počet paralelných inštancií Chrome (predvolené sú 3)
- **--timeout** – nastavíte časový limit na vytvorenie screenshotu (predvolené je 60 sekúnd)

Príklad použitia:
```
./DetectDee screenshot result.jpg screen.jpg
```

#### Prispievanie do projektu

Vývojári DetectDee vítajú každú pomoc a príspevky od komunity. Ak máte záujem pomôcť, môžete napríklad:
- Pridať podporu pre nové stránky (stačí napísať JSON alebo upozorniť vývojára na dostupné rozhranie)
- Pomôcť s opravou stránok, ktoré boli v minulosti odstránené kvôli falošným pozitívam
- Pracovať na nových funkciách, ako je credential stuffing alebo podpora ďalších bezpečnostných portálov

#### Podporované stránky

DetectDee podporuje množstvo stránok a platforiem, ktoré sú často využívané v oblasti kybernetickej bezpečnosti, ako napríklad: Freebuf, HackerOne, BugCrowd, VirusTotal, ThreatPost, TryHackMe, Leetcode, Gitee, Quizlet, InfoQ, TechCrunch a mnohé ďalšie.

---

**Záver:**  
DetectDee je výkonný a flexibilný nástroj, ktorý vám umožní efektívne vyhľadávať digitálnu stopu na internete podľa rôznych údajov. Je vhodný pre profesionálov aj bežných používateľov, ktorí chcú mať prehľad o svojej online prítomnosti alebo analyzovať digitálnu stopu iných osôb. Vždy však dbajte na etické a legálne použitie tohto nástroja!

STRÁNKY:::

Secret
Supported site
CyberSecurity
 Freebuf
 HackerOne
 BugCrowd
 Jarvisoj
 VulFocus
 Secrss
 VirusTotal
 newBugKu
<a title="Chutná Vareška" href="https://chutnavareska.sk/">Chutná Vareška</a>
yystv
 XZ
 huoxian
 ywhack
 TheHackerWorld
 ThreatBook
 SecPulse
 HackerRank
 EastMoney-src
 Sec-Wiki
 90sec
 Googleplay
 BugBank
 ichunqiu
 Seebug
 0x00sec
 anquanke
 Infosecurity-magazine
 xsssql
 T00ls
 52pojie
 Mozhe
 ThreatPost
 Vulbox
 BugKu
 BuTian
 Track
 Seebug-paper
 tttang
 TryHackMe
<a href="https://www.youtube.com/c/TheHackersWorld" rel="nofollow">TheHackerWorld</a>cstis
qsnctf
 techcrunch
Programmer
 OpenSource
 infoQ
 twle
<a href="https://quizlet.com/" rel="nofollow">Quizlet</a>
Gitee
 Leetcode
 
 qyer
 Sourceforge
 Spotify
 Twitch
 Wikipedia
 osu!
 academia-edu
 anilist
 bezuzyteczna
 hubpages
 ebio-gg
 mastodon-xyz
 f3-cool
 monkeytype
 couchsurfing
 geocaching
 behance
 coinvote

 myanimelist
 rajce-net
 svidbook
 hackaday
 d3ru
 ctan
 imgur
 trashboxru
 appledeveloper
 biggerpockets
 wattpad
 envatoforum
 patreon
 authorstream
 gfycat
 airbit
 memrise
 pokemonshowdown
 weebly
 irl
 lor
 nextcloudforum
 wicgforum
 npm
 mastodon-technology
 social-tchncs
 finanzfrage
 <a href="https://slack.com/">slack</a>
 smugmug
 traktrain
 wykop
 livelib
 gunsandammo
 keakr
 needrom
 sbazar-cz
 moikrug
 hackthebox
 icq
 livejournal
 oraclecommunity
 royalcams
 swapd
 uid
 hackster
 artstation
 blogger
 coderwall
 rcloneforum
 sportlerfrage
 youtubechannel
 buzzfeed
 slideshare
 fl
 discogs
 joplinforum
 bitbucket
 giantbomb
 giphy
 hashnode
 playstore
 notabug-org
 xboxgamertag
 xvideos
 mastodon-social
 buymeacoffee
 etsy
 motorradfrage
 newgrounds
 trakt
 weblate
 dailymotion
 tradingview
 icons8community
 mixcloud
 vimeo
 myspace
 wix
 lottiefiles
 cryptomatorforum
 replit-com
 trawelling
 about-me
 caddycommunity
 eintrachtfrankfurtforum
 periscope
 sportsru
 pr0gramm
 choicecommunity
 codeforces
 ionicforum
 vero
 yandexmusic
 chaos-social
 tenor
 webnode
 akniga
 egpu
 note
 instructables
 sketchfab
 vsco
 asciinema
 lesswrong
 themeforest
 youtubeuser
 spletnik
 7cups
 alik-cz
 cnet
 bookcrossing
 warriorforum
 queer-af
 championat
 pornhub
 eintracht
 znanylekarz-pl
 getmyuni
 lobsters
 flipboard
 munzee
 3dnews
 imgup-cz
 fosstodon
 sessionize
 pinkbike
 biohacking
 chaos
 crevado
 gesundheitsfrage
 goodreads
 slides
 toster
