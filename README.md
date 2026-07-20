# evilolive's Tools

A small collection of standalone tools, calculators, and references, built as a static [Jekyll](https://jekyllrb.com/) site and hosted on GitHub Pages. Not limited to any one category — new tools get grouped under whatever `category` fits.

**Live site:** https://evilolive420.github.io

## Tools

- **[Sawtooth Graph Calculator](https://evilolive420.github.io/sawtooth-graph-calculator.html)** — Compare two transmissions on an RPM vs Speed sawtooth chart, with tire size, rear-end ratio, and powerband highlighting.
- **[FlowCurve](https://evilolive420.github.io/flow-curve.html)** — Smooth or interpolate pasted MAF calibration data (Voltage/Frequency vs Airflow) using Whittaker-Eilers smoothing or PCHIP interpolation with custom resampling.
- **[Shot Group Analyzer](https://evilolive420.github.io/shot-group-analysis.html)** — Mark bullet holes on a target photo to compute group size, mean radius, MOA/MRAD, and point-of-impact offset, with optional manual perspective correction.

## Local development

```sh
bundle install
bundle exec jekyll serve
```

Then visit `http://localhost:4000`.

## Adding a new tool

The tool list on the homepage is data-driven, not hand-maintained. To add a new tool:

1. Create a new page at the repo root with front matter like:
   ```yaml
   ---
   layout: default
   title: Your Tool Name
   wide: true
   category: motorsports
   description: A short one-line description shown on the tool page itself.
   tags: [some, relevant, tags]
   ---
   {% include back-to-index.html %}
   {% include page-header.html %}
   ```
2. Add a matching entry to `_data/tools.yml` (`title`, `url`, `description`, `category`, `tags`).

No other files need editing — the homepage and per-page header render automatically from these.

## Support

If these tools saved you some time:

[![Buy Me a Coffee](https://img.shields.io/badge/-Buy%20me%20a%20coffee-ffdd00?logo=buy-me-a-coffee&logoColor=black)](https://www.buymeacoffee.com/evilolive420)
