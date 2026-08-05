## init

Cette commande crée un fichier Vagrantfile dans le répertoire courant.

Par exemple :

```bash
mkdir mon_projet
cd mon_projet

vagrant init
```

Tu obtiendras :

```
mon_projet/
└── Vagrantfile
```

Ce fichier contient un modèle de configuration que tu pourras modifier.

Que se passe-t-il en interne ?

Lorsque tu exécutes :

```bash
vagrant init
```

Vagrant :

1. vérifie que le dossier ne contient pas déjà un Vagrantfile ;
2. crée un nouveau fichier Vagrantfile avec des commentaires et des exemples ;
3. n'installe aucune machine virtuelle ;
4. ne télécharge aucune box ;
5. ne démarre rien.

Autrement dit :

vagrant init prépare uniquement le projet.

## up
