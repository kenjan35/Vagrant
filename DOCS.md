## C'est quoi un Vagrantfile ?

Un Vagrantfile est un fichier écrit en Ruby qui décrit une machine virtuelle.

Au lieu de créer une VM à la main dans VirtualBox :
* choisir Ubuntu
* donner 2 Go de RAM
* ajouter un réseau privé
* partager un dossier
* installer nginx

On écrit simplement un fichier :

```ruby
Vagrant.configure("2") do |config|

end
```

Puis on lance :

```bash
vagrant up
```

et tout est créé automatiquement.

## Structure d'un Vagrantfile

Voici le plus petit Vagrantfile possible :

```ruby
Vagrant.configure("2") do |config|
    config.vm.box = "ubuntu/jammy64"
end
```

Regardons chaque ligne.

#### 1. Vagrant.configure("2")

```ruby
Vagrant.configure("2") do |config|
```

Cela signifie :

"Je vais utiliser la version 2 du format de configuration."

Le mot config est simplement une variable.

On pourrait écrire :

```ruby
Vagrant.configure("2") do |machine|
```

ou

```ruby
Vagrant.configure("2") do |banana|
```

mais tout le monde utilise :

```ruby
config
```

#### 2. config.vm.box

```ruby
config.vm.box = "ubuntu/jammy64"
```

Une **box** est une image de machine virtuelle.

Comme Docker possède :

* ubuntu
* alpine
* debian

Vagrant possède :

* ubuntu/jammy64
* debian/bookworm64
* generic/alpine319

Lorsqu'on fait :

```bash
vagrant up
```

Vagrant télécharge automatiquement cette box si elle n'est pas déjà présente.

Le bloc se termine

```ruby
end
```

Il ferme le bloc commencé par :

```ruby
do
```

## Ajouter un nom

On peut écrire :

```ruby
Vagrant.configure("2") do |config|

    config.vm.box = "ubuntu/jammy64"
    config.vm.hostname = "serveur-web"

end
```

Une fois connecté :

```ruby
hostname
```

on obtiendra :

```ruby
serveur-web
```