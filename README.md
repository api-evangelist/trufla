# Trufla (trufla)

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
