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

`def login_twitter
  client = Twitter::REST::Client.new do |config|
    config.consumer_key        = ENV["TWITTER_CONSUMER_KEY"]
    config.consumer_secret     = ENV["TWITTER_CONSUMER_SECRET"]
    config.access_token        = ENV["TWITTER_ACCESS_TOKEN"]
    config.access_token_secret = ENV["TWITTER_ACCESS_TOKEN_SECRET"]
  end
  return client
end`
------------------------------------

