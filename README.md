# CV Website: Arnau Yanes Sitjà

Hypermedia project, part 1. A single-page, static CV website built with plain **HTML + CSS**.

- **Live page (GitHub Pages):** https://arnauyanessitja.github.io/hypermedia-project-part-1/
- **Figma design (proposal):** https://www.figma.com/design/NNWYJHImvMexvQFxjEY85B/Hypermedia-Project-Part-1---Arnau-Yanes?node-id=1-2&t=ctxPkomvi28h3xLr-1

---

## 1) Project analysis

### User profile (user persona)

**Role:** Talent acquisition specialist (recruiter) at a tech company in the Girona area, looking for interns and junior profiles.  
**Goals:** Quickly decide if the candidate fits an **internship or junior** role; check what he studies and in which year; see his **work experience**; verify **languages** and **technical skills** (C++, Java, Python, HTML, CSS, JavaScript); find the **contact** details instantly.  
**Needs:** Very limited time per candidate, so she expects a **clear structure**, content that is easy to skim, and links that work.  
**Devices:** Mostly desktop/laptop; sometimes mobile.  
**Expectations:** A fast and professional page, with obvious sections (**About me**, **Experience**, **Education**, **Skills**, **Contact**), simple navigation and readable typography. Since most candidates are students with little experience, she also looks for signals such as responsibility, teamwork and languages.

---

### Information architecture

The website is a single-page project, so the information architecture is mainly about the order of the sections and how the user moves between them. The page uses semantic HTML5 elements: a `<header>` with the navigation menu, a `<main>` with all the CV sections, and a `<footer>`.

The **header** is sticky, so it stays at the top of the screen while the user scrolls. On the left it shows my name, and on the right a menu with five links: About me, Experience, Education, Skills and Contact. Each link points to the `id` of a section (`#experience`, `#skills`...), so the recruiter can jump directly to what she wants to check without scrolling through the whole page.

The **main** area follows the order of a traditional CV, ranked by importance for a recruiter:

1. **Home:** my name, a one-sentence summary (who I am, what I study, what I'm looking for), two buttons ("Contact me" and "View my GitHub") and my photo on the right. In a few seconds the user knows who I am and can put a face to the name.
2. **About me:** a short description of my personality and strengths.
3. **Experience:** split into two blocks. "Academic projects" shows what I've done at university (programming assignments, web pages and a team project with a link to GitHub), and "Professional experience" lists my summer and part-time jobs, from the most recent to the oldest. Each block has a title, a grey line with dates and place, and a short bullet list that is quick to scan.
4. **Education:** each item shows the degree in bold and, below, the school and dates in grey.
5. **Skills:** programming languages and tools as small tags, languages in a table (so the levels can be compared at a glance) and a short list of additional information (driver's licence, availability, hobbies).
6. **Contact:** my email and GitHub, so the user can act after reading.

The order goes from a quick presentation (who I am) to the evidence (experience, education, skills) and ends with an action (contact). Personal data such as my phone number and date of birth are not published, because the page is public.

---

### Visual design

I wanted a simple, clean and professional design, so that the content is the protagonist and the page is easy to scan. I took inspiration from my paper CV, which uses dark blue, and from typical one-page developer portfolios with a top menu.

**Color palette.** The main color is a deep blue (`#1F4A7A`), the same one as in my paper CV. Blue communicates seriousness and trust, which suits a recruiter and a technical profile. It's used for the header, the titles, the buttons and the table header. The page background is a very light, cool grey (`#F6F8FB`), and every second section has a light blue background (`#E4ECF5`), so the sections are clearly separated without needing lines. Text is a dark blue-grey (`#1B2430`) and secondary information, such as companies, places and dates, is in a softer grey (`#5C6B7C`). All the colors are defined as CSS variables in `:root`, so they can be changed in a single place.

**Typography.** I used **Inter** from Google Fonts for the whole page, with Arial as a fallback. It's a sans-serif typeface designed for screens and very readable at small sizes. Instead of mixing fonts, I create the hierarchy with size and weight: 44 px for my name, 26 px for section titles, 18 px bold for item titles and 16 px for body text.

**Layout.** The content is centered in a `.wrapper` with a maximum width of 1000 px, which keeps lines at a comfortable length. Flexbox is used for the header, the buttons and the skill tags; CSS Grid for the two columns of the home section (text and photo). The photo is cropped to show the face and shoulders, with slightly rounded corners. Tags and buttons also have small rounded corners and light borders to keep the interface tidy.

**Responsive.** With a media query at 800 px, the menu moves under my name and the home section becomes one column, with the photo above the name, so the page works well on a phone.

---

## 2) Design proposal using Figma

- **Frames:** desktop (1440 px).
- **Components:** header with menu, home (name, summary, buttons and photo), about me, experience block with bullet list, education item, skill tags, language table, contact, footer.
- **Styles:** the same color variables and typefaces described in the visual design section.
- **Link:** https://www.figma.com/design/NNWYJHImvMexvQFxjEY85B/Hypermedia-Project-Part-1---Arnau-Yanes?node-id=1-2&t=ctxPkomvi28h3xLr-1

---

## 3) Project implementation

- **Technologies:** plain **HTML5** (semantic structure) and **CSS3** (layout and visuals). No frameworks such as Bootstrap and no JavaScript: the page is small, and writing the layout by hand with Flexbox and Grid keeps the code short and gives full control. The only external resource is Google Fonts.
- **Files:**
  - `index.html`: page content
  - `style.css`: all the styles, in one external style sheet, organised in commented blocks
  - `img/arnau.jpg`: profile photo
- **Navigation:** internal anchors in the header menu; external links open in a new tab with `target="_blank"` and `rel="noopener"`.
- **Layout:** centered wrapper, sticky header, Flexbox (menu, buttons, tags) and CSS Grid (home section with text and photo).
- **Responsive:** one media query (800 px) that changes the menu and turns two columns into one.
