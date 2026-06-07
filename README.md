# Paycheck Calculator

A standalone, browser-based paycheck estimator for hourly and salaried
employees. No installation required — open the HTML file in any browser
and it works. All data saves automatically to your browser between sessions.

Built to solve a real problem: most online paycheck calculators don't
account for the full picture — overtime, ESPP contributions, multiple
401k strategies, state-by-state tax differences, and varying pay
frequencies. This one does.

---

## Screenshot

<img width="766" height="1257" alt="Screenshot 2026-06-06 at 8 07 03 PM" src="https://github.com/user-attachments/assets/027d921d-bd8a-4d54-a198-14adf4a993be" />

---

## Features

- **Hourly and Salary modes** — single toggle switches the entire form
- **Multiple pay frequencies** — weekly, bi-weekly, twice monthly, monthly
- **Earnings breakdown** — regular, overtime (x1.5), worked holiday (x1.5),
  PTO, sick, and holiday hours
- **Federal income tax** — 2025 IRS Publication 15-T withholding tables
  with all four filing statuses (Single, MFJ, MFS, Head of Household)
- **All 50 states + Washington D.C.** — progressive bracket calculations
  with effective rate display; flat-rate and no-income-tax states handled
  automatically
- **Pre-tax deductions** — medical, dental, vision, FSA, 401k pre-tax
  contribution percentage
- **After-tax deductions** — life insurance, AD&D, 401k Roth percentage,
  ESPP (hourly mode), 401k loan repayment
- **Mega backdoor Roth** — after-tax non-Roth 401k field (salary mode)
- **Lock buttons** — lock any field to prevent accidental changes
- **Pay day calendar** — pick your two monthly pay dates for twice-monthly
  schedules, with correct day counts including leap years
- **Auto-saves** — all inputs persist in browser localStorage between
  sessions
- **No dependencies** — single HTML file, works completely offline

---

## Version History

### v4.0 — Combined Calculator [current] (`paycheck_calculator_v4_combined.html`)
Unified hourly and salary into one calculator with full pay frequency
support and mega backdoor 401k.

- Combined hourly and salary modes into a single tool with a pay type
  selector
- Added pay frequency options: Weekly, Bi-Weekly, Twice Monthly, Monthly
- Added interactive monthly calendar for Twice Monthly pay schedules,
  with accurate day counts per month including leap years
- Added 401k After-Tax percentage field for mega backdoor Roth strategies
- Unified filing status and pay frequency dropdowns across both modes

### v3.0 — Salary Mode (`paycheck_calculator_v3_salary.html`)
Standalone salary calculator built alongside the hourly version before
the two were merged.

- Annual salary input with automatic per-period gross calculation
- Replaced the fixed 401k loan label with a free-text description field
  for flexible static deduction labeling
- Added pre/after-tax toggle on the static deduction field
- Added After-Tax Non-Roth retirement contribution field
- Removed ESPP (not applicable to salaried employees)

### v2.0 — FICA + 50-State Tax Engine (`paycheck_calculator_v2.html`)
Major overhaul of deductions and tax calculations.

- Consolidated 11 individual benefit fields into two buckets:
  Pre-Tax Benefits and After-Tax Benefits
- Changed ESPP to calculate as a percentage of regular, PTO, and sick pay
- Added Worked Holiday Hours earnings row at 1.5x rate
- Added Social Security (6.2%) and Medicare (1.45%) FICA calculations
- Replaced Oregon-only flat tax with a full 50-state + D.C. bracket engine
- State tax now calculates effective rate dynamically based on annual
  gross income and filing status

### v1.0 — Initial Hourly Calculator (`paycheck_calculator_v1.html`)
First working version, converted from a React artifact into a
self-contained HTML file.

- Hourly pay with bi-weekly pay schedule
- 11 individual benefit deduction fields with per-field pre/after-tax
  toggles
- Federal income tax using Oregon bracket calculation
- Foundation for all future versions

---

## How to Use

1. Download the version you want (v4.0 recommended).
2. Open the file in any modern browser — Chrome, Firefox, Safari, or Edge.
3. No internet connection needed after download.
4. Choose your filing status, pay type, and pay frequency.
5. Enter your hourly rate or annual salary.
6. Fill in your hours worked and any applicable deductions.
7. Select your state for automatic state tax estimation.
8. Your estimated net pay updates in real time.

Your inputs save automatically in your browser. Use the lock buttons
to protect values you don't want changed accidentally.

---

## Disclaimer

Federal withholding uses 2025 IRS Publication 15-T tables. State tax
brackets reflect 2024/2025 rates shown as effective rates (tax divided
by gross income). State standard deductions and local or county taxes
such as Maryland and New York City are not applied. Social Security
wage base is $176,100. Results are estimates only — consult a tax
professional for advice specific to your situation. 
If you find an error/bug, please let me know so I can correct it! Thank you!

---

## Built With

- HTML, CSS, JavaScript
- React 18 (via CDN — no build step or installation required)
- Babel Standalone (JSX transpilation in the browser)
- Browser localStorage for data persistence

---

## A Note on How This Was Built

These calculators were built collaboratively with Claude (Anthropic's AI).
I defined the requirements, iterated on each version, tested the outputs
against real paychecks, caught and corrected calculation errors, and drove
every decision about what to build and how. Claude helped with code
generation and iteration. The problem-solving, product thinking, and
validation were mine.

I believe in being transparent about AI-assisted work.

---

## License

This project is licensed under the GNU General Public License v3.0.
See the [LICENSE](LICENSE) file for details.

Free to use and modify. If you distribute a modified version, you must
also make your source code available under the same GPL v3 license.

---

## Author

**Meagan Lapworth**
[linkedin.com/in/meagan-lapworth-smallwinz](https://www.linkedin.com/in/meagan-lapworth-smallwinz)
[github.com/MeaganLapworth](https://github.com/MeaganLapworth)
