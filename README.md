# Reconstruction & Visualisation Skill

**Don't just reformat the material. Reconstruct the story, make it visual, and make it easy for your reader to understand.**

A [Claude Skill](https://support.claude.com/en/articles/12512180-using-skills-in-claude) that turns messy documents,
data, long reports and old slides into clear reports and presentations, built around what your reader needs to
understand or do.

It tells a real story, picks pictures and charts that help, sticks to what your source actually says, and checks its
own work so it doesn't make things up or overstate them.

**[Install the skill](https://github.com/virapandy/reconstruction-and-visualisation-skill#install)** ·
**[See sample outputs](https://github.com/virapandy/reconstruction-and-visualisation-skill#sample-outputs)** ·
**[Download the latest version](https://github.com/virapandy/reconstruction-and-visualisation-skill/releases/latest/download/reconstruction-and-visualisation-skill.skill)**

### When to use it

Use it for the **final version** of something that matters: a report for a board or funder, slides for an important
meeting, or anything people outside your team will read.

Don't use it for quick notes or rough internal drafts. It asks you questions, waits for your go-ahead along the way,
and checks its work, which takes time. That's worth it for a final draft, but too much for everyday notes. For those,
just ask Claude directly.

### How it works

1. **You tell it about your reader:** who they are, what they already know, and what you need them to do.
2. **You pick the story.** It reads everything and offers two ways to tell it.
3. **You approve the plan:** each section, its main point and its picture, and what will be left out.
4. **It builds and checks.** It writes the document, looks at every page, and checks it against your source. Then it
   offers a second, independent check before you share it.

**What you get:** a Word report, a web page (with a PDF copy), a print-ready PDF, or a slide deck you can download as
PowerPoint or PDF. Each one comes with a short note saying what was kept, what was left out, and anything it wasn't
sure about.

**Who it's for:** anyone who needs to turn material into something a specific reader will use. You don't need any
technical skills. It works in the Claude app (web, desktop and mobile) and in Claude Code.

## Install

**In the Claude app (web, desktop or mobile)**

1. [Download the skill file](https://github.com/virapandy/reconstruction-and-visualisation-skill/releases/latest/download/reconstruction-and-visualisation-skill.skill).
2. Go to **Settings → Capabilities → Skills**, upload the file, and click **Save skill**.
3. In **Settings → Capabilities**, turn on **Code execution and file creation**. The skill uses small programs to
   check its own work. Without this setting it still runs, but with fewer checks, and it tells you so.

**In Claude Code**

The skill file is a zip. Unzip it into your skills folder:

```bash
mkdir -p ~/.claude/skills/reconstruction-and-visualisation-skill
unzip reconstruction-and-visualisation-skill.skill -d ~/.claude/skills/reconstruction-and-visualisation-skill
```

**Then just ask.** For example: "restructure this report for the board" or "turn this data into a deck for our
funders".

**Updating.** Download the file again. In the Claude app, open the installed skill's **⋯** menu and choose
**Replace**, because uploading it a second time doesn't replace the old one. Then start a **new chat**, since a chat
that was already open keeps the old version. At the start of each job, the skill tells you in one line if a newer
version is out.

## What makes it different

- **You stay in charge.** You approve the story, the plan, and what gets left out before anything is built.
- **Story first, then pictures.** It settles the main message and the order of points before choosing any chart. In
  a slide deck, every main slide makes one point with one picture.
- **Three ways to work.**
  - Keep your structure and words, and just add visuals.
  - Let it find the best shape.
  - Fit a set template, such as a funder's form.

  If your source can't fill a section, it says so rather than making something up.
- **It looks at what it built.** It checks every page, and for web reports it checks phone and laptop sizes too. It
  fixes problems before you see them.
- **It checks its facts.** Small built-in programs check its work. They stop it quoting things your source doesn't
  say, flag claims stronger than the evidence, and keep words like "may" and "suggests" when text is shortened.
- **A second opinion.** Before you share the document, it can set up a fresh check of it against your source.
- **One place to edit.** The content lives in a Claude Doc you can comment on and change. Come back later, edit it,
  and ask for an updated version.
- **Honest about its limits.** It lists which of its checks are enforced and which still rely on Claude's judgement.
  The full list is in `SKILL.md`.
- **Plain-English option.** For readers of English as a second language, it uses short sentences, one instruction per
  sentence, and keeps every "may" and "might".
- **Nothing about your work is sent anywhere else.** The only outside request is a quick check on GitHub for a newer
  version, and it sends nothing about your job. Feedback is optional, and covered under [Feedback](#feedback).

## Tested on real jobs

We ran six real jobs in Claude chat, one for each type of output, using openly licensed sources. Fresh reviewers
checked each document against its source:

- **Numbers:** about 835 claims checked, with no number errors.
- **Invented content:** none.
- **Source headings:** every one accounted for.
- **Key questions:** 5 or 6 out of 6 could be answered from each document.

Four of the six passed the accuracy check outright. The other two each had one sentence that overstated its source,
and visual polish was the weakest area. Every problem found was fixed and given a test in later versions.

## Sample outputs

These are three real runs in Claude chat, one for each main format. Each started from one source file and a one-line
request, and they're shown as built. They used an earlier version of the skill (v1.7.0). The only change is that
names of places, people, organisations and businesses are replaced (GP A–E, Buyer A, Trader B). All figures are as
in the sources.

**Web report:** a camp-by-camp programme write-up, rebuilt for programme leaders before a strategy review. The skill
broke "the camp model works" into twelve parts and showed which ones the evidence supports.

| Opening | Evidence and timeline | Unit chart and ladder |
|---|---|---|
| ![Web report opening page](samples/digital-report-1-opening.png) | ![Evidence matrix](samples/digital-report-2-evidence-matrix.png) | ![Unit chart and ladder](samples/digital-report-3-unit-chart-and-ladder.png) |

On a phone, the same report rearranges itself to fit the screen.

![Web report at phone width](samples/digital-report-4-phone.png)

**Print report:** the source was a spreadsheet described as survey data. The skill found it was really a model of one
average household. It agreed a new scope with the requester, rebuilt the model's sums, and found an improvement that
the model lists but never uses. The result is four A4 pages for a district team's quarterly meeting:

![Print report, all four pages](samples/print-report-all-pages.png)

| Page 1 | Page 3 |
|---|---|
| ![Print report page 1](samples/print-report-page-1.png) | ![Print report page 3](samples/print-report-page-3.png) |

**Slide deck:** insights on three of the eight groups in a value chain, for a funder meeting. Every main slide makes
one point with one picture. The final request to the funder is left as a marked gap for the requester to fill in.

![All twelve slides](samples/deck-all-slides.png)

| A range chart | A unit chart |
|---|---|
| ![Slide 2](samples/deck-slide-02.png) | ![Slide 7](samples/deck-slide-07.png) |

## Step by step

| Step | Who | What happens |
|---|---|---|
| 1. Questions | You | It asks about your purpose, your reader, how visual it should be, and the format you want, one question at a time. |
| 2. Two stories | Claude | It reads your whole source and writes two different ways to tell it. |
| 3. Pick the story | You | Choose one, or ask for a mix. |
| 4. Plan | Claude | It lists the main points in order, then lays out a section-by-section plan (slide by slide for a deck). |
| 5. Approve the plan | You | Approve it or change it. Changing it now is quick, but changing it after building is slow. |
| 6. Agree what's left out | You | Every heading in your source is shown as kept with a picture, kept as text, or left out. |
| 7. Write, build, look | Claude | It writes into a Claude Doc you can edit, builds the output, looks at every page, and checks it against the source. |
| 8. Final go-ahead | You | You see the finished plan and confirm before the final file is made. |
| 9. Delivered | You | You get the file, a PDF copy for web and print reports, and a short note. It asks if you want an independent check. |
| 10. Learn | Claude | It says what went well or badly and asks for your suggestions. |

Before step 1, it quietly checks once whether a newer version is out. If you come back to an earlier job, it reminds
you of the brief before carrying on.

## Feedback

At the end of a job, the skill may offer to send a short report on how the run went. The report contains only counts
and check results, plus your Python version and operating system. It has nothing from your documents, headings,
figures or answers. You see the whole report first, and nothing is sent unless you press send.

- Email: feedback.rv@gmail.com
- Issues: [reconstruction-and-visualisation-skill-feedback](https://github.com/virapandy/reconstruction-and-visualisation-skill-feedback/issues)

## Licence and credits

See [LICENSE](LICENSE). The other assets in the package carry their own licences, and their notices are inside the
package:

- **Icons:** [Tabler Icons](https://tabler.io/icons) and [Health Icons](https://healthicons.org), with notices in
  `assets/icons/THIRD-PARTY-NOTICES.md`. The `livestock-market` icons are original to this package.
- **Typefaces:** Newsreader and IBM Plex Sans Condensed, under the SIL Open Font License (`assets/kits/fonts/OFL.txt`).
- **Report parts:** their pattern sources are credited in `assets/kits/CREDITS.md`.
- **Reference pages:** sources and attribution are in `assets/exemplars/CREDITS.md`.
