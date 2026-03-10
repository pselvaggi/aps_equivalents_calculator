# Antipsychotic Dose Equivalent Calculator

A single-file, offline-ready clinical tool for converting antipsychotic doses to **olanzapine equivalents (OLZ eq)** and **chlorpromazine equivalents (CPZ eq)** in real time.

Built for research databases in psychiatry and neuroimaging. No installation required — open `index.html` in any browser.

---

## Features

- **Real-time calculation** — results update instantly as you type
- **Up to 3 oral antipsychotics + 1 LAI** per patient
- **Multi-patient support** — add as many patients as needed
- **LAI conversion** — dose × PK factor → daily oral equivalent → OLZ/CPZ eq
- **Automatic flags** — missing data, estimated factors, complete data
- **Patient summary table** — overview of all entries at a glance
- **CSV export** — one-click export ready for SPSS / R / Excel
- **Reference tables** — conversion factors always visible at the bottom
- **No dependencies** — single HTML file, works fully offline

---

## Drugs Supported

**Oral:** Olanzapine, Risperidone, Haloperidol, Aripiprazole, Quetiapine, Amisulpride, Paliperidone, Lurasidone, Ziprasidone, Brexpiprazole, Clozapine, Chlorpromazine, Perphenazine, Zuclopenthixol, Levomepromazine, Clothiapine, Cariprazine, Promazine, Pimozide, Levosulpiride, Fluphenazine

**LAI:** Risperidone LAI (Risperdal Consta), Paliperidone LAI 1M/3M, Aripiprazole LAI, Haloperidol decanoate, Fluphenazine decanoate, Zuclopenthixol LAI, Olanzapine LAI (ZypAdhera)

---

## Conversion Methods

| Measure | Reference | Method |
|---|---|---|
| **OLZ equivalents** | Leucht et al. *Am J Psychiatry* 2020;177:342–353 | ED95-based dose-response meta-analysis |
| **CPZ equivalents** | Gardner et al. *Am J Psychiatry* 2010;167:686–693 | Classic chlorpromazine equivalence |

Factors marked with `*` in the reference table are estimates derived from Leucht et al. 2014/2016 or therapeutic dose ranges, and are flagged automatically in the output.

**LAI formula:**  
`daily_oral_eq = (total_dose_mg / interval_days) × PK_factor`  
Then converted to OLZ eq and CPZ eq using the same oral factors.

---

## Usage

1. Open `index.html` in a browser (Chrome, Firefox, Safari, Edge)
2. Click **+ Add patient** to create a new entry
3. Select drug from the dropdown → enter dose in mg/day
4. For LAI: select formulation → enter total dose (mg) + interval (days)
5. OLZ eq (green) and CPZ eq (amber) appear instantly
6. Click **Export CSV** to download all data

---

## Methods Text (for papers)

> Antipsychotic doses were converted to olanzapine equivalents (OLZ-eq) using the dose-response meta-analysis method by Leucht et al. (2020) (*Am J Psychiatry* 177:342–353). Chlorpromazine equivalents (CPZ-eq) were calculated using Gardner et al. (2010) (*Am J Psychiatry* 167:686–693). For compounds not covered by these primary references, conversion factors were estimated from Leucht et al. (2014, 2016) or therapeutic dose ranges (see Supplementary Table). For LAI formulations, doses were first converted to daily oral equivalents using published pharmacokinetic data, then converted to OLZ-eq and CPZ-eq. In polypharmacy, equivalents were summed. Cases with unknown doses were excluded from dose-related analyses.

---

## References

1. Leucht S, Crippa A, Siafis S, et al. Dose-response meta-analysis of antipsychotic drugs for acute schizophrenia. *Am J Psychiatry.* 2020;177(4):342-353.
2. Gardner DM, Murphy AL, O'Donnell H, et al. International consensus study of antipsychotic dosing. *Am J Psychiatry.* 2010;167(6):686-693.
3. Leucht S, Samara M, Heres S, et al. Dose equivalents for antipsychotic drugs: the DDD method. *Schizophr Bull.* 2016;42(S1):S90-S94.
4. Leucht S, Samara M, Heres S, et al. Dose equivalents for second-generation antipsychotics: the minimum effective dose method. *Schizophr Bull.* 2014;40(2):314-326.

---

## License

For academic and clinical research use. Please cite the original references (Leucht 2020, Gardner 2010) when using conversion factors derived from this tool.
