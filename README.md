# Adaptive Biotechnologies

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

Adaptive Biotechnologies Corporation (Nasdaq: ADPT) is a Seattle, Washington immune-medicine
company that reads and translates the adaptive immune system at scale. Founded in 2009 by Chad
Robins and Harlan Robins as Adaptive TCR Corporation, it sequences rearranged T-cell and B-cell
receptor genes and applies computational models to turn the immune repertoire into clinical and
research data. Its lead product, **clonoSEQ**, is an FDA-cleared next-generation sequencing assay
for measurable residual disease (MRD) in multiple myeloma, B-ALL, CLL, mantle cell lymphoma and
DLBCL, run from its CLIA-certified, CAP-accredited Seattle laboratory. It also sells **immunoSEQ**
research assays with the cloud-based immunoSEQ Analyzer and the **immuneACCESS** public repertoire
data repository, and **MRD biopharma services** to drug developers.

## API surface

**Adaptive publishes no public API.** Contract discovery on 2026-09-07 probed `/openapi.json`,
`/openapi.yaml`, `/swagger.json`, `/api-docs`, `/v1/openapi.json`, `/redoc`, `/docs`, `/llms.txt`,
`/apis.json`, `/apis.yml` and the full named `/.well-known` set (security.txt, openid-configuration,
oauth-authorization-server, oauth-protected-resource, api-catalog, ai-plugin.json, ucp.json,
acp.json, aauth-resource.json, apis.json, agent-card.json, agent.json) across
`www.adaptivebiotech.com`, `adaptivebiotech.com`, `clients.adaptivebiotech.com`,
`www.clonoseq.com` and `www.immunoseq.com`. Every path returned 404 on the four honest hosts;
`www.immunoseq.com` is a catch-all that 301s everything to the corporate site, and a
negative-control path confirmed it. No GraphQL endpoint, MCP server, A2A agent card, AsyncAPI,
gRPC or WSDL was found, and neither GitHub organization bearing the company's name publishes a
single public repository.

The real integration surface is clinician-facing and delivered bilaterally: clonoSEQ orders and
results flow through Epic (including Epic Aura), Flatiron Health's OncoEMR via Molecular Profiling
Integration, and Carequality / health information exchanges — arranged through Adaptive's
integration specialists rather than through self-serve documentation, with an Epic build described
as an 8-12 week project.

## Artifacts in this profile

| Artifact | What it records |
|---|---|
| `conformance/` | Published certifications (ISO 27001, ISO 13485, MDSAP, EU IVDR, CLIA, CAP, state lab licenses, HIPAA) and the interoperability standards Adaptive does not declare |
| `security/` | Probed TLS, HSTS, DNSSEC, CAA, SPF and DMARC posture |
| `well-known/` | The `/.well-known` probe across five hosts — a measured absence |
| `packages/` | No first-party SDK in any registry; the two third-party consumers of the immunoSEQ file format |
| `plans/` | No published plans or list pricing |
| `rate-limits/` | No published limits (no API to limit) |
| `llms/` | A generated llms.txt describing this profile |

## Links

- Website: https://www.adaptivebiotech.com/
- clonoSEQ: https://www.clonoseq.com/
- clonoSEQ EMR integration: https://www.clonoseq.com/emr-integration/
- immunoSEQ Analyzer: https://clients.adaptivebiotech.com/login
- Licenses and accreditation: https://www.adaptivebiotech.com/licenses-and-accreditation/
- Blog: https://www.adaptivebiotech.com/blog/
- Investor relations: https://investors.adaptivebiotech.com/
