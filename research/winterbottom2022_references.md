# Winterbottom et al. (2022): reference list and evidence review

**Status: INCOMPLETE. The full text and reference list could not be retrieved.**

## 1. Access log (2026-10-05)

| Source | Result |
|---|---|
| wfccn-ijcc.com article page and PDF (WebFetch) | Blocked by the network egress proxy (EGRESS_BLOCKED) |
| doi.org/10.29173/ijcc32 | Blocked |
| researchgate.net (publication 364252000) | Blocked |
| api.openalex.org, api.semanticscholar.org, Europe PMC (ebi.ac.uk) | Blocked |
| scholar.archive.org, aacnjournals.org | Blocked |
| WebSearch | Worked, but it returns only search-engine snippets that a model has summarized. It never returned the reference list. |

Because of this, **no reference list is given below.** No citation in this file is claimed to be one of the paper's references. To finish the task, someone needs to open the PDF directly (https://wfccn-ijcc.com/index.php/ijcc/article/download/32/28/56) and paste or save the text. Then the reference-by-reference review can be done.

## 2. Verified bibliographic data

- Winterbottom F, Webre H, Gaudet K, Burton J. *A Patient Safety Solution: Evaluation of a 24/7 Nurse-led Proactive Rapid Response Program.* International Journal of Critical Care. 2022 (September);16(2):32-44. DOI: 10.29173/ijcc32. The PDF header reads "A Pre- Post Evaluation of a 24/7 Nurse-led Proactive Rapid Response...".
- Authors, as given in the search results: Fiona Winterbottom, DNP, APRN, ACNS-BC, ACHPN, CCRN (Ochsner Health, New Orleans); Heather Webre, MSN, RN, CCRN; Kala Gaudet, BSN, RN, CCRN; Jeff Burton, PhD.

## 3. Paper content found in search snippets (paraphrased, NOT verbatim)

The search tool summarizes pages, so none of the text below should be quoted as the authors' exact wording.

- **Problem:** a high rate of cardiac arrests outside the ICU, and no structured system to identify and rescue deteriorating patients before arrest.
- **Design and setting:** a pre-post evaluation in a 650-bed quaternary academic regional referral center (Ochsner), January 2014 to February 2020. The rapid response system redesign began in early 2017. The 24/7 nurse-led proactive rapid response program launched in December 2017.
- **AI and devices (key sentence, close paraphrase, appeared in two separate searches):** "In September 2017, artificial intelligence clinical deterioration alerts were introduced through the electronic health record (EHR), as were portable devices and patient wearable technologies."
  - **Not found:** any device vendor or brand, or any detail on how the AI alert worked in the paper (inputs, thresholds, alert volume). These need the PDF.
- **Program activity:** high-risk screening was the largest category of events, followed by proactive rounding, then reactive responses. The biggest gains were in screening and rounding.
- **Outcomes:** the authors report statistically significant decreases in critical-care cardiopulmonary arrests, non-critical-care cardiopulmonary arrests, rapid response consults, unplanned ICU transfers, and hospital deaths. **The exact rates and p-values were not retrievable.** Search summaries mixed in numbers from other papers (for example "2.2 to 0.8 per 1000 patient-days" and "1.69/1,000 discharges"). Those numbers are NOT from this paper and must not be attributed to it.
- **Conclusion:** a structured 24/7 nurse-led rapid response program can decrease cardiopulmonary arrests, unplanned ICU transfers, and hospital deaths.

## 4. Context: Ochsner's AI deterioration model (from public sources, not from the paper)

- Ochsner, Epic (machine learning platform) and Microsoft Azure; launched around 2018. Predicts deterioration about 4 hours ahead. Alerts go to the Rapid Response Team, which intervenes proactively ("pre-code" alerts).
- **Inputs:** lab values, vital signs and other EHR data ("thousands of data points"; data are consumed as they enter the EMR). Models were built on datasets of more than 125,000 hospitalized patients.
- **Alert volume:** "six to 10" alerts a day out of hundreds of patients.
- **Pilot result:** 44% reduction in adverse events (including cardiac arrests) outside the ICU over a 90-day pilot. The model won the 2018 Microsoft Health Innovation Award.
- Sources: Microsoft Transform, https://news.microsoft.com/transform/ochsner-ai-prevents-cardiac-arrests-predicts-codes/ ; AHA case study, https://www.aha.org/system/files/2018-06/ochner-value-initiative-warning-system-case-study.pdf ; MedCity News (Mar 2018), https://medcitynews.com/2018/03/ochsner-health-system-uses-ai-detect-early-warning-signs-patients/ ; innovationOchsner, https://www.ochsner.org/io/work/ai-predictive-modeling/ ; HC Innovation Group, https://www.hcinnovationgroup.com/population-health-management/news/13029884/ochsner-health-system-adopts-new-ai-powered-early-warning-system
- Note on timing: the paper's snippet dates the AI alerts to September 2017, while the press coverage says 2018. This needs checking against the PDF.

## 5. Related literature that surfaced (NOT confirmed as references in the paper)

Relevance tags reflect BioButton's use case.

- **HIGH.** (Authors not confirmed in search; probably Edelson DP, Churpek MM et al.) Early Warning Scores With and Without Artificial Intelligence. JAMA Netw Open 2024. https://www.ncbi.nlm.nih.gov/pmc/articles/PMC11544488/ . Compared scores head to head: eCARTv5 had the best AUROC (0.895); the Epic Deterioration Index was among the worst (0.808). This is directly relevant to the Epic-based model Ochsner uses.
- **MEDIUM.** Heal M, Silvest-Guerrero S, Kohtz C. Design and Development of a Proactive Rapid Response System. CIN 2017;35(2):77-83. DOI 10.1097/CIN.0000000000000292. In a quasi-experimental study, EHR-triggered early-warning criteria increased RRT activations compared with a control unit (P = .013). It is not by Winterbottom.
- **MEDIUM.** Winterbottom-led follow-up: "From Reactive to Proactive: A Novel Rapid Response System." Crit Care Nurse 2025;45(2):74. PubMed 40168007. Abstract not retrieved.
- **MEDIUM.** "Rapid Response System Restructure: Focus on Prevention and Early Intervention." PubMed 34437321. Authorship and findings not retrieved.
