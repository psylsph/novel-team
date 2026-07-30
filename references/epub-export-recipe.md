# EPUB Export Recipe

After all editorial stages (10-16) pass, export the manuscript to EPUB for author sign-off.

## Prerequisites

- `pandoc` installed (test with `which pandoc`)
- All chapter files in `chapters/chapter-*.md`

## Steps

### 1. Create metadata YAML

```
---
title: "Novel Title"
author: "Author"
publisher: "Self-Published"
rights: "All rights reserved"
lang: "en-GB"
subject: "Fiction, Thriller, Military"
---
```

Save to a temp file (e.g. `/tmp/epub-metadata.yaml`).

### 2. Create CSS for EPUB

Minimal serif styling:

```
body { font-family: Georgia, "Times New Roman", serif; line-height: 1.6; }
h1 { text-align: center; font-size: 1.4em; page-break-before: always; }
h1:first-of-type { page-break-before: avoid; }
p { text-indent: 1.5em; margin: 0; }
p:first-of-type { text-indent: 0; }
```

Save to `/tmp/epub-style.css`.

### 3. Combine chapters

```
cat /tmp/epub-metadata.yaml > novel-combined.md
echo "" >> novel-combined.md
for i in $(seq 1 CHAPTER_COUNT); do
  f="chapters/chapter-$(printf '%02d' $i).md"
  echo "" >> novel-combined.md
  cat "$f" >> novel-combined.md
  echo "" >> novel-combined.md
done
```

### 4. Convert to EPUB

```
pandoc novel-combined.md \
  -f markdown \
  --metadata-file=/tmp/epub-metadata.yaml \
  --toc \
  --toc-depth=1 \
  --css=/tmp/epub-style.css \
  --split-level=1 \
  -o novel.epub
```

### 5. Clean up

```
rm -f novel-combined.md
```

## Smart-quote handling

If the EPUB shows mojibake (e.g. `don't` renders as `don't`), source files have mixed curly/straight quotes. Fix before pandoc:

```
sed -i "s/\xe2\x80\x98/'/g; s/\xe2\x80\x99/'/g; s/\xe2\x80\x9c/\"/g; s/\xe2\x80\x9d/\"/g" novel-combined.md
```

Or disable pandoc's smart extension: use `-f markdown-smart` in the pandoc command.
