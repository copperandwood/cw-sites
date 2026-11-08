# cw-sites

Sites web de l'Ensemble Copper & Wood : copperandwood.com, www.copperandwood.com, copperandwood.fr et www.copperandwood.fr.

## Ce que fait ce dépôt aujourd'hui

Le fichier `.htaccess` redirige toutes les adresses des quatre domaines vers la billetterie HelloAsso du concert. C'est le lien imprimé sur l'affiche.

Une seule exception : la page `confidentialite.html` (aussi accessible par `/confidentialite`), la politique de confidentialité de l'association. Meta l'exige pour l'application « Dizzy Copper & Wood » qui gère la Page Facebook, le compte Instagram et les publicités. Ne pas la supprimer tant que cette application existe.

La redirection est temporaire (302) : les navigateurs ne la gardent pas en cache, ce qui permet de changer la cible à chaque concert. Le chemin demandé n'est pas ajouté : copperandwood.com/n-importe-quoi mène aussi à la billetterie.

La racine du dépôt est la racine web : le jour où l'association aura un vrai site de présentation, ses fichiers viendront ici.

## Déploiement

Le dépôt est relié aux hébergements OVH de l'association par l'intégration Git d'OVH (onglet « Mes sites » de l'hébergement, « Associer Git »). Un webhook GitHub prévient OVH à chaque mise à jour de `main`, qui est alors déployée automatiquement.

Si un déploiement ne part pas, lire les livraisons du webhook (Settings > Webhooks > Recent deliveries). Le 8 novembre 2026, OVH a répondu « 401 Unauthorized » aux pushes qui ajoutaient un fichier, et accepté ceux qui ne faisaient que modifier des fichiers existants. Une fusion qui modifie seulement un fichier existant fait alors repartir le déploiement de tout le dépôt.

## Changer la cible de la redirection

1. Modifier l'URL dans `.htaccess` sur une branche et ouvrir une pull request.
2. Fusionner la pull request dans `main` (Guillaume).
3. Vérifier en ligne les quatre adresses, en http et en https, et la page `/confidentialite.html`.

Personne n'a besoin du mot de passe FTP.
