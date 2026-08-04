# IHG Hotels & Resorts (ihg-hotels)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

InterContinental Hotels Group PLC (trading as IHG Hotels & Resorts) is a British asset-light hotel group headquartered at Windsor Dials, 1 Arthur Road, Windsor, Berkshire SL4 1RS, United Kingdom, with an Americas office in Atlanta, Georgia. Its own corporate site reports 7,014 hotels and 1,035,589 rooms across more than 100 countries, around 400,000 colleagues, 20 brands and the IHG One Rewards loyalty programme. In the distribution chain it sits on the supply side as a franchisor and manager, aggregating independently owned and operated properties into one central reservation system and pushing that inventory out through ihg.com and its app, the three GDSs, OTAs and wholesalers, and corporate and group channels. Its API posture, stated honestly, is gated and undocumented: there is no live developer portal, no reference documentation and no machine-readable contract of any kind.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/ihg-hotels/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/ihg-hotels/refs/heads/main/apis.yml)

## Tags

- Travel
- United Kingdom
- Hospitality
- Hotels
- Booking
- Distribution
- GDS
- Loyalty
- Affiliate
- Partner Gated

## Timestamps

- **Created:** 2026-07-28
- **Modified:** 2026-07-28

## APIs

No IHG API is publicly documented, so `apis[]` is intentionally empty.

Real IHG APIs demonstrably exist. `api.ihg.com` still CNAMEs to `ihg.api.mashery.com` with an `sb-ihg.mashery.com` sandbox in the chain — the TIBCO Mashery gateway that once fronted IHG's developer programme. `apis.ihg.com`, `b2b.ihg.com`, `mcp.ihg.com`, `booking.ihg.com` and `concerto.ihg.com` all resolve behind Akamai and return 403 or 401 on every path probed, including `/openapi.json`, `/swagger.json`, `/api-docs` and `/.well-known/`. hubli announced a live real-time group-booking API integration across 6,600+ IHG properties. None of that is documented, so none of it is listed here — publishing an Akamai-gated hostname as an API would be fabrication.

## An API programme that went backwards

This record exists mainly to document a regression.

**PartnerConnect RoomService** at `pcroomservice.ihg.com` was a genuine public developer portal, built on TIBCO Mashery. It had one-page self-registration, an API key console ("My API's") with separate staging and production keys, an I/O Docs interactive console, an API gallery, a support forum and a published *IHG Commercial API Terms of Use*. It documented five APIs by name:

| API | What it returned |
| --- | --- |
| Hotel Descriptive Info API | Hotel name, address, hotel and room amenities for one hotel, queried by hotel code |
| Single Property Availability API | Base rate without tax plus basic property information |
| Rate range (AREA availability) API | Lowest and highest rate for a city, or for one hotel |
| Hotel Search API | Name, brand code, hotel code and region code for all IHG hotels, with a timestamp delta parameter |
| Single Property Availability with Rate Rules API | Rates with tax, cancellation, commission and guarantee rules |

That portal is gone. `pcroomservice.ihg.com` is NXDOMAIN on Google, Cloudflare and Quad9 resolvers as of 2026-07-28; the Internet Archive holds page captures only through 2017. Search engines still index it and still describe it as operational — that index is stale.

What is live is [partnerconnect.ihg.com](https://partnerconnect.ihg.com/) (HTTP 200), an **affiliate marketing programme** whose signup routes to Commission Junction. It still advertises "access to real-time hotel rates, availability and hotel content API's" and links to no technical resource whatsoever.

## Distribution

IATA NDC does not apply to a hotel group. The hospitality analogues would be OpenTravel/OTA and HTNG, and IHG cites neither anywhere public.

The structural finding inverts the usual reading of hotel-group lock-in. IHG does not own its own reservation platform. It announced a partnership with **Amadeus** in 2015 to build a cloud Guest Reservation System replacing **HOLIDEX** — Holiday Inn's proprietary reservation system, in service since 1965 — and migrated onto it across 2018 and early 2019. Group and meetings bookings route into Amadeus Delphi and Meeting Broker. The hotel group most likely to be a lock-in vendor is itself a customer of a GDS company's product. The lock-in in travel does not stop at the airline; it goes all the way up.

## Switching cost

- **Interface shape:** none-published. No standard is referenced — no OpenTravel/OTA version, no HTNG specification, no OpenAPI, no WSDL, no schema of any kind. The retired API names echo OTA message shapes but no conformance claim was ever made. A partner integrating with IHG today builds against a contract with no public existence at all.
- **Second source:** alternatives-with-migration. IHG rate and availability content is resold by Amadeus, Sabre, Travelport, Expedia Rapid, the Booking.com Demand API and the bedbanks — so there are real routes to the inventory. There is no second source for IHG's own commercial terms or for IHG One Rewards accrual, which the retired join page sold as the differentiator: *"Allow your customers to earn IHG Reward Club points."*
- **Exit path:** export-on-request. Consumer-side UK/EU GDPR portability only, verbatim: *"You can ask us to provide your personal information to you in a structured, commonly used, machine-readable format, or you can ask to have it transferred directly to another data controller."* Requested through the Privacy and Cookie Center (OneTrust webforms) or `privacyoffice@ihg.com`. There is no bulk export operation and nothing at all for a partner, agency or corporate travel programme.
- **Identifier portability:** IHG-proprietary hotel code, brand code and region code, with no published mapping to GDS chain and property codes, GIATA IDs or any other shared hotel identifier. Affiliate tracking hangs on Commission Junction's CID and PID, not IHG's or the partner's. No IATA or ARC accreditation is required or referenced.
- **Contractual lock-in:** partially published. The archived *IHG Commercial API Terms of Use* bound partners to the **Master PartnerConnect Terms and Conditions** and the **Six Continents Hotels E-commerce Master Service Agreement** — both named, neither ever published — imposed **volume commitments**, classed *"API parameters"* as Confidential Information, and allowed suspension *"effective immediately"* at IHG's sole discretion. The sharpest live clause is not an API term at all: *"Members whose accounts are cancelled, by IHG or by the Member, will forfeit all Points, Point vouchers, Reward Nights, and any other benefits associated with the account."* Switching cost expressed as confiscation.
- **Access gate:** application-approval. The only published onboarding is a Commission Junction affiliate application, which IHG reviews and may *"revoke ... at any time"*. Direct commercial relationships exist but IHG publishes no form, contact, pricing or eligibility criteria — the only published route to a conversation is emailing `partnerconnect@ihg.com` with "NEW VENDOR REQUEST" in the subject line. No sandbox, no trial, no self-serve key, no published rate limits.
- **Distribution model:** gds-intermediated.

Full evidence, including every URL probed with its HTTP status and the verbatim contractual clauses, is in [`review.yml`](review.yml).

## Common Properties

- [Website](https://www.ihg.com/)
- [InterContinental Hotels Group PLC](https://www.ihgplc.com/)
- [IHG PartnerConnect affiliate marketing programme](https://partnerconnect.ihg.com/)
- [PartnerConnect frequently asked questions (PDF)](https://partnerconnect.ihg.com/wp-content/uploads/2017/04/FAQ-PartnerConnect.pdf)
- [PartnerConnect publisher signup via Commission Junction](https://signup.cj.com/member/signup/publisher/?cid=1675692)
- [IHG PartnerConnect RoomService (decommissioned Mashery portal, archived 2017)](https://web.archive.org/web/20170503133654/https://pcroomservice.ihg.com/api_description)
- [IHG Commercial API Terms of Use (archived 2015)](https://web.archive.org/web/20150926153219/https://pcroomservice.ihg.com/Terms_of_use)
- [Privacy statement](https://www.ihg.com/content/us/en/customer-care/privacy_statement)
- [IHG Privacy and Cookie Center](https://www.ihg.com/content/us/en/customer-care/privacy-and-cookie-center)
- [IHG One Rewards member terms and conditions](https://www.ihg.com/content/gb/en/customer-care/member-tc)
- [Terms of service](https://www.ihg.com/hotels/gb/en/global/customer_care/tc)
- [Brands](https://www.ihg.com/content/gb/en/about/brands)
- [IHG Agent](https://www.ihgagent.com/home)
- [Careers](https://careers.ihg.com/)
- [Investor relations](https://www.ihgplc.com/en/investors)
- [PartnerConnect new vendor requests](mailto:partnerconnect@ihg.com)
- [IHG Data Protection Officer / privacy office](mailto:privacyoffice@ihg.com)
- [LinkedIn](https://www.linkedin.com/company/ihg)

## Maintainers

- Kin Lane — kin@apievangelist.com
