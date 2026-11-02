# Template: resume-ats

- **Type:** CV
- **Source extension:** .tex
- **Engine/toolchain:** pdflatex
- **Page limit:** 2 pages
- **Fonts:** Latin Modern (lmodern, a standard TeX distribution font; no bundled files)
- **Class/packages:** article (10pt, a4paper); geometry, fontenc, inputenc, lmodern, xcolor, enumitem, microtype, hyperref. All standard.

## Compile command

    cd cv && rm -f <file>.pdf && mkdir -p build && pdflatex -interaction=nonstopmode -output-directory=build <file>.tex && mv build/<file>.pdf ./

## Style rules

- The user supplied this layout (originally `documents/cv/Resume.tex`) and wants **every CV generated in exactly this format**. Do not fall back to moderncv.
- Single column, no tables or images. Header: name in uppercase blue (RGB 31,119,180), grey headline line `Title | Keyword | Keyword | Keyword`, then one contact line (phone | email | city | LinkedIn | GitHub).
- Section order: PROFESSIONAL SUMMARY, PROFESSIONAL EXPERIENCE, RESEARCH EXPERIENCE, PROJECTS (with an "Earlier Projects" list), OPEN SOURCE CONTRIBUTIONS, TECHNICAL SKILLS, CERTIFICATIONS, EDUCATION, LANGUAGES. Headings are ALL CAPS in English.
- Use only the macros `\entry`, `\project`, `\research`, `\skill`, `\minorproject`; dates sit right-aligned in each macro's last argument.
- Dates use an **ASCII hyphen** (`Aug 2021 - Aug 2024`, `2024 - Present`), not `--`: LaTeX turns `--` into an en-dash that some ATS parsers drop. This is the one deliberate deviation from the supplied file.
- Spell acronyms out once, then abbreviate. British spelling throughout.
- Tailor by reordering and trimming per the guide at the top of the skeleton. When over two pages, cut in this order: Earlier Projects, the two weakest certifications, the third bullet of each project.
- The employer name must follow `01-candidate-profile.md` ("Sprinriver Technology Private Limited"), not any variant spelling.

## Known pitfalls

- `\item` text that begins with a literal `[` must be braced (`\item {[text]}`), otherwise LaTeX treats it as an optional label.
- Escape `&`, `%`, `_`, `#` and `$` in body text (`pg\_trgm`, `100\%`).
- The `\section` command is redefined here (no numbering, rule below the heading); do not use `\section*`.
- There is no place for a per-line "in progress" note under Education. Use `YYYY - Present` as the date and state the thesis submission month in the summary.
- The compile redirects to `build/`; `/apply` Step 5e must delete `cv/build` afterwards.
