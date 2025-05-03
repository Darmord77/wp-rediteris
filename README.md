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


Detect
Hunt down social media accounts by username, email or phone across social networks

Usage:
  DetectDee detect 

Flags:
  -c, --check           self-check
  -e, --email strings   
  -f, --file string     Site data file (default "data.json")
  -g, --google          Show google search result
  -h, --help            help for detect
  -n, --name strings    name[s], e.g. piaolin,poq79,SomeOneYouLike
      --nsfw            Include checking of NSFW sites from default list.
  -o, --output string   Result file (default "result.txt")
  -p, --phone strings   phone[s], e.g. 15725753684,13575558962
      --precisely       Check precisely
      --proxy string    Make requests over a proxy. e.g. so5://127.0.0.1:1080
  -r, --retry int       Retry times after request failed (default 3)
  -s, --site strings    Limit analysis to just the listed sites. Add multiple options to specify more than one site.
  -t, --timeout int     Time (in seconds) to wait for response to requests (default 10)
      --token string    chatgpt api token

Global Flags:
  -v, --verbose   verbose output

Please update the data for the first time

./DetectDee update
To search for only one user:

./DetectDee detect -n piaolin
To search for more than one user:

./DetectDee detect -n piaolin,blue
To search for more than one user and use ChatGPT for user tagging of results(need ChatGPT token):

./DetectDee detect -n piaolin,blue --token {ChatGPT Token}
To search for email: . x

./DetectDee detect.. 
To search for phone: ..xxx

./DetectDee detect -p 
Show google search(please check yourself):

./DetectDee detect -n piaolin,blue -g
To search in specified site:

./DetectDee detect -n piaolin -s github,v2ex
Screenshot
The screenshot function is used to screenshot the results of detect. Note that this function requires:

Chrome
A period of time
A bit of memory usage
Usage:                                                                         
  DetectDee screenshot [flags]                                                 
                                                                               
Flags:                                                                         
      --chrome         Show chrome                                             
  -d, --dir string     Folder path of the screenshot (default "screenshots")   
  -f, --file string    Url list file (default "result.txt")                    
  -h, --help           help for screenshot                                     
      --path string    Chrome ExecPath                                         
      --proxy string   Make requests over a proxy. e.g. socks5://127.0.0.1:1080
  -t, --thread int     Chrome number (default 3)                               
      --timeout int    Timeout (default 60)                                    
                                                                               
Global Flags:                                                                  
  -v, --verbose   verbose output
Screenshot the results of detect

./DetectDee screenshot
result.jpg screen.jpg

Contributing
We would love to have you help us with the development of DetectDee. Each and every contribution is greatly valued!

Here are some things we would appreciate your help on:

Addition of new site support, You can notify me that a site has an interface available, or you can write JSON directly
Bringing back site support of sites that have been removed in the past due to false positives
Todo
Credential Stuffing for result
More site
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
 aqniu
cstis
qsnctf
 techcrunch
Programmer
 OpenSource
 infoQ
 twle
 Quizlet
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
 slack
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
