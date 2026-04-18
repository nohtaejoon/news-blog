# Google Analytics 4 (GA4) Setup Guide for AdSense-ready Blog

Overview:
- GA4 measurement ID is used to collect user interaction data for analysis in Google Analytics.
- For a Jekyll GitHub Pages site, add the GA4 tag snippet to the site layout (head) to enable data collection.

Steps:
1) Create or open GA4 property in Google Analytics.
2) Copy the Measurement ID (format: G-XXXXXXXXXX).
3) Update your site head (e.g., in _layouts/default.html) by inserting the GA4 tag:

<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>

4) Deploy and verify in Real-Time reports of GA4.

Notes:
- If you already use Universal Analytics (UA), GA4 is separate; you can run both in parallel during a transition period.
- Ensure you comply with privacy rules and display a privacy policy that discloses analytics usage (see Phase 2 privacy page).
