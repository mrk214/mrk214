# Bible JSON Datasets

This GitHub profile hosts a collection of public **[Bible datasets in JSON format](https://mrk214.github.io/snapshots/data.json)**, covering multiple languages and Bible versions.

The data was generated from publicly available HTML pages and normalized into a **[common JSON structure](https://github.com/mrk214/reading-json-files/blob/main/src/types.ts)** to make it easier to consume programmatically while preserving as much information from the original source as possible.

## 🧑‍💻 Source Datasets

These repositories contain the complete datasets for each language:

- 🇬🇧 **[bible-data-en-eng](https://github.com/mrk214/bible-data-en-eng)** (`English`)
- 🇪🇸 **[bible-data-es-spa](https://github.com/mrk214/bible-data-es-spa)** (`Spanish`)
- 🇵🇹 **[bible-data-pt-por](https://github.com/mrk214/bible-data-pt-por)** (`Portuguese`)

Each repository contains one or more Bible versions sharing the same JSON schema.

In addition to the normalized JSON data, these repositories also preserve the original HTML for every chapter (`chapter_html`). This allows anyone to audit the source, inspect the original markup, or regenerate the dataset if needed.

These repositories should be considered the **source of truth** for the project.

## 🚀 Production Snapshots

Repository:

- 🚀 **[snapshots](https://github.com/mrk214/snapshots)**

This repository contains production-ready copies of every dataset.

The only difference from the source datasets is that the `chapter_html` field has been removed, making the files significantly smaller and more suitable for applications that only need the normalized JSON data.

If you're building an application, this is probably the repository you want to use.

## 📚 Usage Example

Repository:

- 📚 **[reading-json-files](https://github.com/mrk214/reading-json-files)**

This repository contains a practical example showing how to read and use the JSON files.

It is **not** a library or SDK. Its only purpose is to demonstrate how the datasets can be consumed.

Since every dataset follows the same JSON schema, the examples apply to all languages and Bible versions.

---

### Which Repository Should I Use?

| If you want to...               | Repository           |
| ------------------------------- | -------------------- |
| Build an application            | `snapshots`          |
| Access the original source HTML | `bible-data-*`       |
| Learn the JSON structure        | `reading-json-files` |

### Notes

- All datasets share a common JSON schema across languages and Bible versions.
- Differences in formatting (paragraphs, headings, verse grouping, poetry, etc.) reflect the original source whenever possible and are not artificially standardized.
- The scraper used to generate these datasets is private. The published repositories contain the generated data only.
