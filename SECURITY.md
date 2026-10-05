# Politique de securite

## Signaler une vulnerabilite

Ne pas ouvrir d'issue publique pour une faille de securite.

- Repos prives : contacter directement un maintainer de l'organisation.
- Repos publics : utiliser l'onglet "Security" > "Report a vulnerability"
  (Private Vulnerability Reporting) quand il est disponible.

Nous accusons reception sous 72 h et visons un correctif ou un plan
d'action sous 14 jours selon la severite.

## Perimetre couvert

Tous les depots de l'organisation. Chaque depot est equipe de :

- Dependabot alerts + security updates (correctifs automatiques en PR)
- dependabot.yml pour les mises a jour hebdomadaires
- Workflow "Security Scan" : Gitleaks (secrets) + ClamAV (antivirus)
- Workflow "Quality" : code smell (Biome/Ruff), couverture, audit de deps

## Regles

- Jamais de secret dans le code : variables d'environnement ou GitHub
  Secrets uniquement. Gitleaks bloque les commits contenant des secrets.
- Pas d'endpoint/API key en clair dans les issues ou PRs.
