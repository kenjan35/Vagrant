## C'est quoi un Vagrantfile ?

Un Vagrantfile est un fichier écrit en Ruby (mais tu n'as pas besoin de connaître Ruby) qui décrit une machine virtuelle.

Au lieu de créer une VM à la main dans VirtualBox :
* choisir Ubuntu
* donner 2 Go de RAM
* ajouter un réseau privé
* partager un dossier
* installer nginx

tu écris simplement un fichier :

```ruby
Vagrant.configure("2") do |config|

end
```

Puis tu lances :

```bash
vagrant up
```

et tout est créé automatiquement.

