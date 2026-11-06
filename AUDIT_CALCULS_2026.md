# Audit des calculs — Simulations logement, micro-entreprise et SAS / SASU

**Date du contrôle : 6 novembre 2026**  
**Périmètre :** `index.html`, simulations budgétaires, micro-entreprise, aides, SAS/SASU, export et reprise des scénarios.

## Conclusion

Le site **n'est pas** un simulateur CAF officiel, un logiciel de paie ou une comptabilité fiscale.
La cohérence de certains calculs a été vérifiée, et des erreurs matérielles ont été corrigées.
Les résultats restent dépendants de données renseignées et de conventions de calcul.
**Ne pas utiliser les montants pour une déclaration URSSAF, une liasse fiscale, un calcul de droits CAF ou un arbitrage bancaire sans vérification.**

## Corrections de priorité critique appliquées

1. **Aides sociales autrefois présumées** : l'ancien site ajoutait sans justification une APL déduite d'une formule arbitraire, une prime d'activité mensuelle simplifiée et 100 € de MOBILI-JEUNE. Ces montants ne sont plus comptés automatiquement. Le montant **confirmé** par la CAF ou Action Logement est maintenant saisi explicitement ; 0 € dans l'entrée signifie « non saisi », pas absence de droit.
2. **Prime d'activité** : les bornes de bonification d'avril 2026 sont corrigées (709,18 € à 1 658,76 € avec maximum 240,63 €). La formule encore affichée à titre **d'illustration** ne peut pas établir de droits car le site ne connaît pas les ressources des 3 mois de référence, tous les revenus du foyer, le montant net social de chaque fiche de paie, l'ouverture des droits ou les conditions propres au statut étudiant. Elle est exclue du budget.
3. **Micro-entreprise / ACRE** : ne présume plus que l'ACRE est accordée. Les cotisations 2026 sont calculées par activité et la CFP est ajoutée séparément, sans l'exonérer. Les charges BNC et BIC varient selon le type d'activité. Il faut choisir une ACRE réduite seulement si elle a été accordée et est toujours applicable.
4. **Impôt IR du micro-entrepreneur** : la fausse règle « impôt 0 % en dessous de 17 438 € » est supprimée. L'impôt au barème dépend du foyer fiscal et de l'ensemble des revenus. L'utilisateur saisit une **provision** ; les taux de versement libératoire ne s'appliquent que si les conditions d'option sont remplies.
5. **Frais réels micro** : les dépenses d'exploitation réelles sont déduites de la trésorerie disponible, sans réduire artificiellement les cotisations forfaitaires. Un déficit de trésorerie n'est pas ramené à 0.
6. **Taxe sur les salaires** : les taux marginaux progressifs étaient auparavant appliqués de manière excessive ; le calcul est corrigé. L'exonération si le CA de N-1 est dans le seuil de franchise est vérifiée si les éléments nécessaires sont présents. Si l'assujettissement est incertain, l'outil prévient.
7. **Diagramme de flux** : les frais professionnels micro sont désormais explicitement représentés. Un reste à vivre négatif devient un **besoin de financement** visible, pas une fausse recette.

## Règles et périmètres vérifiés

| Poste | Règle 2026 | Traitement actuel | Fiabilité |
|---|---|---|---|
| BNC non réglementée | Social 25,6 % + CFP libérale 0,2 % | Calcul conditionnel, ACRE si sélectionnée | Bonne si activité, droit ACRE et CA corrects |
| BIC service | Social 21,2 % + CFP 0,1 % commercial ou 0,3 % artisanal | Calcul conditionnel | Bonne si classification correcte |
| ACRE après 01/07/2026 | 25 % de réduction des cotisations sociales, pas de la CFP | Option désactivée par défaut | Bon taux ; dates et accord à vérifier |
| VFL | 1,7 % BIC services ; 2,2 % BNC | Appliqué seulement si option choisie | Bonne formule, éligibilité non vérifiée |
| IR au barème | Barème progressif et quotient familial | Montant de provision saisi manuellement | **Non calculé** |
| Prime d'activité | Calcul sur période de référence, ressources du foyer et bonification | Montant confirmé saisi ; estimation hors budget | **Droit non calculé** |
| APL/ALS/ALF | Ressources N-12, logement, foyer, zone et autres données | Montant confirmé saisi | **Droit non calculé** |
| MOBILI-JEUNE | Aide 10 à 100 €/mois, loyer après aide logement, période couverte | Montant saisi limité à 100 € et au reste du loyer ; 0 hors alternance | Conditions d'attribution non simulées |
| Président SAS/SASU non rémunéré | Pas de cotisations sur un salaire nul | Coût salaire nul | Correct en régime général dans ce périmètre |
| Président SAS/SASU rémunéré | Charges déterminées par la paie, situation et exonérations | **Estimation seulement** : 22 % salariales et 35 % patronales du brut | **Non exact** |
| IS | Taux 25 % ; 15 % jusqu'à 42 500 € sous conditions (capital, détention, CA) | Calcul annualisé sans déficit reporté | Bonne formule sous hypothèses |
| CFE | Création exonérée la première année ; autres règles selon N-2 et commune | Exonérations simples et provision/avis saisi | Montant local **non calculé** |
| TVA franchise | Services 37 500/41 250 € ; commerce 85 000/93 500 € | Seuils pour activités usuelles, calcul projeté du net TVA | Date de franchissement et activités spéciales non calculées |
| Formalités SASU / SAS | 33,83 € RCS ; 19,33 € bénéficiaires ; annonces 142/199 € HT en métropole | Coûts de base en une seule fois | Frais annexes non couverts |
| Réserve légale | Dotation 5 % jusqu'à 10 % du capital | Calcul si capital renseigné | Correct sous hypothèses |
| Dividendes | PFU 31,4 % en 2026, ou choix du barème | Projection PFU et distribution hypothétique | Pas une distribution réelle |
| CVAE | Déclarations dès 152 500 € ; assujettissement potentiel dès 500 000 € | Montant **estimé** à partir de la VA fiscale saisie ou, à défaut, d'une approximation CA - charges | **Non exact** sans VA de comptabilité et vérification d'exonérations |

## Exemples mathématiques de contrôle

- **BNC, 1 000 € de CA, sans ACRE ni impôt saisi** : 256 € sociaux + 2 € CFP = **258 €**, solde avant autres frais **742 €**.
- **BNC, 1 000 € de CA, ACRE de juillet 2026 accordée** : (25,6 % × 75 % + 0,2 %) × 1 000 € = **194 €**, solde avant autres frais **806 €**.
- **BIC services commerciaux, 1 000 € de CA, sans ACRE** : (21,2 % + 0,1 %) × 1 000 € = **213 €** ; en artisanat CFP 0,3 % = **215 €**.
- **SASU sans salaire** : coût de paie du président **0 €**, CFE **0 €** si société créée en 2026, sous réserve des éventuels coûts contractuels ou professionnels.
- **IS sur 50 000 € de bénéfice imposable, conditions du taux réduit réunies** : 42 500 × 15 % + 7 500 × 25 % = **8 250 €** ; taux normal uniquement = **12 500 €**.
- **Taxe sur les salaires** : montant brut de base × 4,25 %, puis suppléments de 4,25 % et 9,35 % dans les tranches supérieures ; décote et exonérations conditionnelles. Attention : barème publié pour les salaires 2025 imposés en 2026, et non garantie de paie 2026.

## Actualisation : réintégration des aides dans les recettes (6 novembre 2026)

Après retour utilisateur, le calcul offre maintenant **trois modes** :
1. **Projection avec aides estimées (par défaut)** : la prime d'activité est estimée par une formule simplifiée, une APL/ALS **hypothétique de 180 €/mois** est préremplie et modifiable, et MOBILI-JEUNE **potentielle jusqu'à 100 €/mois** si alternant et si le loyer net des aides le permet. **Aucun de ces montants ne constitue un droit confirmé**. Ces hypothèses sont clairement visibles dans les recettes, le reste à vivre, le diagramme et les exports.
2. **Aides réellement accordées** : les trois montants sont saisis à partir des notifications CAF et Action Logement, et seuls ces montants sont intégrés.
3. **Sans aide** : les montants sont exclus, ce qui permet de mesurer la capacité financière sans prestations.

**Important :** 180 € d'APL est une **hypothèse arbitraire de budget** destinée à préserver un scénario comparable à la version initiale, et non une simulation réglementaire. La prime calculée est une illustration qui ne connaît pas l'historique trimestriel complet, le montant net social, tous les revenus du foyer ni les conditions personnelles d'éligibilité. MOBILI-JEUNE peut être versée sur 11 mensualités au plus par année de formation, après accord et justificatifs ; une moyenne mensuelle projetée ne signifie pas versement mensuel garanti.

L'ancien état enregistré est migré : une simulation comportant au moins une aide accordée positive sélectionne le mode « Montants accordés » afin de préserver les valeurs saisies ; un scénario sans aide renseignée retrouve la projection. Les champs sont sauvegardés par simulation et restaurés après changement.

Sources : [CAF prime d'activité 2026](https://www.caf.fr/allocataires/actualites/actualites-nationales/les-reponses-vos-questions-sur-l-evolution-de-la-prime-d-activite-en-2026) · [CAF simulation aide au logement](https://www.service-public.gouv.fr/particuliers/vosdroits/R2972) · [Action Logement MOBILI-JEUNE](https://www.actionlogement.fr/l-aide-mobili-jeune).

## Actualisation : frais de fonctionnement et obligations SASU (6 novembre 2026)

La version du simulateur précise désormais :
- **Banque :** dépôt du capital obligatoire lors de la création, abonnement commercial à 0/9/22 €/mois selon le profil retenu ou montant réel personnalisé. Les tarifs sont des **hypothèses**.
- **Comptabilité :** tenue comptable, établissement et dépôt des comptes obligatoires, expert-comptable **facultatif**. Choix autonome (0 € de prestation), logiciel (18 €/mois), expert (95 €/mois) ou valeur réelle.
- **Dépôt des comptes :** 44,14 € pris comme **tarif de référence par correspondance en 2026**, avec une première échéance habituellement après la clôture du premier exercice. Le canal et la date réels priment.
- **Assurances :** RC activité selon profession, assurance local loué/véhicule conditionnelle, mutuelle salariés selon situation ; montants de référence à remplacer par devis.
- **Frais de création facultatifs :** frais de service de dépôt de capital et formalités assistées, distingués de l'apport en capital, **qui n'est pas une charge déductible**.
- **Paie :** salariés éventuels, charges patronales et mutuelle estimatives ; taxe d'apprentissage ajoutée à 0,68 % (ou 0,44 % en Alsace-Moselle), sous réserve d'exonérations et de la DSN.
- **CVAE :** calcul indicatif via le barème 2026 avec valeur ajoutée fiscale saisie ou estimée. Le CA seul ne suffit pas à déterminer exactement cette taxe.
- **TVA des prestataires :** TVA sur comptabilité et domiciliation supposée à 20 % ; TVA non récupérable traitée en charge pendant la franchise et récupérée pendant les mois imposables lorsque la dépense est éligible.

Ces améliorations n'apportent **aucune certification fiscale** ; les hypothèses de tarif bancaire, local, expert-comptable, assurance et coût salarial n'ont pas de montant légal uniforme. Tous ces coûts doivent rester révisables.

Voir [la documentation détaillée et les exemples de calcul](SASU_CALCULS_AUTOMATIQUES_2026.md).

### Sources complémentaires

- [Dépôt annuel des comptes](https://entreprendre.service-public.gouv.fr/vosdroits/F31214)
- [Tarifs de dépôt Infogreffe](https://www.infogreffe.fr/tarifs-formalites)
- [Dépôt du capital social](https://entreprendre.service-public.gouv.fr/vosdroits/F32333)
- [Assurances de la société](https://entreprendre.service-public.gouv.fr/vosdroits/F37365)
- [Taxe d'apprentissage](https://entreprendre.service-public.gouv.fr/vosdroits/F22574)
- [CVAE](https://entreprendre.service-public.gouv.fr/vosdroits/F23546)

## Limites identifiées — à ne pas présenter comme des calculs exacts

- **Paie SAS** : pas de calcul DSN complet (mutuelle, prévoyance, retraite, CSG, plafonds, exonérations ACRE, AT/MP). La personne doit vérifier sur Mon-entreprise / Urssaf.
- **Fiscalité SAS** : comptes simplifiés ; pas d'amortissements, provisions, déficits reportables, BFR, échéanciers ni salariés supplémentaires ; une trésorerie projetée n'est pas un solde bancaire certain.
- **Fiscalité TVA** : exercice de 12 mois constant, sans date précise de franchissement, TVA multi-taux ou opérations exonérées ; impossible d'affirmer le montant définitif.
- **CFE** : 300 € utilisés comme provision par défaut dans une SAS existante ne constituent pas un montant légal ou municipal ; l'avis fiscal réel prévaut.
- **Missions militaires et pompiers** : les régimes ne sont pas identiques. L'exonération fiscale des soldes de réserve opérationnelle militaire ne vaut pas une règle générale d'exclusion de toutes les ressources CAF ou rémunérations de pompiers.
- **Aides sociales** : une aide confirmée peut évoluer et ne doit pas être reconduite sans tenir compte de sa durée de validité.
- **Simulation historique** : les scénarios enregistrés sont conservés localement dans le navigateur ; des données antérieures peuvent intégrer des hypothèses erronées ou des montants accordés qui ne sont plus d'actualité. Revalider chaque scénario après changement de règle.
- **Légal** : 2026 France métropolitaine ; les autres territoires, les professions exonérées de TVA, l'IR fiscal des SAS et les régimes sectoriels ne sont pas tous pris en charge.

## Contrôles techniques

Vérifications sur le JavaScript de `index.html` : syntaxe, calcul de différentes activités micro, frais, ACRE, VFL, absence de fausses aides, équilibre du Sankey avec déficit, exemple de taxe sur salaires, exonération de taxe sur salaires, changement de simulation et reprise de ses valeurs. Les tests ont été réalisés par exécution simulée du JavaScript ; **pas d'audit exhaustif en navigateur réel** ni de certification légale de tous les cas particuliers.

## Références réglementaires officielles

- [Régime micro-social et taux](https://entreprendre.service-public.gouv.fr/vosdroits/F36232)
- [CFP du micro-entrepreneur](https://entreprendre.service-public.gouv.fr/vosdroits/F23459)
- [ACRE 2026](https://entreprendre.service-public.gouv.fr/vosdroits/F11677)
- [Prime d'activité étudiant et apprenti](https://www.service-public.gouv.fr/particuliers/vosdroits/F33375)
- [CAF, réforme de la prime d'activité 2026](https://www.caf.fr/allocataires/actualites/actualites-nationales/les-reponses-vos-questions-sur-l-evolution-de-la-prime-d-activite-en-2026)
- [CAF, aides au logement et ressources](https://www.caf.fr/allocataires/foire-aux-questions/logement)
- [Action Logement, MOBILI-JEUNE](https://www.actionlogement.fr/aide-mobili-jeune)
- [IS, seuils et conditions](https://entreprendre.service-public.gouv.fr/vosdroits/F23575)
- [CFE et exonérations](https://entreprendre.service-public.gouv.fr/vosdroits/F23547)
- [TVA et franchise](https://entreprendre.service-public.gouv.fr/vosdroits/F21746)
- [Taxe sur les salaires](https://entreprendre.service-public.gouv.fr/vosdroits/F22576)
- [Frais de création de société](https://entreprendre.service-public.gouv.fr/vosdroits/F37688)
- [Annonces légales, tarif 2026](https://entreprendre.service-public.gouv.fr/actualites/A18724)
- [Dividendes et PFU](https://entreprendre.service-public.gouv.fr/vosdroits/F32963)
- [Réserve légale](https://entreprendre.service-public.gouv.fr/vosdroits/F24024)
- [CVAE](https://entreprendre.service-public.gouv.fr/vosdroits/F23546)

**État de l'audit :** moteur de budget et erreurs les plus graves corrigés ; ce projet demeure un **simulateur pédagogique/financier indicatif**, pas un outil certifié pour le calcul exact de droits ou obligations.
