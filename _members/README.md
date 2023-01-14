# Preparing a member profile

Check the contents of the directory `_members` for a file with your name. 
If there already is one, you can add more information to it (see the template below and other profiles).

## If you do not have a file yet

1. Create a new file, `name-surname.md` in `_members`.
   It is probably a good idea to change the non-ASCII characters to their ASCII counterparts (`čšž` to `csz`).
2. Copy and fill out the template below. The template has two parts: metadata and contents. 
3. Enter metadata into the template.
   You can add more than one homepage under sites (just add another line starting).
   You can delete lines with no information.
4. The contents should be in [Markdown](https://www.markdownguide.org/cheat-sheet/).

## Template

```
---
name: Name
family_name: Family Name
orcid_id: 0000-0000-0000-0000
genealogy: 000000
sites: 
    - url
links:
    mr_id: 00000
    dblp: 00/000
    sicris: 0000
    google_scholar: ____________
    scopus: 00000000000
    cobiss: cobiss+search+string
    wikipedia: wikipedia+page+name
    academia_europaea: ____________
    ias: ____________
---

Contents

```

## Finding the various IDs

* ORCID iD: this is the 16-digit id in the form `0000-0000-0000-0000`,
* COBISS: look up your bibliography on [COBISS](https://plus.cobiss.net/cobiss/si/en/bib/search) and copy the value of `q` (bolded) in the URL: `https://plus.cobiss.net/cobiss/si/en/bib/search?q=`**`000000000000`**.

For the following platforms, find the relevant entry. The ID is the bolded part of the URL in the corresponding item in the list below (the number of digits might not be the same as the number of zeroes).

* [The Mathematics Genealogy Project](https://www.mathgenealogy.org/search.php): `https://www.mathgenealogy.org/id.php?id=`**`000000`**,
* MR Author ID (MathSciNet): `https://www.ams.org/mathscinet/search/author.html?mrauthid=`**`000000`**,
* [DBLP](https://dblp.org): `https://dblp.uni-trier.de/pid/`**`00/000`**,
* [SICRIS](https://cris.cobiss.net/ecris/si/en): find the `Researcher's code` or `Šifra raziskovalca`,
* [Google Scholar](https://scholar.google.com): `https://scholar.google.com/citations?user=`**`000000000000`**.
* [Scopus](https://www.scopus.com/freelookup/form/author.uri): `https://www.scopus.com/authid/detail.uri?authorId=`**`00000000000`**