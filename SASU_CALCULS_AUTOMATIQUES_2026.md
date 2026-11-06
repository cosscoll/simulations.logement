# Calculs automatiques SASU / SAS — simulation 2026

**Périmètre :** SASU/SAS soumise à l'impôt sur les sociétés (IS), France métropolitaine, revenus constants sur 12 mois fictifs.
Les règles sont exécutées automatiquement dès que le CA HT mensuel change. Les résultats sont **estimés**, pas une liquidation fiscale ou une fiche de paie officielle.

## Mode par défaut

1. Ajouter une **SASU** (l'associé est seul).
2. Saisir un **CA HT moyen mensuel** : le site calcule une projection de CA sur douze mois.
3. Par défaut : **0 € de rémunération dirigeant**, aucune cotisation sociale sur une rémunération inexistante ; les frais de fonctionnement facultatifs sont provisionnés à **105 €/mois** (15 € banque + 75 € comptabilité + 15 € assurance). Ces trois montants ne sont **pas des taxes obligatoires**.
4. Les **charges d'exploitation HT** du formulaire réduisent le bénéfice. La TVA d'achat spécifiée est ajoutée lorsqu'elle n'est pas récupérable.
5. L'**IS** est calculé sur le bénéfice annuel après charges. Le taux réduit de 15 % jusqu'à 42 500 € est appliqué uniquement si le CA annuel ne dépasse pas 10 M€, si le capital est libéré en totalité, et si la détention par des personnes physiques est d'au moins 75 %. Sans cette confirmation, le calcul retient 25 %.
6. La **CFE** vaut 0 € en année de création, puis la projection utilise le CA de référence et une hypothèse de base locale et de taux communal ; à défaut d'historique, elle prend le CA annualisé indiqué, en signalant que ce n'est pas le montant fiscal réel. Le taux communal par défaut est supposé à **30 %** à titre indicatif ; il n'existe **aucun** taux national unique.
7. La **TVA** est projetée selon le CA N-1, les seuils de base et les seuils majorés applicables aux activités habituelles. Si le seuil majoré est dépassé avec un CA mensuel constant, la TVA n'est appliquée qu'à compter du premier mois de dépassement estimé. Cette approximation ne connaît pas les dates exactes des factures et ne remplace pas la TVA réelle.
8. Les **frais de création** sont appliqués une seule fois pour une société créée en 2026 (RCS, bénéficiaires effectifs, annonce légale). Les autres prestations éventuelles, non obligatoires, ne sont pas inventées.
9. La **rémunération** entraîne un coût social *approché* dès qu'elle est supérieure à zéro. Le prélèvement à la source dépend du taux renseigné. Seul le salaire net après PAS entre dans le budget personnel. **Le CA et le bénéfice de la SASU ne sont pas des revenus personnels**.
10. Pour les grandes sociétés, le calcul prévoit aussi la **contribution sociale de 3,3 % sur l'IS dépassant 763 000 €**, lorsque les conditions d'exonération ne sont pas réunies. La CVAE demeure à contrôler selon la valeur ajoutée.

## Exemple détaillé : 3 000 € HT/mois, SASU créée en 2026

Hypothèses : aucun autre frais d'exploitation, aucun salaire, frais de fonctionnement automatiques 105 €/mois, activité de services en franchise de TVA, capital non confirmé libéré (IS normal à 25 %), aucune distribution de dividendes.

| Poste | Montant |
| --- | ---: |
| CA HT annuel | 36 000 € |
| Frais de fonctionnement estimés (105 × 12) | −1 260 € |
| Formalités SASU 2026 (RCS, bénéficiaires, annonce légale avec TVA non récupérable) | −223,56 € |
| Salaire / charges sociales du président | 0 € |
| CFE en année de création | 0 € |
| Résultat fiscal prévisionnel | 34 516,44 € |
| IS à 25 % | 8 629,11 € |
| Résultat après IS | **25 887,33 €/an**, soit **2 157,28 €/mois** en moyenne |

Si les conditions du taux réduit d'IS sont confirmées, l'IS estimé est alors **5 177,47 €** (15 % de 34 516,44 €), avec **29 338,97 €/an** de résultat après IS, soit **2 444,91 €/mois**. Il s'agit du **résultat dans la société**, pas de sommes versées à l'associé. La réserve légale et la fiscalité éventuelle des dividendes peuvent ensuite intervenir.

## Ce qui ne peut pas être calculé exactement avec le seul CA

- La CFE dépend aussi de la commune, des bases locales, de l'année N-2, des locaux professionnels et des éventuelles exonérations.
- La TVA dépend de l'historique N-1, des taux applicables aux opérations, des dates des factures, des achats ouvrant droit à déduction et des exemptions sectorielles.
- Les cotisations sociales du président dépendent de la paie exacte (retraite, prévoyance, mutuelle, plafonds, etc.). Taux moyens = **estimation**.
- Les achats, frais et dépenses professionnelles propres à chaque SASU doivent être renseignés ou remplacés par les provisions proposées.
- L'IS définitif dépend de la clôture, des amortissements, des déficits reportables et des autres régularisations.
- La trésorerie réelle dépend des encaissements/décaissements, du BFR et des échéances.

## Références officielles consultées

- [IS et taux réduit : Service Public](https://entreprendre.service-public.gouv.fr/vosdroits/F23575)
- [Fiscalité de la SASU](https://entreprendre.service-public.gouv.fr/vosdroits/F36215)
- [Franchise en base de TVA (seuils 2026)](https://entreprendre.service-public.gouv.fr/vosdroits/F21746)
- [CFE : calcul, base minimale par CA et taux communal](https://entreprendre.service-public.gouv.fr/vosdroits/F23547)
- [CFE d'une entreprise sans local](https://entreprendre.service-public.gouv.fr/vosdroits/F32389)
- [Frais de création d'une société](https://entreprendre.service-public.gouv.fr/vosdroits/F37688)
- [Tarifs d'annonces légales 2026](https://entreprendre.service-public.gouv.fr/actualites/A18724)
- [Taxe sur les salaires](https://entreprendre.service-public.gouv.fr/vosdroits/F22576)
- [Contribution sociale supplémentaire à l'IS](https://entreprendre.service-public.gouv.fr/vosdroits/F23510)
- [Simulateur rémunération SASU Urssaf](https://mon-entreprise.urssaf.fr/simulateurs/sasu)

**Date :** 6 novembre 2026. **Statut :** projection automatique, non certifiée.
