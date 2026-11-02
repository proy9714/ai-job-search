# Search Queries for Job Scraper

<!-- Populated by /setup on 2026-11-02 for Priyadarshi Roy. Re-run `/setup --section search` to change. -->

## Installed portal CLIs (primary for `/scrape`)

`/scrape` discovers every portal skill under `.agents/skills/*/SKILL.md` and runs its CLI first. Enabled now: `linkedin-search`, `freehire-search`. The Danish demo portals (Jobindex, Jobbank, Jobdanmark, Jobnet) stay **disabled** because Denmark is not a target market. More boards for Germany, Europe and India are to be added with `/add-portal` (see "Search Sites" below). You do **not** need a matching `site:` line below for those CLIs to run.

The `site:` query templates in this file are the **WebSearch fallback**: for portals without a CLI, company career pages, or when a CLI fails.

**Language scope:** the candidate works in **English only**. Write every query in English. Do not generate German-language query variants: a role that needs German above A2 is a FAIL under `04-job-evaluation.md`. English postings from German employers are the target.

## Hard filters to apply to every result

- **Full-time, permanent only.** Drop internships, working-student (Werkstudent), thesis, part-time, freelance and fixed-term-only postings.
- **Language:** drop postings requiring German above A2 or any non-English working language.
- **Salary floor (when stated):** EUR 60,000/year in Europe; INR 15 lakh/year in India.
- **Work permit (Europe):** drop EU-citizens-only or "no visa sponsorship" postings. Mark "sponsorship unverified" when silent. Student permit expires March 2027.

## Search Sites

Primary:
- **linkedin.com/jobs** - Europe-wide and India; covered by the `linkedin-search` CLI
- **freehire** - covered by the `freehire-search` CLI

To add with `/add-portal` (fallback to `site:` queries until then):
- **Germany / Europe:** stepstone.de, de.indeed.com, arbeitsagentur.de (Jobbörse), glassdoor.de, xing.com/jobs, eurotechjobs.com, relocate.me, englishjobs.de, berlinstartupjobs.com, euraxess.ec.europa.eu (research)
- **India:** naukri.com, instahyre.com, hirist.tech, cutshort.io, foundit.in, in.indeed.com, wellfound.com

Secondary (company career pages via Google `site:` queries) - top-paying employers:
- **Big Tech:** careers.google.com, amazon.jobs, metacareers.com, jobs.apple.com, careers.microsoft.com, nvidia.wd5.myworkdayjobs.com, jobs.netflix.com
- **AI labs and scale-ups:** deepmind.google, mistral.ai/careers, aleph-alpha.com, deepl.com/careers, huggingface.co/jobs, databricks.com/company/careers, snowflake.com/careers, uber.com/careers, booking.com/careers, zalando.com/careers
- **Industrial AI / R&D (Germany):** jobs.bosch.com, bmwgroup.jobs, jobs.sap.com, zeiss.com/careers, jobs.siemens.com, jobs.dlr.de, jobs.fraunhofer.de, careers.allianz.com
- **India high-pay:** Google, Microsoft, Amazon, Adobe, Uber, Atlassian, Salesforce, Flipkart, PhonePe, Razorpay, Swiggy (India offices)

## Query Categories

All three directions are weighted equally (candidate's choice). Combine each query with location terms: `Germany`, `Europe`, `remote`, `Berlin`, `Munich`, `Frankfurt`, `Amsterdam`, `London`, `Zurich`, `Dublin` for Europe; `India`, `Bengaluru`, `Hyderabad`, `Pune`, `Gurugram`, `Kolkata` for India.

### Priority 1: LLM / GenAI / NLP Engineering

Strongest industry experience: RAG, LLM applications, NLP.

```
site:linkedin.com/jobs "Machine Learning Engineer" LLM Germany
site:linkedin.com/jobs "AI Engineer" "RAG" Europe
site:linkedin.com/jobs "LLM Engineer" OR "GenAI Engineer" OR "Generative AI Engineer" Germany
site:linkedin.com/jobs "NLP Engineer" Europe
site:linkedin.com/jobs "Data Scientist" "Generative AI" Germany
site:stepstone.de "Machine Learning Engineer" English LLM
site:naukri.com "Machine Learning Engineer" LLM RAG Bengaluru
site:hirist.tech "GenAI Engineer" OR "LLM Engineer"
```

### Priority 1: Computer Vision / Multimodal AI

Thesis direction: vision foundation models, pose estimation, VLMs.

```
site:linkedin.com/jobs "Computer Vision Engineer" Germany
site:linkedin.com/jobs "Research Engineer" multimodal OR "vision-language" Europe
site:linkedin.com/jobs "Machine Learning Engineer" "computer vision" Europe
site:linkedin.com/jobs "Applied Scientist" "computer vision" Germany
site:stepstone.de "Computer Vision" Engineer English
site:naukri.com "Computer Vision Engineer" Bengaluru
```

### Priority 1: Applied Research

Research-heavy teams in industry and research institutes.

```
site:amazon.jobs "Applied Scientist" Germany OR Luxembourg OR Berlin
site:linkedin.com/jobs "Applied Scientist" NLP OR LLM Europe
site:linkedin.com/jobs "Research Engineer" "machine learning" Germany
site:linkedin.com/jobs "AI Research Engineer" Europe
site:euraxess.ec.europa.eu "machine learning" research engineer
site:jobs.dlr.de "Machine Learning" -Masterarbeit -Werkstudent
site:jobs.fraunhofer.de "Machine Learning" OR "KI" Engineer English
```

### Priority 2: Adjacent roles

Roles that fit the skill profile but use a different job title.

```
site:linkedin.com/jobs "AI Solutions Engineer" OR "ML Solutions Engineer" Europe
site:linkedin.com/jobs "Forward Deployed Engineer" AI Europe
site:linkedin.com/jobs "Machine Learning Engineer" "digital humanities" OR "cultural heritage"
site:linkedin.com/jobs "Data Scientist" NLP Germany
site:linkedin.com/jobs "ML Engineer" search OR retrieval Europe
```

### Priority 3: Top-paying company career pages (direct)

```
site:careers.google.com "Machine Learning" Zurich OR Munich OR Berlin OR London OR Bengaluru
site:amazon.jobs "Machine Learning Engineer" OR "Applied Scientist" Berlin OR Aachen OR Munich OR Bengaluru
site:metacareers.com "Machine Learning Engineer" London OR Zurich OR Paris
site:jobs.apple.com "Machine Learning" Munich OR Zurich OR Cambridge OR Hyderabad
site:careers.microsoft.com "Machine Learning" OR "Applied Scientist" Germany OR Dublin OR Hyderabad OR Bengaluru
site:jobs.sap.com "AI Engineer" OR "Machine Learning Engineer" -Werkstudent -Intern
site:jobs.bosch.com "Machine Learning" OR "Computer Vision" -Werkstudent -Thesis
```

### Priority 4: Broader net

```
site:linkedin.com/jobs "Machine Learning Engineer" "visa sponsorship" Europe
site:relocate.me "Machine Learning"
site:englishjobs.de "Machine Learning" OR "AI Engineer"
site:linkedin.com/jobs "Python" "Machine Learning" Engineer remote Europe
site:instahyre.com "Machine Learning Engineer"
```

## Location Filter

The candidate is open to relocating anywhere. Use these tiers to **rank**, not to exclude:
- **Ideal:** Germany (any city, including Rhine-Main / Marburg area), remote roles from Germany
- **Acceptable:** rest of the EU/EEA, Switzerland, UK (subject to the permit/sponsorship check)
- **Borderline (second priority):** India (Bengaluru, Hyderabad, Pune, Gurugram/NCR, Chennai, Mumbai, Kolkata)
- **Flag for discussion:** outside Europe and India (US, Middle East, East Asia)

## Language Filter

The candidate works in **English only** (German A2). Apply `04-job-evaluation.md`'s Language Gate together with its candidate-specific override: a posting that requires German above A2, or any other non-English language, as a job condition is **excluded**. Postings simply *written* in German for an English-working role are fine. "German is a plus" is fine.

## Date Filter

Only include jobs posted within the last 14 days, or with an application deadline that has not yet passed. If a posting date cannot be determined, include it but flag as "date unknown".

## Adapting Queries

If the user specifies a focus area, select queries from the matching category and also generate 2-3 custom queries for that focus. For example:
- "/scrape computer vision" -> Computer Vision / Multimodal queries + custom focus-specific queries
- "/scrape india" -> India sites and city terms across all categories
