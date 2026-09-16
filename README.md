# corneliaschneider.github.io

Personal academic homepage of Prof. Dr. Cornelia Schneider (FAU Erlangen-Nürnberg).
Plain HTML and CSS, no build step, no JavaScript, no external services.

## Putting it online (GitHub Pages)

The site is plain HTML, CSS and one small JavaScript file. There is nothing to
build or install: GitHub serves the files exactly as they are.

**1. GitHub account.** Your account name decides the address. For
`https://corneliaschneider.github.io/` the account must be named
**corneliaschneider**. If your account has a different name, the free address is
`https://<your-account-name>.github.io/` instead.

**2. New repository.** github.com → "+" (top right) → *New repository*.

- Repository name: `corneliaschneider.github.io` (exactly your account name +
  `.github.io`, all lower case)
- Visibility: **Public** (GitHub Pages is free only for public repositories)
- Do **not** tick "Add a README file"; this folder already has one
- *Create repository*

**3. Upload the files.** On the empty repository page choose
*uploading an existing file*. Unzip the folder on your computer first, open it,
select **everything inside it** (not the folder itself) and drag the selection
into the browser window. Subfolders (`assets/`, `assets/figures/`, `files/`) come
along automatically. Then write a short message such as "initial version" and
press *Commit changes*.

The uploader ignores hidden files, so `.nojekyll` will probably not be included.
That is fine here: it only matters for file names starting with an underscore,
and this site has none.

**4. Switch on Pages.** Repository → *Settings* → *Pages* →
Source: "Deploy from a branch", Branch: `main`, Folder: `/ (root)` → *Save*.

**5. Wait about a minute**, then open `https://corneliaschneider.github.io/`.
The first build can take two or three minutes. Under *Actions* you can watch it
run; a green tick means the site is live.

### Changing something later

Open the file in the repository, click the pencil icon, edit, *Commit changes*.
The live site updates within a minute. To replace a file (for example a new CV),
use *Add file → Upload files* and upload it under the same name; GitHub replaces
the old one.

### If the page looks unstyled

Then `assets/styles.css` did not arrive, usually because the folder was dragged
in instead of its contents, so the files ended up one level too deep. The
repository root must show `index.html`, not a folder containing it.

## Files

```
index.html          About / home page, research overview, Birkhäuser note, contact
research.html       Research projects A–F
publications.html   Book, submitted work, 40 articles, theses
teaching.html       Courses, supervised PhD/Master/Bachelor theses
cv.html             Career, grants, awards, service, languages + CV downloads
assets/
  styles.css                    all styling; colours are variables at the top
  portrait.jpg                  portrait, cropped from your CV photo
  portrait-square.jpg           square crop (currently unused, kept as spare)
  research-overview.png         your research diagram (used on the research page)
  research-overview.svg         the earlier version of the diagram
  research-overview-toned.svg   same diagram in the site colours (see below)
  research-overview-redrawn.svg redrawn version in the site colours
  blackboard.jpg                your blackboard photograph (teaching banner)
  book-cover.jpg                cover of your Springer book (publications page)
  figures/project-a.png         figures beside the research projects A, B, C, E, F
files/
  Schneider_CV.pdf         your CV (the only CV linked from the site)
```

To publish a new version of the CV, replace `files/Schneider_CV.pdf` with the new
file under the same name. Nothing in the HTML has to change.

## Things to replace or adjust

**Research diagram colours.** The site currently uses your original figure
(blue circles, red centre). If you prefer it in the site colours, change
`assets/research-overview.svg` to `assets/research-overview-toned.svg` in
`index.html` and `research.html`.

**Colours in general.** Everything is controlled by the variables at the top of
`assets/styles.css` (`--bg`, `--accent`, …). Changing `--accent` restyles the
whole site.

## Adding a news section later

The site deliberately has no news section. If you want one later, the simplest
form is a `news.html` built from the same page skeleton plus a nav entry in each
of the five HTML files.
