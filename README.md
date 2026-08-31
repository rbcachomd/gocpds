# GO-CPDS
### GynOnc Chemotherapy Protocol & Documentation System

**Version v1.3 · 31 August 2026**

A single-file, offline-capable web application for gynecologic oncology chemotherapy units.
Open `index.html` in any browser. There is no installation, no server, and no database.

---

> ## ⚠ Not approved for clinical use
>
> The clinical content in this repository is a **draft prepared for departmental review**. It has not been
> endorsed by any Section of Gynecologic Oncology or Pharmacy and Therapeutics Committee.
>
> **Do not use it to treat a patient until it has been reviewed, amended for your institution's formulary, and
> signed off.** Every protocol sheet and order sheet in the application carries this statement.
>
> Doses, thresholds, supportive-care agents, and empirical antibiotics must be reconciled with the local
> formulary and antibiogram. Every prescription and order remains the personal responsibility of the signing
> physician.

---

## What it does

**Protocols** — the departmental chemotherapy reference: regimen sheets with administration sequences, dose
modification tables, toxicity management pathways, and an emetogenic risk matrix.

**Order sheets** — printable pre-printed physician orders in BC Cancer PPPO format, one per regimen, plus a
paclitaxel desensitisation record and a drug availability and verification record.

**Documentation** — take-home prescription, pre-cycle laboratory request, bilingual patient discharge
instructions (English and Tagalog), and a dose computation worksheet.

**Calculator** — body surface area, Cockcroft–Gault creatinine clearance, CKD-EPI 2021 eGFR, and dosing for
carboplatin by Calvert, taxanes, platinums, gemcitabine, etoposide, bleomycin by cumulative unit dose,
bevacizumab per kilogram, and flat-dosed pembrolizumab.

**Fourteen regimens** across ovarian, endometrial, cervical, germ cell, and uterine sarcoma indications.

---

## Privacy

**No patient data is stored or transmitted.** Everything typed into the application lives in browser memory and
is erased when the tab closes. There is no server, no database, no cookies, and no analytics. The printed copy
is the record.

The QR code encodes a link to the general instruction page for a regimen only — no name, no chart number, no
personal data.

Consistent with RA 10173, the Philippine Data Privacy Act of 2012, no personal health information is processed
off-device.

### Two rules for anyone maintaining this repository

1. **Never commit patient details into the file.** Type them into the running application.
2. The access code in `ACCESS_HASH` is a **workflow control, not a security control**. In a public repository it
   is readable by anyone. It separates roles and supports accountability; it does not protect data, and must not
   be represented as a technical safeguard in a privacy impact assessment or audit.

---

## Setting up

Full instructions accompany the application:

| Document | Covers |
|---|---|
| `HOSTING-QUICKSTART.md` | GitHub Pages setup, workstation configuration, troubleshooting |
| `DEPLOYMENT-INSTRUCTIONS.md` | Laptop, single workstation, and multi-site rollout with version control |
| `DEPLOYMENT-AND-GOVERNANCE.md` | Privacy position, module documentation, ISO document control, go-live checklist |
| `CLINICAL-REVIEW-PACK.md` | Sign-off pack for the Section, P&T Committee, and unit pharmacist |

**Before first use:** change the access code. Open the application, click *Set up — change the access code*, and
follow the two steps it shows.

---

## Version control

Every screen and every printed document carries the version stamp. **Increment `APP_VERSION` and `APP_DATE`
whenever the clinical content changes**, and announce the new version to every unit — a stale copy on a
workstation is otherwise undetectable.

Protocol sheets instruct the reader to check that stamp and stop if it does not match the version notified by
the Quality Management Representative.

---

## Clinical references

Content is drawn from ASCO and NCCN antiemesis guidance, the ASCO immune-related adverse event guideline,
ESMO–EONS extravasation guidance, MASCC/ESMO chemoradiotherapy antiemesis recommendations, and the published
trials underlying the embedded regimens — including PORTEC-3, INTERLACE, JGOG 3016, ICON8, SOLO-1, SOLO-2,
PAOLA-1, and AGO-OVAR.

**Institutional protocols, formulary, and antibiogram take precedence over anything stated here.**

---

*Format of the order sheets is modelled on the BC Cancer Provincial Preprinted Order. Clinical content is
departmental and requires local approval before use.*
