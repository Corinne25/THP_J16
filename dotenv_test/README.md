gem install rspec


Small exercices in Ruby -- RSpec 3 Edition
==========

### Set up instructions

1. `$ rspec --init`
2. `$ gem list`
3. `gem install bundler`
4. $ touch Gemfile
    source "https://rubygems.org"
    ruby "2.7.4"
    gem 'rspec'
    gem 'pry'
    gem 'rubocop'
    gem 'pry'
    gem 'dotenv'
5. `$ bundle install`

### dans le fichier spec
1. require 'nom_de_la_gem'  : ../lib/
2. require 'pry'

### dans le fichier spec
1. require 'nom_de_la_gem'  : ../lib/
2. require 'pry'


mon_projet
├── lib
│   └── app.rb
├── spec
│   ├── spec_helper.rb
│   └── app_spec.rb
├── README.md
├── Gemfile
├── Gemfile.lock
└── .rspec

# le reste de ton programme…
Et voilà, tu auras juste à insérer binding.pry pour que le REPL s'exécute à cet endroit du code. C'est comme si IRB se lançait au milieu de l'exécution de ton code et que du coup, tu pouvais interagir avec les variables et méthodes dans leur état actuel (connaître leurs valeurs, faire des tests avec, modifier leurs valeurs, etc.). Par exemple, en exécutant le code suivant :
require 'pry'

def multiply_by_6(var) #définition d'une méthode multipliant par 6 en 2 étapes
var = var * 2
binding.pry # On lance PRY au milieu de la méthode
var = var * 3
return var
end

multiply_by_6(5) # j'exécute la méthode sur la valeur 5
On lance le programme et PRY s'exécute sous la forme d'une fenêtre type IRB. Si on veut afficher la valeur de var, on obtient => 10, la valeur de (5 x 2).
Pour sortir de l'interface de PRY, tape tout simplement exit

4. Points importants à retenir
Pour débugger : 1) lis les messages 2) cherche sur Google 3) mets des puts / utilise PRY 4) appelle un ami.
PRY permet de lancer une sorte d'IRB en plein milieu d'un programme Ruby. Cette interface permet de faire une pause dans l'exécution du programme et de tester la valeur de toutes les variables ou méthodes que l'on souhaite. C'est un outil extrêmement puissant pour débugger un programme et interagir avec.
Pour utiliser PRY, il faut ajouter gem 'pry' dans son Gemfile, require 'pry' en haut de ton programme concerné, puis binding.pry pour exécuter PRY dans ton code.
5. Pour aller plus loin
Tu peux aller sur le site de PRY, ou tu peux aller jeter un œil sur la documentation de PRY sur GitHub.