# wp-rediteris
Snažíme sa zaprocovať na novom plugine pre Slovensku Wordpress komunity


*Disclaimer: This article and this tool are for technical discussion and sharing only. Illegal use is strictly prohibited.

DetectDee: Hunt down social media accounts by username, email or phone across social networks example.gif screen.jpg

Feat
Includes sites frequently used by CyberSecurity practitioners
Hunt down social media accounts by username, email or phone
Precise thread control and custom request headers are used to prevent WAF recognition
Extensible, simple, and easy-to-use template
Integration of mobile versions of social networking sites
Install

cd DetectDee
go mod tidy
go run .
Usage
English

中文文档

Detect
Hunt down social media accounts by username, email or phone across social networks

Usage:
  DetectDee detect [flags]

Flags:
  -c, --check           self-check
  -e, --email strings   email[s], e.g. mail@gmail.com,45715485@qq.com
  -f, --file string     Site data file (default "data.json")
  -g, --google          Show google search result
  -h, --help            help for detect
  -n, --name strings    name[s], e.g. piaolin,poq79,SomeOneYouLike
      --nsfw            Include checking of NSFW sites from default list.
  -o, --output string   Result file (default "result.txt")
  -p, --phone strings   phone[s], e.g. 15725753684,13575558962
      --precisely       Check precisely
      --proxy string    Make requests over a proxy. e.g. socks5://127.0.0.1:1080
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
To search for email:

./DetectDee detect -e mail@gmail.com,test@163.com
To search for phone:

./DetectDee detect -p 15822575984,13188524682
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
