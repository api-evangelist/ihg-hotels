# IHG Hotels & Resorts

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

InterContinental Hotels Group PLC (trading as IHG Hotels & Resorts) is a British asset-light hotel group headquartered at Windsor Dials, 1 Arthur Road, Windsor, Berkshire SL4 1RS, United Kingdom, with an Americas office at 3 Ravinia Drive, Atlanta, Georgia. Its own corporate site states 7,014 hotels and 1,035,589 rooms across more than 100 countries, around 400,000 colleagues, 20 brands and the IHG One Rewards loyalty programme (figures read from ihgplc.com on 2026-07-28). The brand portfolio spans Six Senses, Regent, InterContinental, Vignette Collection, Kimpton, Hotel Indigo, voco, HUALUXE, Crowne Plaza, EVEN Hotels, Holiday Inn, Holiday Inn Express, Holiday Inn Resorts, Holiday Inn Club Vacations, Garner, avid, Atwell Suites, Staybridge Suites, Candlewood Suites, IHG Army Hotels and Iberostar Beachfront Resorts. In the distribution chain IHG sits on the supply side as a franchisor and manager rather than an owner: it aggregates independently owned and operated properties into a single central reservation system and pushes that inventory out through its own ihg.com and app direct channels, through the three GDSs and their agency terminals, through OTAs and wholesalers, and through corporate and group channels. Critically, IHG does not run its own reservation platform any more. It announced a partnership with Amadeus in 2015 to build a cloud Guest Reservation System to replace HOLIDEX, its proprietary system in service since 1965, and migrated onto it across 2018 and early 2019 — so the hotel group most likely to be a lock-in vendor is itself a customer of a GDS company's platform, and group bookings land in Amadeus Delphi and Meeting Broker. Its API posture, stated honestly, is gated and undocumented. There is no live developer portal. The one that existed — PartnerConnect RoomService at pcroomservice.ihg.com, a TIBCO Mashery portal publishing five rate, availability and hotel-content APIs — is decommissioned: the hostname is NXDOMAIN on Google, Cloudflare and Quad9 resolvers as of 2026-07-28 and the Internet Archive holds no page capture after 2019. What remains live is partnerconnect.ihg.com (HTTP 200), an affiliate marketing programme whose signup routes to Commission Junction and which still advertises "access to real-time hotel rates, availability and hotel content API's" without linking to any technical resource. Real API hostnames exist — api.ihg.com CNAMEs to ihg.api.mashery.com with an sb-ihg.mashery.com sandbox, and apis.ihg.com, b2b.ihg.com, mcp.ihg.com, booking.ihg.com and concerto.ihg.com all sit behind Akamai — but every one returns 403 Access Denied or 401 on every path probed, including /openapi.json, /swagger.json, /api-docs and /.well-known/. No OpenAPI, Swagger, AsyncAPI, GraphQL SDL, WSDL, XSD, OpenTravel/OTA or HTNG reference is published anywhere by IHG. apis[] is deliberately empty: listing an Akamai-gated hostname or a decommissioned 2017 portal as a live API would be fabrication. The value of this record is the switchingCost block in review.yml, which captures what published IHG documents actually say about what it costs to leave — including the archived RoomService Terms of Use classing "API parameters" as Confidential Information and binding partners to the Master PartnerConnect Terms and Conditions plus the Six Continents Hotels E-commerce Master Service Agreement, and the current IHG One Rewards member terms stating that members whose accounts are cancelled "by IHG or by the Member, will forfeit all Points, Point vouchers, Reward Nights, and any other benefits associated with the account".

**Areas:** Travel · United Kingdom · Hospitality · Hotels · Booking · Distribution · GDS · Loyalty · Affiliates

## IHG Hotels & Resorts on APIs.io

Everything profiled for IHG Hotels & Resorts is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/ihg-hotels/](https://apis.io/providers/ihg-hotels/)** — or go straight to one of the APIs or properties below.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Security (1)

Authentication, trust centre, and vulnerability disclosure.

- [Ihg Hotels Domain Security](https://apis.io/security/ihg-hotels/ihg-hotels-domain-security/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.ihg.com/)
- [Sign up](https://signup.cj.com/member/signup/publisher/?cid=1675692)
- [Support](https://www.ihgplc.com/en/contact-us)
- [Terms of service](https://www.ihg.com/hotels/gb/en/global/customer_care/tc)
- [Privacy policy](https://www.ihg.com/content/us/en/customer-care/privacy_statement)

## API Evangelist rating

**Kin Score 13.3** — emerging · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 50.0 |
| Contract quality | 0.0 |
| Contract governance | 0.0 |
| Operational transparency | 0.0 |
| Developer ergonomics | 4.8 |
| Access clarity | 34.2 |

**Agent readiness 0.0** — human-only

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | — |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | — |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | — |
| Rate Limit Signal | — |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 18.6** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/ihg-hotels/](https://apis.io/providers/ihg-hotels/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for IHG Hotels & Resorts: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/ihg-hotels/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
