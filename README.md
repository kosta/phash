# Do you remember all your password? #

Are they all strong enough?

Are none of them shared between sites?

…and none of them stored in the cloud?

## If you'd like all of that try pHash. ##

## Here's how it works: ##

* Think of a master password. Something really hard to crack. 
  Like "Tw5s&n1gZj!".
  
* Then choose a website (or whatever) where you want to use that password. 
  Like "Google".
  
* Press "phash". You'll see a long and difficult to remember password. 
  Like "e1dadd6f21a718c8f3120dca10ac7e9f39185ecf".
  
  Use that as your password for Google.
  
* If you need a password for Amazon.com, just put it into the website (or whatever) box.
  You'll get a different password. (Like "e2458d59c2e7a7482a5f8503e53bd74b18adcc13")
  
All you need to remember is your master password. 

All your accounts will have completely different passwords. If one of them is evil,
it can't tear you down.

Nothing is stored in the cloud. It all happens in the browser. 

## Ok, so how does it work (technically)? ##

We simply concatenate the master password and the site

If you need your password but can't access it's website, simply use 
  for linux:
    echo -n 'masterpasswordsite' | sha1sum
  for mac os x:
    echo -n 'masterpasswordsite' | shasum
  for windows:
    install cygwin and run the linux command. Sorry :)
 
Of course, you need to replace "masterpasswordsite" with your master password and
site name (no space in between). Oh and don't forget to 
  history -c
  rm ~/.bash_history
afterwards. (Non-bash users: You probably know what to do. If not, ask Google)