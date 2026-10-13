# Convertisseur de devises

## 1. Besoin

Permettre à l’utilisateur de convertir un montant d’une devise vers une autre.

## 2. Règles appliquées

- L’utilisateur saisit un montant positif ou nul et choisit une devise de départ et une devise d’arrivée.
- La virgule ou le point peuvent servir de séparateur décimal ; les espaces peuvent séparer les milliers.
- Les devises sont chargées depuis l’API Frankfurter.
- Le taux de change est récupéré au moment de la conversion. Sa date et sa valeur sont affichées avec le résultat. Les taux sont actualisés quotidiennement par le service.
- Si les devises sont identiques, le montant reste inchangé et aucun taux n’est demandé.
- Le résultat est arrondi et affiché avec deux décimales.
- Si la saisie est invalide ou si le taux est indisponible, un message d’erreur est affiché et aucun résultat de conversion n’est présenté.

## 3. Exemples

- **Conversion :** avec un taux d’exemple de 1 EUR = 1,08 USD, 100 EUR donnent 108,00 USD. Le taux réel affiché par l’application peut différer.
- **Même devise :** 25 EUR convertis en EUR donnent 25,00 EUR.
- **Saisie invalide :** la saisie « abc » affiche un message demandant un montant valide.
- **Taux indisponible :** l’application indique que la conversion est impossible et invite à réessayer plus tard.

## Questions précisées

- **Quelles devises proposer ?** Toutes les devises proposées par le service de taux.
- **Quelle source utiliser ?** L’API Frankfurter, sans clé API.
- **À quelle fréquence les taux sont-ils actualisés ?** Quotidiennement selon le service.
- **Afficher la date du taux ?** Oui, avec le résultat de la conversion.
- **Combien de décimales afficher ?** Deux, avec l’arrondi usuel.
- **Les montants négatifs sont-ils autorisés ?** Non ; zéro est accepté.
- **Que faire si le taux est indisponible ?** Afficher une erreur plutôt qu’un résultat trompeur.
- **Quels formats de saisie accepter ?** Accepter virgule ou point comme séparateur décimal et des espaces pour grouper les milliers.

## Utilisation

Ouvrir [`index.html`](./index.html) dans un navigateur. Une connexion Internet est nécessaire pour charger la liste des devises et les taux de change.
