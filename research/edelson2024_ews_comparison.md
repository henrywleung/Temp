# Early Warning Scores With and Without Artificial Intelligence (JAMA Netw Open 2024)

**Citation:** Edelson DP, Churpek MM, Carey KA, et al. Early Warning Scores With and Without Artificial Intelligence. *JAMA Netw Open.* 2024;7(10):e2438986. Published Oct 15, 2024. DOI [10.1001/jamanetworkopen.2024.38986](https://dx.doi.org/10.1001/jamanetworkopen.2024.38986). Open access ([PMC11544488](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC11544488/)).

Note: the full text was blocked from this environment. The details below come from search-result snippets of the paper, its abstract and the eCARTv5 development paper. Entries marked (standard definition) are the published definitions of those scores, not text taken from this paper.

## Design
- Retrospective cohort: 362,926 medical-surgical ward encounters at 7 hospitals in the Yale New Haven Health System.
- Outcome: ICU transfer or death within 24 hours.
- Compared 3 AI/proprietary scores (eCARTv5, Rothman Index, Epic Deterioration Index) with 3 public weighted scores (MEWS, NEWS, NEWS2).
- Thresholds were matched to the sensitivity of NEWS at its moderate-risk (5) and high-risk (7) cutoffs, then PPV and "efficiency" (alerts needed per event found) were compared.

## Performance

| Score | Type | AUROC (95% CI) |
|---|---|---|
| eCARTv5 | ML (gradient-boosted trees), AgileMD | **0.895** (0.891-0.900) |
| NEWS2 | Public | 0.831 (0.826-0.836) |
| NEWS | Public | 0.829 (0.824-0.835) |
| Rothman Index | Proprietary (PeraHealth) | 0.828 (0.823-0.834) |
| Epic Deterioration Index | Proprietary (Epic) | 0.808 |
| MEWS | Public | 0.757 (0.750-0.764) |

- **PPV at the moderate-risk matched sensitivity (NEWS 5):** lowest was EDI at 6.3% (score 41), highest was eCARTv5 at 17.3% (score 94). At the same sensitivity, EDI produces roughly 2.7x as many false alerts per true event as eCART.
- **Statistical comparison:** NEWS significantly outperformed EDI. eCARTv5 had the highest PPV at both matched thresholds.
- **Lead time:** the authors say eCART flagged deterioration "with sufficient time to intervene." From the eCARTv5 development paper (Crit Care Explor 2025): at the moderate threshold the median lead time was 16 h for eCARTv5 versus 17 h for NEWS and 13 h for MEWS; at the high threshold it was 5 h for eCARTv5 versus 3 h for NEWS and 2 h for MEWS.

## Inputs per score

| Score | Inputs |
|---|---|
| **eCARTv5** | 97 features: age, BMI, vital signs (incl. RR, SpO2), labs, time of day, nursing/RT documentation (delivered FiO2, Braden), plus 24-h min/max/mean trends. **Top features: max RR in prior 24 h, delivered FiO2, min SBP in prior 24 h, HR.** |
| **Epic Deterioration Index** | Age; SBP, temp, HR, RR, SpO2; GCS, neuro assessment, cardiac rhythm, O2 requirement; hematocrit, WBC, K, Na, pH, platelets, BUN (from Singh 2021) |
| **Rothman Index** | (standard definition) About 26 variables: vitals, labs, cardiac rhythm, Braden score, nursing head-to-toe assessments |
| **NEWS / NEWS2** | (standard definition) RR, SpO2, supplemental O2, temp, SBP, HR, level of consciousness (NEWS2 adds new confusion and a hypercapnic SpO2 scale) |
| **MEWS** | (standard definition) SBP, HR, RR, temp, AVPU |

## Caveats
- **Conflict of interest:** Edelson has equity in AgileMD (which sells eCART) and a eCART patent, with royalties paid by the University of Chicago. An editorial in the same issue, "Toward the Rigorous Evaluation of Early Warning Scores" (DOI 10.1001/jamanetworkopen.2024.38966), discusses this.
- Only one health system was studied, retrospectively, and no score was retrained locally.
- The EDI version is not reported here, and Ochsner's model may not be EDI.

## Why it matters for BioButton / Ochsner
- **RR matters most:** in the best-performing model, the most important feature is RR (max over 24 h). RR is in every score above, so continuous BioButton RR could add real signal, but a high-RR bias would directly inflate scores and drive false alerts.
- **HR is also a top feature,** and BioButton measures it.
- **Trend features help:** eCART's 24-h min/max/mean trends are the kind of features that continuous wearable data supports better than q4h manual vitals.
- **Talking point for Ochsner:** if Ochsner runs EDI, the comparison shows that even NEWS beats it, and an ML score with trends beats both.

## Sources
- [JAMA Netw Open / Ovid full text](https://www.ovid.com/journals/janop/fulltext/10.1001/jamanetworkopen.2024.38986~early-warning-scores-with-and-without-artificial)
- [PMC11544488](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC11544488/)
- [Becker's: Epic deterioration index falls short](https://www.beckershospitalreview.com/healthcare-information-technology/digital-health/epic-deterioration-index-falls-short-study/)
- [Editorial: Toward the Rigorous Evaluation of Early Warning Scores](https://jamanetwork.com/journals/jamanetworkopen/fullarticle/2824889)
- [eCARTv5 development paper, Crit Care Explor 2025 (PMC11949291)](https://pmc.ncbi.nlm.nih.gov/articles/PMC11949291/)
- [eCARTv5 supplement (feature list)](https://cdn-links.lww.com/permalink/ccx/b/ccx_1_1_2025_02_15_churpek_cce-d-24-00553_sdc1.pdf)
