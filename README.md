# Hamburger, Real-Encyclopädie für Bibel und Talmud – digital edition

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.24465434.svg)](https://doi.org/10.5281/zenodo.24465434)

**English** · [Deutsch](README.de.md)

Jacob Hamburger (1826–1911), rabbi of Mecklenburg-Strelitz, wrote the first Jewish encyclopedia in German. This repository holds a transcription of the work as structured data and as DSL dictionaries:

| Part | Entries | Notes |
| --- | ---: | ---: |
| Abtheilung I, *Die biblischen Artikel* (vol. 1, 2nd ed. 1884) | 1,900 | 21,996 |
| Abtheilung II, *Die talmudischen Artikel* (vol. 2, 1883) | 853 | 15,890 |
| Supplementbände I–VI (1886–1901): Bible and Talmud; post-talmudic Judaism up to Moses Mendelssohn | 273 | 6,041 |
| **Total** | **3,026** | **43,927** |

Footnotes stay where they are in the text. Hebrew alternatives of headwords are included as extra headwords. Abbreviations are explained, references to Bible, Mishnah, Tosefta, Talmud and Midrash are resolved, and *s.* cross-references point to the article they name. The combined register (supplement vol. III) is not included.

The data were prepared for the free desktop library [Safran](https://github.com/mitkin89/Safran), where the three parts are bundled as dictionaries.

## Contents

| Path | Content |
| --- | --- |
| `data/hamburger-band-1-bibel.json`, `…-band-2-talmud.json`, `…-supplemente-1-6.json` | `{"title", "entries": [{"heads", "html", "text"}]}`; `text` is plain text with notes as `[Anm. n: …]` |
| `dsl/*.dsl` | the same as DSL dictionaries (UTF-8 with BOM); notes as `[com]⁽n⁾ …[/com]` |
| `abbreviations.json` | the abbreviations used in the markup, with their expansion |

### HTML markup

- `<div class="dl" style="margin-left:Nem">` – one paragraph of the article.
- `<sup class="dfn">n</sup><span class="dnote">…</span>` – a footnote, at the place of its number.
- `<abbr class="gab" data-t="…">` – an abbreviation with its expansion.
- `<a class="dsrc" data-sref="…">` – a reference resolved to a [Sefaria](https://www.sefaria.org)-style reference.
- `<a class="dref" data-q="…">` – a cross-reference to another article.

## Method and reliability

- The pages were transcribed with Claude (Anthropic, 2026) from page images in eScriptorium: the digitizations of the Bayerische Staatsbibliothek (vol. 1 `bsb11604377`, vol. 2 `bsb11604378`, supplement volumes) and, for supplement volumes V and VI, the Internet Archive scan of the combined supplements. Abbreviations, references and cross-references were marked by script.
- This is a working transcription, **not a critical edition**; it has not been proofread completely against the print. The Hebrew in the small footnotes of the supplement volumes has not been proofread. Please report errors as an issue, with headword.

## License

- Jacob Hamburger (†1911): the printed work is in the **public domain**.
- Transcription, structured data, DSL files and the list of abbreviations: **[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)**, see [LICENSE.md](LICENSE.md).

## Citation

Itkin, Igor Mendel (ed.): *Hamburger, Real-Encyclopädie für Bibel und Talmud – digital edition*, version 1.0.0, 2026. https://doi.org/10.5281/zenodo.24465434

See [CITATION.cff](CITATION.cff). Each release is archived on Zenodo with its own DOI.
