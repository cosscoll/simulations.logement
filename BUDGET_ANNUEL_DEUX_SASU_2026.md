# Prévision annuelle — SASU IA et SASU UCP (référence 2026)

**Préparé le 6 novembre 2026.** Simulation d'une **année pleine de 12 mois**, même si les sociétés sont créées fin 2026. France métropolitaine, SASU à l'IS, président non rémunéré, aucun salarié, activité numérique. Il s'agit de deux **profils de budget**, et non de deux sociétés juridiquement ou comptablement créées. Les tarifs de banque, conseil, assurances, SaaS et acquisition sont des **hypothèses de dépenses**, à remplacer par les devis et les factures. Montants en euros arrondis à deux décimales.

## 1. Budget de référence pour 12 mois

| Poste | SASU IA (formations et produits numériques) | SASU UCP (plateforme de mise en relation BTP) | Nature |
|---|---:|---:|---|
| Compte bancaire (9 €/mois chacune) | 108,00 € | 108,00 € | Contrat estimé |
| Expert-comptable (95 €/mois et 130 €/mois) | 1 140,00 € | 1 560,00 € | **Prestataire facultatif**, tenue comptable obligatoire |
| Assurance RC / cyber (18 €/mois et 55 €/mois) | 216,00 € | 660,00 € | Tarifs indicatifs, obligations dépendant de l'activité |
| Hébergement web (25 / 60 €/mois) | 300,00 € | 720,00 € | Abonnement estimé |
| Base de données (25 €/mois) | 300,00 € | 300,00 € | Abonnement estimé |
| Domaine et messagerie (12 / 15 €/mois) | 144,00 € | 180,00 € | Renouvellements commerciaux |
| Emails transactionnels (0 / 20 €/mois) | 0,00 € | 240,00 € | Dépend de l'usage et des quotas gratuits |
| Sauvegardes, sécurité et surveillance (20 / 45 €/mois) | 240,00 € | 540,00 € | Services/outils supplémentaires estimés |
| Outils de formation, vidéo ou monitoring (30 / 35 €/mois) | 360,00 € | 420,00 € | Logiciels supplémentaires estimés |
| Acquisition et marketing (100 / 200 €/mois) | 1 200,00 € | 2 400,00 € | Dépenses commerciales choisies |
| Support/modération externalisé (0 / 120 €/mois) | 0,00 € | 1 440,00 € | Prestations choisies ; 0 si gérées soi-même |
| Conseil juridique, documents CGV/CGU, RGPD, suivi conformité | 300,00 € | 900,00 € | **Budget de services**, pas une taxe légale |
| **Total de fonctionnement HT hors frais de paiement** | **4 308,00 €** | **9 468,00 €** | Dépenses projetées |
| TVA amont estimée non récupérable si franchise TVA | 736,80 € | 1 560,00 € | Hypothèse simplifiée de TVA à 20 % sur compta et logiciels ; factures réelles à vérifier |
| **Coût de fonctionnement de 12 mois, en franchise** | **5 044,80 €** | **11 028,00 €** | Charges projetées |
| Création légale : RCS + bénéficiaires effectifs + annonce légale TTC | 223,56 € | 223,56 € | Une seule fois si création en 2026 |
| Réserve pour futures corrections/maintenance (150 / 250 €/mois) | 1 800,00 € | 3 000,00 € | **Réserve de trésorerie, non déductible** tant que non dépensée |
| Matelas imprévus (10 % / 15 % du fonctionnement estimé HT) | 430,80 € | 1 420,20 € | **Réserve de trésorerie, non déductible** |
| Réserve CFE de la prochaine année | 300,00 € | 400,00 € | **Hypothèse**, pas avis fiscal ; montant final local inconnu |
| Réserve pour premier dépôt annuel des comptes | 44,14 € | 44,14 € | Référence de prix du dépôt **par correspondance**, non coût certain du canal numérique |
| **ENVELOPPE ANNUELLE À ANTICIPER** | **7 843,30 €** | **16 115,90 €** | Somme des dépenses projetées et réserves |
| **ENSEMBLE DES DEUX SASU** | | **23 959,20 €** | **1 996,60 €/mois** en moyenne sur 12 mois |

**Attention :** la TVA des fournisseurs dépend de leur localisation, de leur régime et du droit à déduction. Les deux lignes « TVA non récupérable » sont des hypothèses prudentes du simulateur, pas des montants de facture. Le prix des services américains de type Vercel ou Supabase est publié en USD ; les montants en euros sont des **budgets arrondis**, pas une conversion de prix contractuelle.

Les enveloppes ci-dessus sont calculées avec **0 € de CA**, donc 0 € de frais de paiement et 0 € d'IS sur un bénéfice. Dès qu'il existe du CA ou du salaire, taxes et frais variables sont recalculés en fonction des hypothèses de la simulation. Les revenus de commissions de UCP ne sont pas assimilés au chiffre d'affaires des artisans.

## 2. Frais qui varient lorsque les entreprises vendent

**Paiements par carte** (carte standard EEE et tarif simplifié Stripe France au 6 novembre 2026) : `1,5 % × montant encaissé par carte + 0,25 € × nombre de paiements`. Le nombre est estimé par `montant encaissé ÷ panier moyen`. Le simulateur utilise 99 € de panier moyen IA et 25 € pour UCP. Ce n'est **pas une obligation de choisir Stripe** et les frais réels peuvent varier. Le fonctionnement de Stripe Connect, les paiements reversés aux artisans, les litiges ou la fraude peuvent créer des frais supplémentaires non inclus.

**Exemple purement illustratif :**
- IA : 24 000 € de recettes annuelles entièrement encaissées par carte, panier 99 € : **420,61 € de frais de paiement** avant frais supplémentaires éventuels.
- UCP : 36 000 € de recettes de la plateforme encaissées par carte, panier 25 € : **900,00 € de frais de paiement** avant frais Connect.
- Ces montants deviennent des charges d'exploitation **si réellement facturés** ; une marge de sécurité supplémentaire est calculée dans le budget de trésorerie.

**Impôt sur les sociétés** : 25 % du bénéfice imposable ; sous conditions (CA ≤ 10 M€, capital entièrement libéré et détention ≥ 75 % personnes physiques), 15 % sur les 42 500 premiers euros de bénéfice, puis 25 %. Aucune obligation d'IS sur un exercice déficitaire ; les déficits reportables peuvent nécessiter un calcul supplémentaire.

**CFE** : exonération l'année de création (avec formalités correspondantes), puis calcul local en fonction de l'année de référence et de la commune. Le tableau du Service Public contient des **bases minimales**, et non un impôt unique. Les sommes de 300 € et 400 € prévues pour les exercices suivants sont uniquement des réserves prudentes ; elles ne présument pas le montant de l'avis.

**TVA** : l'entreprise peut rester en franchise sous conditions ou devenir redevable ; la TVA collectée auprès des clients est séparée du CA HT et la TVA amont peut être récupérée sous conditions. Formation professionnelle et livres numériques peuvent nécessiter des qualifications ou taux spécifiques. La simulation ne remplace pas l'analyse des prestations.

**Cotisations sociales** : président non rémunéré = 0 € de cotisations sur son mandat ; s'il reçoit un salaire, le coût employeur et le prélèvement personnel s'ajoutent. Les paiements de dividendes ont une fiscalité distincte.

**Autres frais éventuels** : personnel, auto-entrepreneurs sous-traitants, prestataires de maintenance, conseil fiscal/juridique, licences et contenus, taxe sur les salaires, CVAE à haut niveau d'activité, indemnités de litige, remboursements/chargebacks, consommations API IA, incidents cyber, achat de matériel et renouvellement de licences. **Ne pas forcer tous ces postes dans les charges s'ils ne sont pas engagés.**

## 3. Obligations particulières

### SASU IA

Si elle dispense de la **formation professionnelle** au sens du Code du travail, déclaration d'activité dans les 3 mois suivant la première convention ou le premier contrat et **bilan pédagogique et financier annuel**. Le site doit être conforme aux obligations de vente à distance, contenus numériques, confidentialité et rétractation applicables. Une démarche Qualiopi peut s'avérer nécessaire si la société cherche des **financements publics/mutualisés** ; les tarifs des audits et du conseil ne sont **pas** inclus dans le total de base, car ils dépendent du périmètre.

### SASU UCP

Plateforme d'intermédiation : CGU/CGV, transparence de la qualité des professionnels, processus de signalement/modération, protection des données, sécurité, disponibilité du service, prévention des fraudes. Si UCP encaisse ou redistribue le **prix des travaux** au nom des artisans, faire vérifier le statut de la plateforme et les modalités de paiement auprès du prestataire financier ; **ne pas confondre le volume de travaux avec le CA réellement conservé par UCP**. Un chatbot recourant à une API facturée à l'usage a un coût à intégrer lorsque son déploiement réel sera défini.

## 4. Cadence des frais et règle de trésorerie

| Moment | Dépenses ou obligations principales | Nature |
|---|---|---|
| Au moment de la création | Annonce légale, RCS, bénéficiaires effectifs ; éventuel dépôt de capital payant | Paiements ponctuels ; le capital n'est pas une charge |
| Chaque mois | Banque, compta si externalisée, hébergement, données, domaines, outils, sécurité, marketing, modération | Paiements variables ou abonnements |
| À chaque vente | Commission de paiement ; éventuellement Connect, remboursement, litiges | Variable |
| À la clôture | Établissement des comptes, déclarations fiscales, résultat fiscal, IS | Obligation, montant calculé selon bénéfice |
| Après approbation | Dépôt annuel des comptes (en principe exercice suivant pour création fin 2026) | Frais obligatoires du dépôt, montant selon canal |
| Année suivant la création | CFE selon les éléments d'imposition et règles d'exonération | Montant local, non connu par le seul CA |
| À tout moment | Sécurité, contestations, maintenance, perte d'un prestataire | Pour cette raison, réservez un matelas de trésorerie |

Si les deux sociétés sont créées le **6 novembre 2026**, leur première période jusqu'au 31 décembre 2026 ne dure pas 12 mois. Le tableau représente **12 mois de régime de fonctionnement**, sans tenter de calculer la fiscalité proratisée d'une création tardive. Il faut paramétrer la date exacte de début, l'exercice et les premiers revenus pour établir un calendrier de trésorerie réel.

## 5. Optimisation sans supprimer les obligations

- Une comptabilité **autonome** peut remplacer le prestataire, mais impose de tenir des comptes conformes et de gérer bilan/déclarations.
- L'acquisition marketing peut démarrer faible et progresser avec les ventes ; le budget de 100/200 €/mois n'est pas légalement imposé.
- Les outils de paiement, email et base de données disposent d'offres à prix variable ; une activité commerciale sur Vercel n'est pas destinée à utiliser l'offre Hobby personnelle/non commerciale.
- Les réserves sont **du cash immobilisé volontairement**, pas des factures ou des charges déductibles avant dépense.
- Si les deux structures utilisent certains prestataires communs, une facture et une répartition comptable justifiée doivent éviter une double facturation ou une imputation non documentée.

## 6. Sources officielles et fournisseurs

Réglementation : [IS SASU](https://entreprendre.service-public.gouv.fr/vosdroits/F36215) ; [IS taux et conditions](https://entreprendre.service-public.gouv.fr/vosdroits/F23575) ; [CFE](https://entreprendre.service-public.gouv.fr/vosdroits/F23547) ; [formation professionnelle](https://entreprendre.service-public.gouv.fr/vosdroits/F19087) ; [dépôt des comptes](https://entreprendre.service-public.gouv.fr/vosdroits/F31214) ; [formalités de constitution](https://entreprendre.service-public.gouv.fr/vosdroits/F37688) ; [tarifs dépôts comptes par correspondance](https://www.infogreffe.fr/tarifs-formalites) ; [tarifs guichet unique](https://formalites.entreprises.gouv.fr/tarifs.php).

Fournisseurs : [Stripe France, frais cartes](https://stripe.com/fr/pricing) ; [Stripe Connect, cas plateforme](https://stripe.com/connect/pricing) ; [Vercel plans](https://vercel.com/pricing) ; [Supabase pricing](https://supabase.com/pricing) ; [Resend email](https://resend.com/pricing).

**Conclusion de planification :** **7 843,30 €** pour IA et **16 115,90 €** pour UCP, soit **23 959,20 € pour les deux** sur un exercice type de 12 mois, à CA zéro, incluant des réserves non déductibles. À ajuster selon devis, outils réellement utilisés, CA, régime de TVA, salaires, fréquence de paiements et démarrage exact.
