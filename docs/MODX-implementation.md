# Kranghand Design — Renovatie & Verbouwing Leiden

## Prototype

`renovatie-leiden-prototype.html` is een zelfstandig visueel HTML-prototype. Het gebruikt bestaande projectafbeeldingen en links van kranghanddesign.com, maar is **niet** op de live website gepubliceerd.

## SEO-velden voor MODX + Localizator

- Nederlandse resource alias: `renovatie-leiden`
- NL URL: `https://kranghanddesign.com/nl/renovatie-leiden`
- `<title>` / `seotitle`: `Renovatie & Verbouwing Leiden | Kranghand Design`
- Meta description: `Uw woning renoveren in Leiden? Kranghand Design verzorgt complete binnenrenovaties, van interieurontwerp en materiaalselectie tot uitvoering en afwerking.`
- H1: `Renovatie & verbouwing in Leiden`
- Suggested main intent: complete indoor renovation, design-to-delivery; broader than interior styling alone.
- Organic search cluster: `renovatie Leiden`, `verbouwing Leiden`, `renovatiebedrijf Leiden`, `totaalrenovatie Leiden`, `woningrenovatie Leiden`.

## Implementation in MODX

1. Create a new resource with alias `renovatie-leiden`, use a dedicated template/chunk; publish the NL content first. Ensure routing for `/nl/renovatie-leiden` works with Localizator and consistent canonical URL/trailing slash behavior.
2. Port HTML `<main>` contents into an existing MODX template layout so the site's shared header, footer, cookie manager and analytics are not duplicated. Move the standalone `<style>` into a versioned CSS asset; remove the `preview` banner and `noindex,nofollow` from the prototype before publication.
3. Use actual project photos or their existing thumbnails; the prototype currently references live image URLs on the website. Verify responsive sizes and loading, and consider using optimized images (`srcset`, WebP/AVIF) supplied by the site.
4. Link CTA buttons to `/nl/contact` initially; for direct lead capture, integrate an actual SendIt form with server-side validation, honeypot and notifications (do not leave a fake non-functional form).
5. Add a Localizator-specific `seotitle` and a meta description field, if the latter does not already exist. Populate canonicals and hreflang only for published equivalent translations. Do not point EN/RU hreflang to a non-existent page.
6. Add `Service` JSON-LD to this resource only. The prototype contains basic Service markup; adjust provider to match current site's business entity (`@id`) and avoid contradictory address/entity IDs.
7. Add internal links in NL navigation, home, portfolio project pages and relevant blog entries. Include in sitemap.xml, verify Indexing in Google Search Console.
8. In GA4 and GTM track `renovation_cta_click` with `page_location` and referral/UTM metadata; count a conversion only after a successful SendIt submission, not just button clicks.
9. Monitor Google Search Console weekly by page and Dutch queries. Focus on impressions and qualified leads; ranking top 3 is not guaranteed and measured keyword volumes in this niche are small.

## Items that must be confirmed with Nadia before publication

- Who is the contracting party for renovation works and who takes responsibility for execution: Nadia's own company, a fixed renovation team or independent contractor contracts?
- Full service list and exclusions (structural works, plumbing, electrical work, permitting, etc.). Current draft only claims interior renovation and coordination.
- Exact service area outside Leiden, if any. No surrounding city names are claimed as operating regions in the draft.
- Whether she offers written workmanship guarantees, time commitments, fixed budgets, etc. No such claims are made in the draft.
- Whether testimonials from previous interior design customers can be presented as renovation testimonials; prototype links to honest existing review page and does not fabricate a renovation-specific quote.

## Source material reviewed

- https://kranghanddesign.com/nl/work-with-me
- https://kranghanddesign.com/nl/portfolio/river-garden-leiden
- https://kranghanddesign.com/nl/portfolio/a-hotel-chic-and-welness-villa-blended-with-nature
- https://kranghanddesign.com/nl/portfolio/maisonette-with-roof-terrace-scheveningen
- https://kranghanddesign.com/nl/reviews/
- https://kranghanddesign.com/nl/contact