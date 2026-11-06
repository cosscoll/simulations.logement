# Simulateur SASU / SAS : paramètres et règles de calcul 2026

Mise à jour : 6 novembre 2026 — **Projection française indicative, pas une liquidation fiscale officielle**.

Le simulateur calcule les charges à partir du CA HT mensuel, suppose un exercice de 12 mois et permet de conserver plusieurs simulations. Les coûts sont répartis selon **obligation légale**, **obligation conditionnelle** ou **choix commercial facultatif**. Tout montant estimé reste remplaçable par une valeur réelle.

## 1. Paramètres et coûts de fonctionnement

| Situation choisie | Coût retenu | Nature | Condition et limite |
| --- | --- | --- | --- |
| Banque avec offre sans frais | 0 €/mois | Commercial, non garanti | Le **dépôt du capital** est toujours obligatoire à la création |
| Banque économique | 9 €/mois | Estimation de marché | Dépend de l'offre contractuelle |
| Banque traditionnelle | 22 €/mois | Estimation de marché | Dépend de l'offre contractuelle |
| Banque personnalisée | Montant saisi | Réel si devis | Remplace la provision |
| Comptabilité gérée soi-même | 0 € d'expert-comptable | Prestation facultative | **Tenir les comptes, établir les comptes annuels et les déposer restent obligatoires** |
| Logiciel comptable | 18 €/mois | Estimation de marché | Coût non obligatoire si gestion autonome sans abonnement |
| Expert-comptable externe | 95 €/mois | Estimation de marché | Jamais imposé comme prestataire par défaut |
| Domiciliation au domicile du dirigeant | 0 €/mois de coût dédié | Hypothèse | Sous réserve de pouvoir y domicilier la société |
| Entreprise de domiciliation | 25 €/mois | Estimation contractuelle | Si choisie |
| Coworking | 120 €/mois | Estimation contractuelle | Si choisi |
| Local loué | 350 €/mois + 25 €/mois d'assurance | Hypothèse et obligation conditionnelle | Ne pas compter le même loyer deux fois dans les charges |
| RC professionnelle volontaire | 18 €/mois | Estimation | Peut être facultative pour certains services numériques |
| Activité réglementée | 55 €/mois | Provision indicative | **Assurance parfois obligatoire ; devis à obtenir** |
| BTP / garantie décennale | 140 €/mois | Provision très indicative | Garanties et primes variables : faire vérifier le contrat |
| Véhicule possédé ou loué par la société | 55 €/mois par véhicule | Obligation d'assurance, coût estimé | À ajuster avec un devis |
| Salariés | Salaire brut + 40 % de cotisations patronales + 30 € de mutuelle par salarié/mois | Estimation de paie | Déclarations DSN, mutuelle et conventions à valider |
| Président rémunéré | Brut estimé à partir du net + cotisations patronales estimées | Estimation de paie | Président non rémunéré : **0 €** sur son mandat |
| Rémunérations soumises à taxe d'apprentissage | 0,68 % du brut / 0,44 % en Alsace-Moselle | Réglementaire avec exceptions | Les exonérations liées aux apprentis ne sont pas entièrement modélisées |
| Dépôt annuel des comptes existants | 44,14 €/an | Obligation de dépôt, tarif de référence par correspondance | Paiement réel peut différer selon canal |
| SASU constituée en 2026 | 0 € de dépôt annuel compté sur 2026 | Temporalité | Premier dépôt généralement après clôture, référence 44,14 € pour exercice suivant |
| Dépôt du capital lors création | 0 € frais prestataire ou 35 € de provision, modifiable | Capital obligatoire, frais du service variables | Le **capital lui-même n'est pas une dépense** |
| Assistance rédaction statuts / formalités | 0 € par défaut, montant personnalisé | Facultatif | Pas de prestation imposée |

Les postes de banque, comptabilité et assurance ne sont **plus cumulés par défaut en forfait de 105 €**. Les menus sélectionnent un profil cohérent et le mode « personnalisé » permet de saisir tes tarifs. Les services sont traités comme des montants hors TVA à préciser lorsque nécessaire ; en franchise, la TVA non récupérable sur certaines prestations est incluse dans les charges.

## 2. Taxes et prélèvements

- **IS** : résultat annuel imposable × 25 %, ou 15 % sur les 42 500 premiers euros si capital entièrement libéré, au moins 75 % détenus par des personnes physiques et CA annuel ≤ 10 M€ ; 25 % au-delà.
- **Contribution additionnelle IS** : 3,3 % sur l'IS dépassant 763 000 € si absence d'exonération PME ; à valider.
- **TVA** : franchise/option/réel, CA N−1, seuil de franchissement de l'année, avec moyenne annualisée et approximation du premier mois taxable. TVA collectée et déductible **hors résultat HT**.
- **CFE** : année de création exonérée ; autres années selon CA historique, base minimum et taux communal. Les simulations par défaut utilisent une fourchette et un taux communal supposé ; l'avis réel prévaut.
- **Taxe sur les salaires** : conditionnelle, selon TVA et CA historique, assiette simplifiée.
- **Taxe d'apprentissage** : calculée sur les rémunérations brutes soumises si présentes, avec taux régional, et avertissement pour exonérations apprenti.
- **CVAE** : au-delà de 500 000 € de CA, taux progressif 2026 appliqué à la valeur ajoutée fiscale. Si celle-ci n'est pas renseignée, la valeur ajoutée est **approchée** depuis le CA et les charges externes. Dégrèvement et taxe additionnelle CCI indicatifs. Déclaration éventuelle si CA > 152 500 €.
- **Réserve légale et dividendes** : calcul de provision annuelle à partir du capital et éventuel PFU sur hypothèse de distribution ; ne sont jamais ajoutés automatiquement au revenu personnel.

## 3. Cas concrets

### SASU numérique nouvellement créée, sans rémunération et sans prestataires externes

CA HT moyen = **3 000 €/mois** ; 0 € d'autres charges ; banque économique 9 €/mois ; comptabilité autonome ; activité numérique ; siège au domicile ; aucun véhicule ; aucun salarié ; franchise TVA ; capital non confirmé intégralement libéré.

- CA HT annuel : **36 000 €**.
- Banque : **108 €/an**.
- Frais de création obligatoires incluant annonce légale + TVA non récupérable : **223,56 €**.
- CFE, charges salariales du président, taxe d'apprentissage, CVAE, dépôt des comptes courant 2026 : **0 € dans ce scénario**.
- Résultat taxable annuel : 36 000 − 108 − 223,56 = **35 668,44 €**.
- IS à 25 % : **8 917,11 €**.
- **Résultat après IS : 26 751,33 €/an**, soit **2 229,28 €/mois** en équivalent ; il reste **dans la SASU**.

Si l'éligibilité au taux réduit d'IS est confirmée, IS à 15 % = **5 350,27 €**, après IS **30 318,17 €/an**. Si la SASU choisit un expert-comptable, un bureau, une assurance ou verse un salaire, le résultat baisse et les calculs s'actualisent.

### SASU avec 2 salariés

Avec 2 salariés à 2 000 € de brut chacun, les estimations de coûts sont : **4 000 € de salaire brut + 1 600 € de charges patronales + 60 € de mutuelle/mois**, hors autres charges et exonérations éventuelles. Taxe d'apprentissage estimée : **326,40 €/an** à 0,68 % (hors autres rémunérations et cas d'exonération).

## 4. Limites importantes

Les frais de prestataires (banques, outils, assurances, locaux, paie) sont des provisions de marché **inventoriées comme telles**, jamais des tarifs légaux. Les cotisations de paie exactes ne peuvent pas être calculées avec le seul net souhaité sans les détails DSN. Une garantie décennale a des tarifs très variables. La CFE ne peut pas être déterminée exactement sans la commune, le local et l'avis. La CVAE est imprécise sans la vraie valeur ajoutée fiscale. La TVA peut être affectée par le jour réel de dépassement du seuil, les taux multiples, les factures, les exemptions et les régimes spéciaux. Le résultat annuel constant ne constitue pas un bilan comptable ni un solde de trésorerie de banque.

## 5. Sources officielles (vérification novembre 2026)

- [Coûts de création](https://entreprendre.service-public.gouv.fr/vosdroits/F37688) ; [annonces légales 2026](https://entreprendre.service-public.gouv.fr/vosdroits/F31972)
- [Dépôt du capital](https://entreprendre.service-public.gouv.fr/vosdroits/F32333)
- [Dépôt annuel des comptes](https://entreprendre.service-public.gouv.fr/vosdroits/F31214) ; [tarifs Infogreffe](https://www.infogreffe.fr/tarifs-formalites) ; [tarifs INPI](https://formalites.entreprises.gouv.fr/tarifs.php)
- [Assurances obligatoires selon activité](https://entreprendre.service-public.gouv.fr/vosdroits/F37365)
- [Taxe d'apprentissage](https://entreprendre.service-public.gouv.fr/vosdroits/F22574)
- [Cotisation CFE et base minimum 2026](https://entreprendre.service-public.gouv.fr/vosdroits/F23547)
- [CVAE et taux 2026](https://entreprendre.service-public.gouv.fr/vosdroits/F23546)
- [Fiscalité de l'IS](https://entreprendre.service-public.gouv.fr/vosdroits/F23575)
- [TVA et franchise](https://entreprendre.service-public.gouv.fr/vosdroits/F21746)
- [Simulation paie SASU Urssaf](https://mon-entreprise.urssaf.fr/simulateurs/sasu)
