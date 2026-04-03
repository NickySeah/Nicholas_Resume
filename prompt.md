Please review my entire main.tex file and perform a code cleanup with a strong focus on ATS readability, concise formatting, and clean styling. Follow these strict guidelines:

1. Single-Page Constraint (CRITICAL): The final resume MUST fit perfectly on a single page. Adjust vertical spacing (e.g., `\vspace`, list `itemsep`, `parsep`, or geometry margins) carefully to ensure there is no spillover onto a second page, without making the text look cramped.

2. Section Header Styling: Every section header (e.g., Education, Experience, Technologies, Projects) must have a horizontal line extending across the page immediately below the text. Use the `titlesec` package and the `\titleformat` command (with `\titlerule`) to apply this globally to all `\section{}` commands.

3. ATS Optimization: Ensure the document structure guarantees linear text extraction (left-to-right, top-to-bottom).
   * Remove any ATS-breaking environments such as `paracol`, `minipage`, floating text boxes (e.g., `eso-pic`), or overly complex nested tables. Replace them with standard, linear text flow or simple, flat `tabularx` environments.
   * Ensure standard section headers use the standard `\section{}` command so parsers can correctly categorize my information.
   * Do NOT remove packages essential for machine readability and font encoding (e.g., `glyphtounicode`, `cmap`, `fontenc`, `inputenc`, `lmodern`, `charter`, and `hyperref`).

4. Identify and Remove Unused Packages: Analyze the preamble and remove any \usepackage declarations that are not actively used in the document body.

5. Format and Indent: Reformat the code so it is highly readable. Apply consistent standard indentation (typically 4 spaces) for all nested environments (e.g., `\begin{document}`, `\begin{tabularx}`, `\begin{highlights}`). Group the remaining \usepackage declarations logically.

6. Preserve Content: Do not change any of my actual resume text, metrics, job titles, or bullet points. Your goal is only to clean the underlying code to be ATS-friendly, visually polished, and developer-readable.

Output the full, cleaned LaTeX code and replace my current file.

---

Please review my entire main.tex file and adjust the vertical spacing to make it visually balanced and human-readable, while strictly maintaining the 1-page limit and ATS readability. 

Currently, the text is squeezed too tightly at the top, leaving too much empty space at the bottom. Fix this by applying the following layout rules:

1. Even Vertical Distribution: Utilize the empty space at the bottom by adding "breathing room" between sections and items.
   * Increase the `\vspace` slightly before and after each `\section{}`.
   * Increase the `itemsep` and `parsep` slightly within the `\begin{highlights}` (itemize) environments so the bullet points aren't cramped.
   * Ensure the geometry margins (top, bottom, left, right) are standard and not overly narrow (e.g., around 0.75 inches or 2 cm).

2. Single-Page Constraint: The document MUST still fit exactly on one page, but it should comfortably fill that page from top to bottom. Do not use `\vfill` in a way that creates unnatural gaps.

3. Maintain ATS & Styling:
   * Keep the linear text flow and `tabularx` structures (no `paracol` or floating boxes).
   * Keep the `titlesec` horizontal lines under each section header.
   * Keep all ATS-essential packages (`glyphtounicode`, etc.).

4. Preserve Content: Do not alter any of my actual resume text, metrics, job titles, or bullet points. 

Output the full, revised LaTeX code so I can replace my current file.

---

Please review the `\section{Experience}` and `\section{Projects}` in my main.tex file. I need you to rewrite the bullet points under each role/project to be highly professional, realistic, and scannable. Follow these strict rules:

1. Remove Fluff & Hyperbole: Eliminate exaggerated or unrealistic metrics (e.g., "100% alignment", "100% efficiency"). Replace them with grounded, realistic descriptions of the actual technical impact or business value delivered.

2. Apply Resume Best Practices: Structure each bullet point using the XYZ formula (Accomplished [X] as measured by [Y], by doing [Z]). Start every bullet with a strong, past-tense action verb (e.g., Architected, Engineered, Modernized). Keep each point concise, ideally 1 to 2 lines maximum.

3. Condense Weak Points (Summarize): If you determine that a specific project or experience entry lacks sufficient technical depth or verifiable metrics to support multiple strong XYZ bullet points, do NOT invent details or stretch the truth. Instead, summarize the core contribution and primary technologies used into just 1 or 2 concise, impactful bullet points.

4. Strategic Bolding: Use the `\textbf{}` command to bold the most critical keywords in each bullet point. Focus on bolding specific technologies (e.g., `\textbf{AWS Amplify}`, `\textbf{RabbitMQ}`) and realistic metrics (e.g., `\textbf{reduced onboarding time by 20\%}`). Do NOT bold entire sentences or over-bold; stick to 1-3 key phrases per bullet.

5. Preserve LaTeX Structure: Output the rewritten sections in valid LaTeX, maintaining the exact same itemize/highlights environments currently used in the file. Do not alter the dates, job titles, or company names.

Output the revised LaTeX code for the Experience and Projects sections and replace the current file

---

Act as a Senior Technical Recruiter and Engineering Manager evaluating undergraduate resumes for competitive Software Engineering internships. Please review the entirety of my main.tex file and provide a comprehensive critique followed by code revisions.

Step 1: The Evaluation (Text Output)
Provide a blunt, professional assessment of my resume's content:
* Rating: Give it a score out of 10 based on how competitive it is for a backend/full-stack SWE internship.
* Things Done Well: List 3 to 4 specific aspects of the resume that are exceptionally strong (e.g., specific metrics, project architectures, technology choices).
* Room for Improvement: List areas that are weak. Look for passive verbs, vague descriptions, repetitive sentence structures, or project points that lack depth or business context.

Step 2: The Execution (Code Output)
After providing your evaluation, output the revised LaTeX code implementing your suggested improvements. Adhere strictly to these rules:
* Maintain ATS & Format: Do not change the underlying LaTeX structure, custom environments, or ATS-friendly preamble we have established. The resume must remain on one page.
* Enhance, Don't Fabricate: Improve the phrasing using the XYZ formula (Accomplished X as measured by Y, by doing Z) and strong action verbs. Do not invent fake metrics, fake tools, or stretch the truth.
* Strategic Bolding: Ensure key technologies (e.g., AWS, RabbitMQ) and metrics are bolded for scannability, but do not over-bold.

Please provide the evaluation first, followed by the fully updated LaTeX code blocks for the sections you improved.

---
Yes, please do one more pass focused strictly on the XYZ pattern. 

Since I do not want any fabricated numbers, if quantitative data (like percentages or hours saved) is not naturally available for a point, please use strong qualitative metrics for the [Y] component (e.g., "ensuring zero-trust access," "eliminating manual data entry," "achieving 99.9% eventual consistency," or "improving cross-team release confidence").

Keep the strategic bolding on the key technologies and outcomes, and ensure the phrasing sounds like a mature, mid-level engineer rather than a junior listing tasks. 

Please output the final revised LaTeX code for the Experience and Projects sections so I can apply the updates.

---
Please generate a professional `README.md` for this repository. This repo contains my ATS-friendly software engineering resume written in LaTeX, along with a GitHub Actions CI/CD pipeline that automatically compiles the PDF on every push.

Please structure the README with the following sections:
1. Title & Description: A clean title (e.g., "Nicholas Seah - Software Engineering Resume") and a brief explanation of the repo's purpose and automation.
2. 🚀 Latest Release (Download): Clear instructions for a recruiter or visitor on how to download the most recently compiled PDF from the GitHub Actions "Artifacts" tab. 
3. 🛠️ Local Development Setup: Step-by-step instructions on how to compile the resume locally. Include prerequisites (VS Code, LaTeX Workshop extension, MiKTeX/MacTeX, and Strawberry Perl for latexmk).
4. ⚙️ CI/CD Pipeline: A brief explanation of how the GitHub Action (`build-resume.yml`) works under the hood to compile the LaTeX code using Ubuntu and upload the artifact.
5. 📄 License/Usage: A brief note stating that others are welcome to use the LaTeX structure/format as a template, but should remove my personal data.

Format the output in clean, standard Markdown using appropriate headers, bullet points, and code blocks for terminal commands.