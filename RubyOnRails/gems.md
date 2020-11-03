# Ruby Popular GEMS use

## Gem Dotenv

<p>Dotenv est une gem qui permet de stocker des clés d'API dans un fichier qui va rester secret, car il ne sera jamais push sur GitHub.
Via la gem, ton programme pourra faire appel au contenu de ce fichier pour utiliser les clés.</p>

**usage:**

<p>Dans Gemfile ajouter le gem 'dotenv' puis mettre ".env" dans -> .gitignore 

*Attention: Lorsque l'on utilise dotenv, on doit lancer notre programme à la racine de notre programme.* </p>

------------------------------------

## Gem Twitter

**Method configuration to login:**

`def login_twitter`
 ` client = Twitter::REST::Client.new do |config|`  
   ` config.consumer_key        = ENV["TWITTER_CONSUMER_KEY"]`  
   ` config.consumer_secret     = ENV["TWITTER_CONSUMER_SECRET"]`  
   ` config.access_token        = ENV["TWITTER_ACCESS_TOKEN"]`  
   ` config.access_token_secret = ENV["TWITTER_ACCESS_TOKEN_SECRET"]`  
 ` end`  
  `return client`  
`end`  

**Tweeter quelque chose**

`client.update("quelque chose")`


------------------------------------

**Liker un tweet**

`client.favorite!`

------------------------------------

**Follow quelqu'un**

`client.follow`

------------------------------------

## Gem Colorize

<p>Gem qui permet de colorer le text lorsqu'on l'affiche sur le Terminal.   
Permet une jolie syntaxe.</p>

**.red** / **.blue**

Colore en rouge/bleu le texte

**.black.on_white**

Colore le fond en blanc et le texte en noir.


ex: 
<p align=center><img src="https://camo.githubusercontent.com/6fa26496720b5bda64100615d92b8bf00dd5e470/68747470733a2f2f692e6962622e636f2f383658326a42382f436170747572652d642d652d6372616e2d323032302d31302d31362d612d30302d31312d31392e706e67"></p>

--------------------------------------

## Gem Faker

<p>Permet de generer des valeurs afin de seed sa DB.</p>

--------------------------------------

## Gem table-print

<p>Permet de mettre sous forme de tableaux la DB au sein de la console</p>

```shell
tp User.all
```

<p>Affiche tous les utilisateurs de la base de donnée sous forme de tableau.</p>

--------------------------------------

## Gem dotenv-rails

<p>Équivalent de Dotenv pour RubyOnRails</p>

---------------------------------------

## Bcrypt

<p>Permet de crypter les mots de passe</p>