# Reconstruction & Visualisation Skill

**Don't just reformat the material. Reconstruct the story, make it visual, and make it easy for your reader to understand.**

A [Claude Skill](https://support.claude.com/en/articles/12512180-using-skills-in-claude) that helps turn messy
documents, data, long reports and old slides into clear reports and presentations, built around what your reader
needs to understand or do.

It aims to tell a real story, use pictures and charts where they help, and stay close to what your source actually
says.

**[Install the skill](https://github.com/virapandy/reconstruction-and-visualisation-skill#install)** ·
**[See sample outputs](https://github.com/virapandy/reconstruction-and-visualisation-skill#sample-outputs)** ·
**[Download the latest version](https://github.com/virapandy/reconstruction-and-visualisation-skill/releases/latest/download/reconstruction-and-visualisation-skill.skill)**

### When to use it

It's best for the **final version** of something that matters, like a report for a board or funder, slides for an
important meeting, or anything read outside your team.

For quick notes or rough internal drafts, it's probably too much. It asks questions, waits for your go-ahead and
checks its work, and all of that takes time. For everyday notes, just ask Claude directly.

### How it works

> **You:** "Turn this report into a short deck for our board." *(and attach the report)*
>
> **Claude** asks a few questions, one at a time: who the readers are, what they already know, and what you need
> from them.
>
> **Claude** offers two ways to tell the story. **You** pick one.
>
> **Claude** shows the plan, slide by slide, and what it would leave out. **You** approve it or ask for changes.
>
> **Claude** builds the deck, looks at each slide, and checks the numbers against your report.
>
> **Claude** has the deck checked by a separate reviewer, fixes what it can, and hands it over with a short note on
> what was kept, left out or uncertain.

**What you get:** a Word report, a web page (with a PDF copy), a print-ready PDF, or a slide deck you can download as
PowerPoint or PDF.

**Who it's for:** anyone turning material into something a particular reader will use. No technical skills needed.
It works in the Claude app (web, desktop and mobile) and in Claude Code.

## Install

**In the Claude app**

1. [Download the skill file](https://github.com/virapandy/reconstruction-and-visualisation-skill/releases/latest/download/reconstruction-and-visualisation-skill.skill).
2. Go to **Settings → Capabilities → Skills**, upload it, and click **Save skill**.
3. In **Settings → Capabilities**, turn on **Code execution and file creation**. The skill uses this to check its own
   work. Without it, the skill still runs, but with fewer checks, and it tells you so.

**In Claude Code**, unzip the file into your skills folder:

```bash
mkdir -p ~/.claude/skills/reconstruction-and-visualisation-skill
unzip reconstruction-and-visualisation-skill.skill -d ~/.claude/skills/reconstruction-and-visualisation-skill
```

**Then just ask.** For example: "restructure this report for the board".

**Updating:** download the file again. In the Claude app, open the installed skill's **⋯** menu and choose
**Replace**, then start a new chat. The skill mentions it at the start of a job when a newer version is out.

## What makes it different

- **You approve the key decisions.** That means the story, the plan, and what gets left out.
- **Story first, then pictures.** It works out the main message before choosing any charts.
- **It works with your structure, too.** It can keep your structure and words, find a new shape, or fill in a set
  template. If your source can't fill a section, it says so.
- **It checks its own work.** It looks at every page it builds and checks numbers and quotes against your source.
- **It always gets a second check.** Before delivery, a separate reviewer that sees only your source and the finished
  document looks for claims stronger than the evidence. You can decline it, but the skill always asks.
- **It's open about its limits.** It says which checks are enforced and which still depend on Claude's judgement.

## Tested on real jobs

The skill has been through several rounds of testing on real jobs, across different types of output. Reviewers who
hadn't seen the work compared each document with its source, looking at:

- **Accuracy:** wrong numbers, invented content, or claims stronger than the source
- **Completeness:** whether anything important went missing
- **Clarity:** whether the story and the visuals help the reader understand
- **Format:** whether it works as a report, web page, print page or slide deck

Problems that were found have been fixed and given automated tests, so they're less likely to come back. It isn't
perfect, though: it's still worth reading the result before you share it.

## Sample outputs

These are three runs from an earlier version (v1.7.0), shown as built. Names of places, people and organisations are
replaced, and the figures are as in the sources.

**Web report:** a programme write-up, rebuilt for leaders before a strategy review.

| Opening | Evidence and timeline | Unit chart and ladder |
|---|---|---|
| ![Web report opening page](samples/digital-report-1-opening.png) | ![Evidence matrix](samples/digital-report-2-evidence-matrix.png) | ![Unit chart and ladder](samples/digital-report-3-unit-chart-and-ladder.png) |

The same report on a phone:

![Web report at phone width](samples/digital-report-4-phone.png)

**Print report:** four A4 pages from a household spreadsheet, for a district team's quarterly meeting.

![Print report, all four pages](samples/print-report-all-pages.png)

| Page 1 | Page 3 |
|---|---|
| ![Print report page 1](samples/print-report-page-1.png) | ![Print report page 3](samples/print-report-page-3.png) |

**Slide deck:** value-chain insights for a funder meeting, with one point and one picture per slide.

![All twelve slides](samples/deck-all-slides.png)

| A range chart | A unit chart |
|---|---|
| ![Slide 2](samples/deck-slide-02.png) | ![Slide 7](samples/deck-slide-07.png) |

## Feedback

At the end of a job, the skill may offer to send a short report on how the run went. It contains no content from
your documents, and you see it in full before deciding whether to send it.

- Email: feedback.rv@gmail.com
- Issues: [reconstruction-and-visualisation-skill-feedback](https://github.com/virapandy/reconstruction-and-visualisation-skill-feedback/issues)

## Licence and credits

See [LICENSE](LICENSE). Icons are from [Tabler Icons](https://tabler.io/icons) and [Health Icons](https://healthicons.org),
and the typefaces are Newsreader and IBM Plex Sans Condensed (SIL Open Font License). Full notices and credits are
inside the package, in `assets/icons/THIRD-PARTY-NOTICES.md`, `assets/kits/fonts/OFL.txt`, `assets/kits/CREDITS.md`
and `assets/exemplars/CREDITS.md`.
