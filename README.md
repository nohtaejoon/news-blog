# Automated Content Update Workflow

This repository hosts a Jekyll-based blog (Minima theme) on GitHub Pages. Phase 5 adds a manual content-automation workflow to help keep trending content fresh and SEO-friendly while preparing for GA4 analytics.

Workflow overview:
- Check trending keywords via Google Alerts (documented below).
- Create new posts in the _posts/ directory using the format: YYYY-MM-DD-title.md
- Ensure each new post includes proper frontmatter (layout, title, date, category, tags, description, image).
- Apply SEO hygiene: include multi-paragraph content (1,500+ characters), clear headings (H2/H3), and image placeholders.
- Publish via git add -> commit -> push, ensuring the site builds on GitHub Pages.

SEO and indexing considerations:
- Ensure sitemap.xml and robots.txt are present and accurate.
- Update Google Search Console if needed after publishing.

If you need to tweak the workflow, update this README and related docs accordingly.
