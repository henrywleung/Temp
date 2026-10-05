# Research handoff prompt

Copy everything below the line into an LLM that has unrestricted web browsing, such as ChatGPT with browsing, Perplexity, Gemini, or Claude with web search on claude.ai. Uploading PDFs you downloaded yourself works best for tasks 1 and 3.

---

You are a research assistant helping a medical-device company (BioIntelliSense, maker of the BioButton wearable, which measures heart rate, respiratory rate, skin temperature, activity, posture and HRV). We are preparing to work with Ochsner Health (New Orleans) on their AI patient-deterioration model, which sends alerts to the rapid response team. I need you to finish a literature review that an earlier assistant could not complete, because publisher sites and citation databases were blocked for it.

## Rules
- **Do not fabricate.** Every citation must include a DOI or URL that you actually opened. If you can't open a page or find something, write "NOT FOUND" or "COULD NOT ACCESS". Never guess.
- **Quote, don't paraphrase,** whenever I ask for exact wording, and give the page or section.
- **Label every claim** as one of: **VERIFIED (full text)**, **ABSTRACT ONLY**, or **SECONDARY SOURCE (name it)**.
- Tag each paper's relevance as **HIGH / MEDIUM / LOW**. HIGH means early warning scores, deterioration prediction or machine-learning models, Epic Deterioration Index, continuous or wearable monitoring, respiratory rate accuracy, or rapid-response outcome data.

## Tasks (in priority order)

### 1. Winterbottom 2022: full reference list and key details
Paper: Winterbottom F, Webre H, Gaudet K, Burton J. "A Patient Safety Solution: Evaluation of a 24/7 Nurse-led Proactive Rapid Response Program." *Int J Crit Care* 2022;16(2):32-44. DOI 10.29173/ijcc32. PDF: https://wfccn-ijcc.com/index.php/ijcc/article/download/32/28/56
- Give the **complete reference list**. For each reference: full citation, DOI, a 1-2 sentence finding, and a relevance tag.
- Quote **word for word** every sentence about artificial intelligence alerts, the EHR, "portable devices" or "wearable technologies". Search snippets paraphrase one sentence as saying "In September 2017, artificial intelligence clinical deterioration alerts were introduced through the EHR, as were portable devices and patient wearable technologies." Confirm the exact text and the date. Press coverage dates the AI tool to 2018.
- Report any **device vendor or product names**.
- Describe the AI alert as the paper does: inputs, thresholds, scoring frequency, alerts per day, and who receives them.
- Give an **outcome table** with exact before/after rates (per 1,000 discharges or patient-days), p-values, study dates and the cost/ROI figures. Our notes say non-ICU arrests went from 5.7 to 2.5, unplanned ICU transfers from 62.9 to 52.3, and deaths from 37.1 to 33.1 per 1,000 discharges, with about $500K cost against about $500K saved. Confirm or correct these.
- For each HIGH reference, open it and confirm its main finding.

### 2. Forward citations: who cites the Ochsner papers
Use Google Scholar "Cited by", Semantic Scholar, OpenAlex (https://api.openalex.org/works/doi:10.29173/ijcc32, then follow `cited_by_api_url`), Crossref and Scopus if you have it. List every citing paper for:
- 10.29173/ijcc32 (Winterbottom 2022, IJCC)
- 10.1097/CNQ.0000000000000379 (Winterbottom & Webre 2021, *Crit Care Nurs Q* 44(4):424-430, "Rapid Response System Restructure")
- 10.4037/ccn2025623 (Winterbottom 2025, *Crit Care Nurse* 45(2):74-76, "From Reactive to Proactive")
- 10.31486/toj.19.0057 (Kumar et al. 2020, *Ochsner J*, MEWS in unplanned surgical ICU admissions)
- Fixler et al. 2023, "Alert to Action," *Ochsner J* 23(3):222-231 (find the DOI)

For each citing paper: full citation, DOI, which Ochsner paper it cites, what it found, how it uses the Ochsner work, and a relevance tag.

Also check whether these actually cite any of the above. Answer **yes or no for each**, based on their reference lists:
- Trenchard-Turner et al., *Intensive Care Med* 2023, DOI 10.1007/s00134-023-07021-y
- Winters et al. 2025, DOI 10.1177/25160435241298992 (AHRQ "Making Healthcare Safer IV: Failure to Rescue – Rapid Response Systems")
- Cioccari et al. 2025, "Ten Steps for Implementing a Hospital Rapid Response System," *J Med Syst*
- Zhang 2024 (*Heart & Lung*), a systematic review of rapid response systems
- Piasecki 2023, a scoping review
- Wu 2022 (*BMC Nursing*)
- Róin 2025 (*Scand J Caring Sci*)
- *Crit Care Nurse* 45(4):49, "Integration of Rapid Response Teams and Early Warning Systems…" (PMID 40748923)
- *Crit Care Nurse* 46(1):9, "Using Artificial Intelligence With Rapid Response Teams," and 46(1):10, "Reflection on the Use of a Rapid Response Team…". Are these letters responding to Winterbottom 2025?

### 3. Ochsner's newer early warning system with "12 hours lead time"
Winterbottom FA. "Rapid Response." *Am J Crit Care* 2025;34(4):317-322. Snippets say Ochsner "piloted an automated early warning system (EWS) based on a very large database" giving rapid response teams about 12 hours of lead time.
- Quote the passage word for word.
- Find the **name or vendor** of that system, plus its inputs, pilot dates, units, alert volume and any results.
- Check the full reference list for the source of the 12-hour figure.
- Do the same for Winterbottom FA, "Rapid Response Innovation," *Crit Care Nurs Clin North Am* 2026 (PMID 42103416). It covers "ambient monitoring networks" and "cognitive computing-enhanced detection". Name every product, vendor or wearable it mentions, and quote its conflict-of-interest statement (reported as Zoll Medical and Baxter).

### 4. Which deterioration model does Ochsner actually run?
- Is Ochsner's 2018 Epic and Microsoft Azure model (Epic's machine-learning platform, 4-hour prediction, 6-10 alerts a day, 44% fewer codes outside the ICU in a 90-day pilot in fall 2017) the **Epic Deterioration Index**, a custom Ochsner model, or something else? Search Epic UGM/XGM presentations, EpicShare, Ochsner press releases, HIMSS case studies, Microsoft case studies and Ochsner Journal.
- Has Ochsner published or presented anything on EDI, eCART, the Rothman Index, the CLEW, Philips, Masimo, Baxter/Hillrom or BioIntelliSense?
- What did Melinda Stretzinger's EpicShare story ("Identifying signs of sepsis sooner with remote inpatient monitoring") say about tools and alert volumes?
- Who was the vendor of the first monitoring device in Ochsner's NEWS plus Virtual ICU nursing project (Kala Gaudet coached it)? The write-up said that device "did not fully meet operational needs." Search AACN CSI Academy project write-ups for Ochsner ("Improving Early Detection of Patient Deterioration").

### 5. Edelson et al. 2024 comparison: missing details
Edelson DP, Churpek MM, Carey KA, et al. "Early Warning Scores With and Without Artificial Intelligence." *JAMA Netw Open* 2024;7(10):e2438986 (open access, PMC11544488).
- Which **EDI version** was tested, and how often was each score calculated?
- Give the AUROC for EDI with its 95% CI, and the PPV at the **high-risk** matched threshold for all six scores.
- Give lead times reported in **this** paper, not the eCARTv5 development paper.
- Give any subgroup results by respiratory status or by how often vital signs were charted.
- Give the full author list and conflict-of-interest statements.

### 6. Background (lower priority)
- The 2026 *J Gen Intern Med* meta-analysis of the Epic Deterioration Index (pooled AUROC reported as about 0.79): full citation, number of studies, pooled AUROC with CI, and how much results varied between studies.
- Any studies of **wearable or continuous respiratory-rate monitoring** feeding an early warning score on general wards (e.g., EarlySense, Philips IntelliVue Guardian, Masimo, BioButton). Report false-alarm rates and how RR measurement error affected scores.

## Output format
Return one markdown document with a section per task. Use tables for reference lists and citing-paper lists, with columns: Citation | DOI/URL | Finding | Relevance | Verification level. End with:
- a list of anything you could not access, and
- a "Top 5 findings for the Ochsner meeting" summary.
