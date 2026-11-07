# cw-sites

Sites web de l'Ensemble Copper & Wood : copperandwood.com, www.copperandwood.com, copperandwood.fr et www.copperandwood.fr.

## Ce que fait ce dépôt aujourd'hui

Le fichier `.htaccess` redirige les quatre adresses vers la billetterie HelloAsso du concert. C'est le lien imprimé sur l'affiche.

La racine du dépôt est la racine web : le jour où l'association aura un vrai site de présentation, ses fichiers viendront ici.

## Déploiement

Le dépôt est relié aux hébergements OVH de l'association par l'intégration Git d'OVH (onglet « Mes sites » de l'hébergement, « Associer Git »). Un webhook GitHub prévient OVH à chaque mise à jour de `main`, qui est alors déployée automatiquement.

## Changer la cible de la redirection

1. Modifier l'URL dans `.htaccess` sur une branche et ouvrir une pull request.
2. Fusionner la pull request dans `main` (Guillaume).
3. Vérifier en ligne les quatre adresses, en http et en https.

Personne n'a besoin du mot de passe FTP.
