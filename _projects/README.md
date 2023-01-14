# Preparing a project profile

Check the contents of the directory `_projects` for a file with with the code of your project. 
If there already is one, you can add more information to it (see the template below and other profiles).

## If you do not have a file yet

1. Create a new file, `project-code.md` in `_projects`.
2. Copy and fill out the template below. The template has two parts: metadata and contents. 
3. Enter metadata into the template.
   You can add more than one homepage under sites (just add another line starting).
   You can delete lines with no information.
4. The contents should be in [Markdown](https://www.markdownguide.org/cheat-sheet/).
5. The fields `principal_investigators`, `pg_investigators`, and `funding` can contain Markdown. 
   If you use a link, you should put the contents of the field between double quotation marks: `"`.

## Template

```
---
title: ________________________________
url: ________________________________
sicris: ________________________________
principal_investigators:
    - PI name
pg_investigators:
    - investigator name
funding: ________________________________
start: 0000-00-00
end: 0000-00-00
---

Contents

```