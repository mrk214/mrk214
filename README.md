# Bible JSON Datasets

This GitHub profile contains a collection of **public Bible datasets in JSON format, covering multiple languages and Bible versions**. Each dataset represents a single Bible version in a single language.

These datasets were generated from publicly available HTML pages and normalized into a **[common JSON structure](https://github.com/mrk214/snapshots/blob/main/types.ts)** to make it easier to consume programmatically while preserving as much information from the original source as possible.

## 🚀 Production Snapshots

These repositories contain _production-ready snapshots_ for every available language dataset:

- 🚀 **[snapshots](https://github.com/mrk214/snapshots)** (`One JSON file per Bible version`)
- 🚀 **[snapshots-by-chapter](https://github.com/mrk214/snapshots-by-chapter)** (`One JSON file per chapter`)

Unlike the **source repositories**, the `chapter_html` field has been removed from every JSON file, and all JSON files are minified. This makes them significantly smaller and better suited for applications that only need the normalized JSON data.

If you're building an application, these are probably the repositories you want to use.

## 🧑‍💻 Source Repositories

These repositories contain the complete source datasets for each language:

- 🧑‍💻 **[bible-data-en-eng](https://github.com/mrk214/bible-data-en-eng)** (`English` 🇬🇧)
- 🧑‍💻 **[bible-data-es-spa](https://github.com/mrk214/bible-data-es-spa)** (`Spanish` 🇪🇸)
- 🧑‍💻 **[bible-data-pt-por](https://github.com/mrk214/bible-data-pt-por)** (`Portuguese` 🇵🇹)

Unlike the **production snapshots**, these repositories preserve the original `chapter_html` field for every chapter, and the JSON files remain pretty-printed with indentation for easy human reading. They are intended for development, auditing, inspecting the original HTML, and regenerating the production snapshots.

## 📚 Usage Example

Repository:

- 📚 **[reading-json-files](https://github.com/mrk214/reading-json-files)**

This repository contains a practical example showing how to read and use the JSON files.

It is **not** a library or SDK. Its only purpose is to demonstrate how the datasets can be consumed.

Since every dataset follows the same JSON schema, the examples apply to all languages and Bible versions.

---

### Which Repository Should I Use?

| If you want to...               | Repository                          |
| ------------------------------- | ----------------------------------- |
| Build an application            | `snapshots`, `snapshots-by-chapter` |
| Access the original source HTML | `bible-data-*`                      |
| Understand the JSON structure   | `reading-json-files`                |

### Notes

- All datasets share a common JSON schema across languages and Bible versions.
- Differences in formatting (paragraphs, headings, verse grouping, poetry, etc.) reflect the original source whenever possible and are not artificially standardized.
- The scraper used to generate these datasets is private. The published repositories contain the generated data only.
