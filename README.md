# HEO-Cu Experiment Planner

A small, offline-capable web tool built around the Cu-loading series in
*Tailoring copper content in high-entropy oxides for enhanced water oxidation catalysis*
(Mehrabi-Kalajahi et al., Scientific Reports 16, 20035, 2026,
[doi:10.1038/s41598-026-50442-0](https://doi.org/10.1038/s41598-026-50442-0)).

**Live page:** https://todos125m.github.io/heo-cu-planner/
It is one self-contained HTML file (about 240 KB, no external requests, English and Persian), so it also works from a downloaded copy.

> **Independent project.** Not made by, endorsed by or affiliated with the authors of the paper.
> It is a prototype for discussion, not a research result.

## What it does

| Tab | What it does |
|---|---|
| **Plan** | Fits a Gaussian-process trend through the five measurements of the paper (overpotential, Tafel slope, Rct, steady current), shows a 95 % band and suggests the next Cu loading. Lets you add your own points and replicates. |
| **Analyze LSV** | Paste a two-column linear sweep, choose reference electrode, pH, area and Ru, and get overpotential and Tafel slope. |
| **Related papers** | A table comparing the measurement conditions of the source paper with four related spinel-oxide OER papers (KOH concentration, scan rate, iR correction, replicates, Cdl), and a reading list. |
| **Simulate** | (a) a virtual experiment built from the paper's numbers and its Tables S1 to S3; (b) a physics model of one sweep showing how scan rate, capacitance, uncompensated resistance and iR correction change the reported overpotential and Tafel slope; (c) configurational entropy against Cu; (d) a Monte Carlo estimate of how many replicates are needed to tell two loadings apart. |

## Limits you should know about

- All numbers come from **one sample per Cu loading** (five points). Outputs are a guide for choosing experiments, not predictions.
- The LSV analyzer was checked on a synthetic curve with a known answer, **not on laboratory data**.
- In the measurement model the paper's overpotential and Tafel slope are taken as the sample's kinetics. The double-layer capacitance (5 mF/cm²) is an assumption; the paper gives none.
- The Nyquist plot has one time constant. The paper mentions two, but its Table S3 lists one CPE.
- The abstract of the paper lists the overpotentials in a different order from the body text; this tool follows the body text (252 mV at 40 % Cu).
- Configurational entropy counts all cations together and uses a conventional 1.5R limit that comes from alloys.
- The comparison table was read from the full texts of open-access papers; two RSC papers could not be opened and the supplements were not read. Check numbers against the originals before using them.

## Data sources

- Paper values: the article and its supplementary tables S1 to S3 (the paper is CC BY-NC-ND 4.0). Only numbers are used; no figures are reproduced.
- Related papers: linked inside the tool.
- Font for the Persian interface: Vazirmatn (SIL Open Font License), embedded.

## Run locally

Open `index.html` in any modern browser. Nothing to install.

## License

Code: MIT (see `LICENSE`). Paper data and the embedded font keep their own licenses.

---

## توضیح فارسی

ابزاری کوچک و مستقل (یک فایل HTML، بدون درخواست خارجی، فارسی و انگلیسی) بر پایه‌ی سری بارگذاری Cu در مقاله‌ی بالا.
**آدرس:** https://todos125m.github.io/heo-cu-planner/

بخش‌ها: برنامه‌ریز آزمایش بعدی (فرایند گاوسی)، تحلیل LSV (اضافه‌ولتاژ و شیب تافل)، مقایسه‌ی شرایط اندازه‌گیری با مقاله‌های مرتبط، و شبیه‌سازی (آزمایش مجازی، اثر روش اندازه‌گیری، آنتروپی پیکربندی، تعداد تکرار لازم).

**محدودیت‌ها:** همه‌ی عددها از یک نمونه‌ی تکی برای هر Cu است و راهنما هستند نه پیش‌بینی؛ تحلیل‌گر LSV با داده‌ی آزمایشگاهی واقعی آزموده نشده؛ ظرفیت لایه‌ی دوگانه (۵ mF/cm²) یک فرض است؛ این پروژه ارتباطی با نویسندگان مقاله ندارد.
