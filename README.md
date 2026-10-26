# Trufla (trufla)

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

Trufla Technology is a Calgary, Alberta insurtech that builds digital distribution software for independent property and casualty insurance brokerages, serving 300+ brokerages primarily across Canada with some UK clients. Founded in 2018 by Sherif Gemayel out of Sharp Insurance's in-house tooling (SharpMobile plus the E-Method digital agency), Trufla sells a broker-channel suite rather than underwriting risk itself. Its API posture is entirely partner-gated and inbound: there is no public developer portal and no self-serve API.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/trufla/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/trufla/refs/heads/main/apis.yml)

## Tags

- Insurance
- Canada
- Property and Casualty
- Insurtech
- Broker
- Agency Management
- CSIO
- Policy Administration
- Quote Bind Issue
- Digital Distribution

## Timestamps

- **Created:** 2026-07-25
- **Modified:** 2026-07-25

## APIs

None. Trufla publishes no public, self-serve API and no downloadable API definitions.

Every first-party developer host was probed on 2026-07-25 and none exists — `developer.trufla.com`, `developers.trufla.com`, `docs.trufla.com` and `api.trufla.com` all return NXDOMAIN at DNS. The site's full [page sitemap](https://www.trufla.com/page-sitemap.xml) (HTTP 200, 79 URLs) contains no developer, API, or documentation page. Every OpenAPI and Swagger discovery path on `www.trufla.com` returned HTTP 404, as did `/graphql`, `/.well-known/openid-configuration` and `/.well-known/oauth-authorization-server`. The only machine-readable endpoint on the domain is `/wp-json`, the WordPress REST API of the marketing CMS — incidental infrastructure, not a product API, and deliberately not listed in `apis.yml`.

See [review.yml](review.yml) for the full probe log, HTTP statuses and provenance.

## Products

- **truWeb** — broker websites, insurance marketing, SEO, content and AI plugins
- **truMarket** — insurance CRM with a Quote Bind Issue rating workflow, lead management, SMS and email marketing, a marketplace and an app store
- **truMobile** — customer self-service app and broker portal with policy management, claim reporting, document delivery automation, Clementine RPA and a marketplace for auxiliary products (travel, roadside, pet)
- **DataHub** — Policy KPI Dashboard, AI Retention X-Ray and the Data Module
- **Trudi** — AI insurance assistant spanning retention, underwriting, productivity and insights
- **PolicyPro** — contracted back-office outsourcing service

## Integration Posture

Integration is inbound and gated, the way it works across the Canadian broker channel. The truMarket app store sells subscribable connectors to broker management systems (Acturis, Power Broker, Vertafore, with Applied Epic and TAM named on the Clementine RPA page), plus Salesforce, SEH Systems, telephony, e-signature, payment processing and the Communications Centre (formerly CP360). None is documented as a callable Trufla API.

### Standards

**No ACORD reference found.** ACORD, AL3, ACORD XML, NGDS and IVANS appear nowhere on the public site. Canada's standards seam for the broker channel is **CSIO** (Centre for Study of Insurance Operations), and Trufla treats it as an onboarding service rather than an interface — the truMarket implementation process lists "CSIO Implementation: Ensuring standards compliance and efficient data exchange", and Trufla's terms of service require the brokerage client to supply its own CSIO account and mailbox along with its own "insurer contracts and APIs".

### Quote / Bind / Issue / FNOL

All four verbs exist as product features and none is exposed as an API. Quote, bind and issue are an agent-facing single-entry workflow inside truMarket; the truMobile Marketplace runs quote-to-purchase for auxiliary products consumer-facing; FNOL is claim reporting inside the truMobile self-service app.

### Auth

Not published. No OAuth or OpenID Connect discovery document is served, there is no self-serve signup, and access runs through a sales demo request into licensed broker portals.

## Links

- [Website](https://www.trufla.com/)
- [About](https://www.trufla.com/about-us/)
- [truMarket](https://www.trufla.com/products/trumarket/)
- [App Store / Integrations](https://www.trufla.com/products/trumarket/app-store/)
- [Partners](https://www.trufla.com/resources/partners/)
- [Release Notes](https://www.trufla.com/resources/release-notes/)
- [Blog](https://www.trufla.com/blogs/)
- [Request a Demo](https://www.trufla.com/request-a-demo/)
- [Terms of Service](https://www.trufla.com/legal/terms-of-service/)
- [Privacy Policy](https://www.trufla.com/legal/privacy-policy/)

## Maintainers

- Kin Lane — kin@apievangelist.com
