# Parution dans l'application finale (stable)

## Les branches

Papillon a plusieurs branches sur son repo :

- `stable` est la branche à laquelle le public a accès via les stores.
- `beta` est la branche de test où les nouvelles fonctionnalités sont testées avant d'être publiées dans la branche stable.
- `development` est la branche de développement où les nouvelles fonctionnalités sont ajoutées et les bugs sont corrigés.

## Processus de publication

Lorsqu'une nouvelle fonctionnalité est prête à être publiée, elle est fusionnée dans la branche de développement.

Les nouvelles publications sont gérées par l'équipe de coordination. Lorsqu'une nouvelle publication est prête, elle est soumise à une demande de fusion dans la branche bêta. GitHub Actions est utilisé pour automatiser le processus de publication ainsi que pour la publier sur les stores de test. Une fois que la publication est testée et prête à être publiée, elle est fusionnée dans la branche stable. GitHub Actions est utilisé pour automatiser le processus de publication ainsi que pour la publier sur les stores.

<center>

```mermaid
graph TD
    A(Développement) -->|Test par les devs| B(Bêta)
    B -->|Publié sur les stores de test| ST(Testflight, Google Play Beta)
    ST -->|Test par le public| C(Stable)
    C -->|Publié sur les stores| S(App Store, Google Play)
    S -->|Téléchargé par le public| U(Utilisateurs finaux)
```
</center>
