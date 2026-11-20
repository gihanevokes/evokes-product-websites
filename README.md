# Evokes Pulse, Orbit & Digital Company Suite — website handoff

Updated 20 November 2026. Current design files: Pulse and Orbit meeting-fix revision; existing visual directions retained. Digital Company Suite page added (see "Digital Company Suite page" below). Evokes Compass added as the fourth product page (see "Evokes Compass page" below), and the Pulse and Orbit pages now carry their custom addresses and a Compass card in their suite sections.

## Current website addresses

- Pulse: https://pulse.evokestech.com/
- Orbit: https://orbit.evokestech.com/
- Compass: https://compass.evokestech.com/ (Root Directory `compass`)
- Digital Company Suite: https://evokessuite.vercel.app/ (Vercel project `evokessuite`, Root Directory `suite`)
- CeyDesk: https://ceydesk.evokestech.com/ (prototype; fictional data and simulated payments, so it is not linked from the product pages)

Both pages now use these owner-supplied addresses for their canonical URL, social URL metadata and links to the other product. This revision applies the scoped meeting fixes below. No production deployment was performed.

## Files and deployment

- Evokes_Pulse.html is the complete Pulse website.
- Evokes_Orbit.html is the complete Orbit website.
- compass/index.html is the complete Compass website.
- Evokes_Product_Websites.zip contains pulse/index.html, orbit/index.html and this README.

Each HTML file includes its CSS, JavaScript and exact approved SVG artwork. There are no external fonts, frameworks, image assets or build dependencies. Open either HTML file in a browser for local review.

Use pulse/index.html to update the existing Pulse project and orbit/index.html to update the existing Orbit project. Do not upload the whole combined package as one site. Keep the existing project addresses when deploying these replacements. Vercel Drop creates a new project for every drop; use your existing project's connected Git workflow or the Vercel CLI linked to that project for updates. See https://vercel.com/i/deploy-to-vercel-without-git for the current Vercel guidance.

If the project addresses or custom domains change later, update every page's cross-links and its canonical/social URL metadata together. The custom addresses pulse.evokestech.com, orbit.evokestech.com and compass.evokestech.com are now in use, and the Pulse, Orbit and Compass pages reference them in their canonical URL, social URL metadata and cross-links. The Digital Company Suite page still uses its evokessuite.vercel.app address.


## Digital Company Suite page

`suite/index.html` is the complete Digital Company Suite page: the parent page for Evokes Orbit, Evokes Pulse and CeyDesk. Deploy it as its own Vercel project with Root Directory set to `suite` and Framework Preset set to Other (no build command). Do not combine it with the Orbit or Pulse projects.

- Self-contained single file (about 450 KB): CSS, JavaScript, the Evokes glass emblem (WebP), the Orbit, Pulse and CeyDesk marks (SVG) and the fonts (Inter, matching evokestech.com, and Geist Mono for small labels; both SIL Open Font License) are embedded. No external requests, so it also works offline.
- Branding: the glass emblem with "Digital Company Suite" and a small "by Evokes" line. The Evokes wordmark is not used.
- Hero: the emblem in CSS 3D depth layers with a prism light sweep; Stock (Orbit), People (Pulse) and Business matters (CeyDesk) orbit it. Pointing at a hero word highlights that product. Reduced-motion preference is respected.
- Content decisions: CeyDesk is shown as "coming soon" with no delivery partner named. No prices are shown. Orbit and Pulse are described only with claims taken from their own pages. Each product has its own sign-in today; integration, shared sign-in and combined offers are described as confirmed in writing, never assumed.
- Product previews are labelled as illustrative sample data, reusing the Orbit and Pulse page examples.
- The enquiry form prepares an email for the visitor to review and send; nothing is submitted or stored by the page.
- Print: A4 with every preview, answer and FAQ shown; the dark theme switches to a light print layout.

Follow-ups: the Orbit and Pulse pages still present CeyDesk as available ("Discuss support"); align them with "coming soon" before the suite is shared widely. When the Suite project address is known, consider linking "Evokes Digital Company Suite" on the Orbit and Pulse pages to it.


## Evokes Compass page

`compass/index.html` is the complete Evokes Compass page: import and export management, the fourth product in the Digital Company Suite. Deploy it as its own Vercel project with Root Directory set to `compass` and Framework Preset set to Other (no build command). Do not combine it with the Orbit, Pulse or Suite projects.

- Self-contained single file (about 73 KB): CSS, JavaScript and all SVG artwork are embedded. No external fonts, frameworks, image assets, build dependencies or network requests.
- Identity: a four-point compass rose mark with a graphite palette and a brass signal colour (`#a9712a`), used for the second headline line, the active stage tab, numbers, icon tiles and ticks. Graphite (`#2b3540`) carries buttons, navigation and type. The wordmark is set in the page typeface; drawn letterforms have not been produced.
- Structure follows the Orbit and Pulse pages: logo lockup with product descriptor, pill eyebrow, two-line headline with the second line in the accent, checkmark strip, an elevated product preview card, capability cards, getting-started steps, four plan cards, the suite section, FAQs and a review-before-send enquiry.
- The product preview is a shipment cost sheet with four stages: estimate at order, Customs assessment, goods received with a late freight bill, and the approved final sheet. Per-unit landed cost moves from 7,864.00 to 8,100.00, a variance of +3.0%. Figures are illustrative and were checked for internal consistency; they quote no duty rate, levy or exchange rate.
- Content decisions: no prices. Customs filing is described as staying with the broker. Shared sign-in across the suite is described as in development, never as available. CeyDesk is shown as "coming soon" and is not linked, because the CeyDesk page is a prototype carrying fictional data and simulated payments. There is no sign-in link, because there is no Compass application yet.
- The enquiry form prepares an email to info@evokestech.com for the visitor to review and send; nothing is submitted or stored by the page.
- The suite card marks for Orbit, Pulse and CeyDesk are the approved artwork taken from the existing pages.
- Print: A4, with every costing stage and every FAQ answer shown, navigation and forms hidden, and the on-screen state restored afterwards.

Follow-ups: the Orbit and Pulse pages still present CeyDesk with "Discuss support", while the Compass page shows it as "coming soon"; align the three before the suite is shared widely. Compass sample figures should be reviewed by someone who handles shipments daily before the page is shown to a client. A trademark and domain check on the Compass name has not been carried out.

## Meeting fix list — 15 November 2026

- Matched the three affected section labels to each product's existing eyebrow style.
- Made Orbit's “A little context” field span the full form row.
- Reserved the tallest Orbit demo state at the current width using hidden sizing copies; no fixed pixel height, clipping or inner scrollbar. The sizing copies are excluded from interaction and assistive technology.
- Moved Pulse's three workflow tabs above the changing panel and clarified the prompt.
- Showed all four Pulse plans in a two-column grid (one column on mobile), retaining their wording. Opened Orbit's scope lists by default and gave every plan button equal emphasis.
- Removed visible logo replay/pause controls. Retained the short, non-looping logo entrance and reduced-motion preference.
- Fixed “an Orbit walkthrough”, replaced “Amount not shown” with “Quantity only”, and removed the awkward hero dash.
- Added a complete print workflow containing every demo step, independent of the selected tab. Print opens FAQs, shows all plans/scopes, restores the previous FAQ state afterward, hides navigation/skip links/forms/controls, and requests unbroken cards with A4 margins. Exact page count depends on the browser, fonts and print settings and has not been claimed.

Scope remains limited to meeting usability. The wider commercial/content points remain parked. Product owners must confirm current-release support for Orbit reorder reporting, supplier returns and multiple locations, and Pulse shifts, loans, settlements and CSV/text imports. CeyDesk remains described as professional services; its delivery arrangement and partner attribution require confirmation. No capability, partner, price, integration or support promise has been added.

The HTML files are the maintained sources. Older redesign scripts in temporary working folders predate these corrections and should not be used to regenerate the sites.

## Included behavior

- Pulse: modern sans-serif typography, a split hero with an interactive payroll workflow preview, an essentials grid, four visible plan cards and review-before-send enquiry.
- Orbit: white and soft-blue styling, the approved animated mark, a wide trading preview and separate displays for stock, customer balance and payment collected.
- Exact approved logo paths. Orbit completes a rotation before the small square arrives. Pulse uses a gentle arrival of the people symbol. The short logo entrance and reduced-motion support remain; visible replay/pause controls have been removed.
- Responsive navigation, keyboard-operated sample workflow tabs and expandable FAQs.
- Four subscription discussion routes: Essential, Growth, Business and Enterprise. No unapproved price, capacity limit or automatic checkout is published.
- Plan actions prefill the enquiry form. The visitor reviews the prepared email and explicitly sends it from their own email app. Copy is available as a fallback. These pages do not submit, store or collect enquiries through a backend.
- Sign-in links open the existing product applications. No credentials are embedded. The marketing pages do not provision accounts, enforce subscription entitlements or process payments.
- No analytics, cookies or third-party tracking scripts are installed.

## Sample trading logic

24 opening units + 12 received − 10 sold = 26 units remaining. A LKR 20,000 credit sale − LKR 12,000 receipt = LKR 8,000 outstanding. Payment collected is displayed separately as LKR 12,000. The payment does not reduce stock again.

The examples are clearly labelled illustrative. They are not live product screens. Receipt cost, tax, stock valuation and actual ledger posting are not modelled.

## Validation and launch decisions

Source and DOM event checks cover HTML structure, anchors, labelled fields, embedded assets, original vector geometry, minimum text-size rules, keyboard tabs, workflow arithmetic/reset, plan enquiry prefills, safe enquiry preparation, print-state restoration and ZIP contents. The meeting revision also verifies the screen/print demo states match, every plan scope remains available, and the approved logo geometry is retained.

The owner supplied a rendered UI audit. These fixes were checked in source and a DOM event harness; browser rendering and actual print pagination could not be verified in this environment. Check the updated files at 1366 × 768 on the presenting machine, on mobile, and in its A4 print preview before the meeting. Use the browser print dialog (Ctrl+P); disable browser-generated headers and footers if you do not want its URL/date/page labels.

Before public launch, confirm:

1. Published product capabilities against a tested release. Copy is based on the supplied brochures and reviewed workflow scope, not an end-to-end product acceptance test.
2. Commercial plan features, capacity, prices, billing, cancellation/refund terms and support commitments. The current pages invite a written proposal.
3. Company details, contact address/phone, and the linked privacy and terms pages.
4. Production application URLs when they replace the existing temporary-host sign-in links.
5. CeyDesk service scope and any combined offer. The pages do not promise shared login, automatic synchronisation, included professional work or a confirmed discount.
6. Product-specific social preview images and policies where required.

Subscription entitlements must be enforced by the application backend. Hiding controls in a public HTML file is not subscription enforcement.

## Research and source material

Research reviewed 14 November 2026. The layouts and copy are original; no competitor pricing or performance statistics are republished.

Pulse references:
- https://www.bamboohr.com/platform/payroll/
- https://www.personio.com/product/payroll/
- https://hr360.lk/
- https://www.zoho.com/in/payroll/

Orbit references:
- https://www.inflowinventory.com/
- https://www.sortly.com/
- https://www.zoho.com/inventory/
- https://www.getsalesguru.com/

Primary product sources:
- HR & Payroll brochure2.pdf.
- Inventory-Control-Brochure.pdf.
- Approved Evokes_Pulse_Logo_Vector.svg and Evokes_Orbit_Logo_Vector.svg.
- CeyDesk_Prototype_1.html as the standalone HTML reference.
- https://evokestech.com/ for corporate contact/identity.

## Maintenance

Each HTML file can be maintained directly in Claude Code or a text editor. Keep approved SVG path geometry unchanged. The enquiry renders user input with textContent and encodes it into a mailto URL; it does not insert user input as HTML. Never add credentials, private records or secret API keys to a public HTML file.
