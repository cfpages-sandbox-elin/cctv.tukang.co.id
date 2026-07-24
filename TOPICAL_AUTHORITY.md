# Topical Authority — cctv.tukang.co.id

## Role and boundary

cctv.tukang.co.id should become a practical Indonesian-language decision and operating guide for people planning, buying, installing, securing, accepting, and maintaining CCTV systems. Editorial pages support the site's commercial service, brand, and location routes; they do not reproduce “jual/pasang CCTV + kota” pages, create thin brand-review variants, promise outcomes, or replace advice from qualified electrical, networking, cybersecurity, privacy, legal, structural, or work-at-height specialists.

Every technical, safety, legal, performance, compatibility, certification, warranty, price, or product claim is an evidence gate. Authors must verify it against current Indonesian rules and regulator guidance where applicable, manufacturer documentation for the exact model and firmware, project calculations, site conditions, and test results. If evidence is unavailable, label the point as a question to verify rather than a fact.

## Context used

- `sitemap-complete.xml` is the primary inventory: 3,764 unique URLs.
- The inventory contains 3,537 geographic sales/installation URLs under `/kota/`, 206 `/kota/page/` pagination URLs, 13 brand routes, seven core routes, and one author archive.
- Core routes include `/`, `/home`, `/about`, `/services`, `/contact`, `/merek`, and `/kota`; they retain navigational or commercial intent.
- Existing brand routes cover Ezviz, Infinity, Hilook, Glenz, Dahua, ZKTeco, Panasonic, Honey, Uniview, Omniview, Hikvision, SPC, and Samsung. Editorial briefs may teach readers how to assess documented specifications but must not duplicate these brand landing pages.
- Homepage service/product labels—IP camera, HDCVI camera, PTZ camera, DVR/XVR, NVR, and display/control—helped define the vocabulary. Promotional claims such as free installation, lowest price, ready stock, nationwide shipping, or a three-year warranty were not accepted as evidence.
- No substantive editorial corpus was found in the sitemap, so the map emphasizes foundational coverage and explicit intent separation.

## Ignored template noise

Geographic keyword swaps, pagination, author/archive pages, repeated navigation/footer copy, duplicated metadata, and repeated location-template bodies were excluded from topic discovery. Location names are attributes of service availability, not separate editorial topics. Commercial brand pages remain destinations for product browsing; they are not evidence for model-level performance or compatibility.

## Topical map

| Topic ID | Parent topic | Reader outcome | Boundary | Article target |
|---|---|---|---|---:|
| CCT-01 | Security planning and project brief | Define the problem, stakeholders, constraints, and evidence needed before requesting a CCTV design or quotation. | Planning inputs only; excludes camera placement design in CCT-03 and quote evaluation in CCT-16. | 6 |
| CCT-02 | Camera and system fundamentals | Understand camera families, recorder relationships, and the specification language needed to shortlist a system. | Category education only; excludes scene-quality engineering in CCT-04 and brand landing-page intent. | 6 |
| CCT-03 | Coverage and placement | Translate security objectives into scenes, viewpoints, and blind-spot controls. | Spatial coverage only; excludes mounting execution in CCT-11 and detailed image-performance settings in CCT-04. | 6 |
| CCT-04 | Image quality and optics | Judge whether a proposed camera and configuration can produce useful images in the target scene. | Imaging performance only; excludes retention/storage sizing in CCT-05 and generic camera-category comparisons in CCT-02. | 6 |
| CCT-05 | Recording, storage, and retention | Size and evaluate recorders, storage, retention, redundancy, playback, and export. | Recording lifecycle only; excludes network transport in CCT-06 and privacy policy decisions in CCT-10. | 6 |
| CCT-06 | Network architecture and PoE | Plan CCTV connectivity, addressing, bandwidth, time, segmentation, and network-delivered power. | Data network and PoE only; excludes mains/UPS protection in CCT-07 and account hardening in CCT-09. | 6 |
| CCT-07 | Electrical power and resilience | Identify load, backup, voltage, surge, grounding, and electrical-safety questions requiring verification. | Electrical supply and resilience only; excludes data cabling in CCT-08 and physical mounting in CCT-11. | 6 |
| CCT-08 | Cabling and pathways | Choose, route, terminate, label, protect, and test signal cabling and pathways. | Passive transport infrastructure only; excludes active network design in CCT-06 and mains electrical work in CCT-07. | 6 |
| CCT-09 | CCTV cybersecurity | Reduce unauthorized access and insecure remote connectivity across the device lifecycle. | Digital security controls only; excludes privacy governance in CCT-10 and general network capacity in CCT-06. | 6 |
| CCT-10 | Privacy, legality, and governance | Establish a verifiable lawful purpose, proportionate coverage, access rules, retention, and disclosure process. | Governance and current-law verification only; excludes cybersecurity implementation in CCT-09 and incident export technique in CCT-18. | 6 |
| CCT-11 | Installation and mounting | Prepare safe, durable mounting and weatherproofing work and verify onsite aiming. | Physical installation execution only; excludes coverage design in CCT-03 and commissioning evidence in CCT-12. | 6 |
| CCT-12 | Commissioning and acceptance | Test the installed system against documented requirements before sign-off. | Acceptance testing only; excludes routine maintenance in CCT-15 and initial design in CCT-01. | 6 |
| CCT-13 | Monitoring, alerts, and integration | Design usable monitoring, alert-response, display, analytics, and integration workflows. | Operational monitoring only; excludes recorder retention in CCT-05 and privacy authorization in CCT-10. | 6 |
| CCT-14 | Deployment contexts | Adapt a common planning method to distinct premises and operating environments. | Context-specific requirements only; never creates geographic doorway pages or substitutes for detailed technical topics. | 6 |
| CCT-15 | Maintenance and troubleshooting | Maintain image availability, diagnose faults systematically, and decide when repair or replacement is justified. | Post-handover upkeep only; excludes initial commissioning in CCT-12 and procurement in CCT-16. | 6 |
| CCT-16 | Procurement and quotation | Build a comparable request, evaluate evidence, understand price drivers, and control scope changes. | Buying process only; excludes thin brand rankings and commercial brand/service landing pages. | 6 |
| CCT-17 | Standards, competence, and documentation | Verify which standards, certificates, installer capabilities, and project records actually apply. | Evidence and conformity management only; no unsupported certification or compliance claims and no legal advice. | 6 |
| CCT-18 | Handover, warranty, and incidents | Take control of the system, understand warranty conditions, preserve incident material, and close the data lifecycle. | Ownership transition and exceptional events only; excludes routine acceptance tests in CCT-12 and routine maintenance in CCT-15. | 6 |

## Internal-link rule

Each article links first to its parent topic hub and to the two or three sibling guides needed for the reader's next decision. Cross-topic links follow the work sequence: CCT-01 planning → CCT-03/CCT-04 design → CCT-05–CCT-11 implementation controls → CCT-12 acceptance → CCT-13/CCT-15/CCT-18 operation. Procurement pages may link to `/services/` or `/merek/` only when the reader is ready to compare a service or product; brand mentions link to the existing brand route instead of spawning duplicate editorial pages. No article should link to location pages merely to vary anchor text.

## First publication wave

Publish these 14 foundations first: `CCT-01-01`, `CCT-01-04`, `CCT-02-01`, `CCT-03-01`, `CCT-03-02`, `CCT-04-06`, `CCT-05-03`, `CCT-06-03`, `CCT-09-01`, `CCT-10-04`, `CCT-12-01`, `CCT-15-03`, `CCT-16-01`, and `CCT-18-01`. Together they move a reader from a defensible brief through design and evidence checks to secure ownership, while creating hubs that later articles can support.
