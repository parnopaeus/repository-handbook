<a name="top"></a>
# Preservation

### Introduction

This section may help familiarize the terms **digital preservation** and **digital curation**. Together, digital preservation and digital curation are future-focused efforts that encompass the digital lifecycle within a repository framework.

It is important to define digital **preservation** for the purposes of this document, since the term is used variously. "Digital preservation is a formal endeavor to ensure that digital information of continuing value remains accessible and usable. It involves planning, resource allocation, and application of preservation methods and technologies, and it combines policies, strategies and actions to ensure access to reformatted and "born-digital" content, regardless of the challenges of media failure and technological change" (Wikipedia, https://en.wikipedia.org/wiki/Digital_preservation). Digital preservation differs from backup, which although useful, does not anticipate problems of media deterioration or obsolescence, or file format obsolescence, nor do they introduce strategies to detect and protect against spurious or accidental unwanted changes. Nor do backup copies or mirror sites ensure adequate description of content (including technical and administrative metadata) in the way that preservation policies do. Finally, backups do not entail procedural planning over the long-term, as digital preservation does. Repository managers who are unfamiliar with the subject of digital preservation may be well served by the tutorial Digital Preservation Management: Implementing Short-term strategies for Long-term Problems.

In addition to digital preservation, **digital curation** is another helpful concept. "Digital curation is the selection, preservation, maintenance, collection and archiving of digital assets. Digital curation establishes, maintains and adds value to repositories of digital data for present and future use" (Wikipedia, https://en.wikipedia.org/wiki/Digital_curation). Our physical collections benefit from the curatorial efforts of selectors, archivists, and other specialists who are well acquainted with the scholarly significance of the collection. Likewise, decisions regarding the content of digital repositories should benefit from curatorial efforts, especially at key decision points that could affect the way material is presented digitally (migration to a new platform, user interface changes, the addition of new features, de-duplication, etc.).

#### Contents of this section

  * [Getting started](#getting-started)
  * [Mitigating external threats](#mitigating-external-threats)
  * [Content integrity and authenticity](#content-integrity-and-authenticity)
  * [Obsolescence planning](#obsolescence-planning)
  * [Minimum metadata requirements](#minimum-metadata-requirements)
  * [Essential documentation: Rights](#essential-documentation-rights)
  * [Essential documentation: Accessibility and review](#essential-documentation-accessibility-and-review)

### Getting started

Digital preservation and digital curation are focused on content and keeping content available over time, not necessarily on the technical form that houses the content. Digital preservation relies in part on actions that occur before content is in a preservation environment, so understanding how you are collecting content will inform what is necessary and practical to expect from these pre-ingest environments. When thinking about preservation and curation, think about planning for 15+ years down the road, not 3-5. Consider what could happen in that span of time: platform migrations, catastrophic system failures, changes in access of content, retirement of key personnel with institutional memory, inter-institutional efforts, changes in institutional support, evolution in collecting focus. Digital preservation also includes preserving and maintaining documentation that articulates standards used over time and the arrangement of content itself. The documentation may or may not be stored externally to the system housing the content.

If you need help with the review and preservation and curation planning for the content of your repository, please contact cul-digpres@cornell.edu for assistance.

[Return to top](#top)

### Mitigating external threats

**Do you have a strategy in place to mitigate external threats to the content in your repository?**

Preservation over time includes planning for risks that may threaten the health of your repository. These threats may include inadequate staffing, loss of institutional knowledge that is undocumented, economic threats (budget cuts), and system failures.

- [ ] Identify and document potential external threats to your repository.
- [ ] Evaluate likelihood of threats and extent of risk.
- [ ] Develop a plan to mitigate the risks.
- [ ] Review and evaluate architectural design of your repository for preservation capability (see infrastructure principles). This will inform basic strategy for preservation.
- [ ] Review institutional preservation commitment to assets and metadata. This will inform as to appropriate level of resources assigned for preservation.

[Return to top](#top)

### Content integrity and authenticity

**Are you ensuring integrity and authenticity of digital content?**

Preserving digital content requires a level of trust that users discovering the content access objects that are authentic and have integrity. Authentic objects are those that are what they claim to be (e.g. a dissertation is actually Jane Coriander's dissertation). Evidence of authenticity is documentation around who submitted or ingested the content and verification that metadata describes the right object ingested. Integrity means the object accessed is the same as the object when it was put into the repository. Evidence of integrity is often a checksum created when the object is ingested that can be verified on access.

- [ ] Create checksums for all content ingested into repository and store the value.
- [ ] Recompute and verify checksums against a stored value on a scheduled basis to look for changes to the content.
- [ ] Consider allowing users accessing content to also access the checksums to verify integrity of object.
- [ ] Review content collected passively to ensure object submitted is what submitter described and intended to submit.

[Return to top](#top)

### Obsolescence planning

**Do you have a strategic way to mitigate risk of file format obsolescence?**

If not, develop key policy and enforce by technical means if possible.

- [ ] Develop a policy on accepted or recommended file formats that have greater likelihood of enduring into the future.
      * Note that the collection style of your repository and the actual content you hope to collect may dictate the level risk that you deem "acceptable". In general, active collection of content may allow for more control over formats. In tension with this, some content may only be available in riskier formats.
      * Example: eCommons has a policy of recommended file formats that it makes available to depositors. Note that the chart is subdivided into basic content types, and gives a basic risk level for each format type. This chart is periodically reviewed for the inclusion of new formats.
- [ ] Normalize deposited files to a standard format likely to be persistent.
      * Example: arXiv employs the strategy above to accept a constrained list of file formats, and in addition converts the articles submitted to PDF's. Even though the original submissions are of a variety of formats, this normalized version, the PDF, is a uniform derivative with a high probability of longevity. arXiv mitigates risk of obsolescence, by keeping both the original formats and the normalized derivative.

[Return to top](#top)

### Minimum metadata requirements

**Do you have minimum metadata necessary to support long-term preservation management?**

Establish a set of minimum metadata required for deposited content, and ensure that all deposited content meets this standard. "Preservation metadata" can be understood as an amalgam of other types of metadata: descriptive, administrative, structural and technical. These metadata types can be kept in one schema, such as PREMIS, or they can be kept separately in various components of the repository system. Consistent and well-documented metadata supports preservation curation activities over the long-term (15+ years).

- [ ] Review and document where metadata is stored in repository. (Partner with Metadata Services to ensure uniform and thorough review.)
- [ ] Establish policy for minimum metadata on deposit. (Partner with Metadata Services to ensure completeness.)
- [ ] Use standard, open metadata schemas where possible.
- [ ] Ensure that all schemas in use are fully and externally documented, in an open, preservable format.
- [ ] Determine which constrained vocabulary(ies) are applicable to the content being collected
- [ ] Determine if metadata minimums and standards are enforceable technologically.
- [ ] Maintain documentation of changes to metadata minimums and standards over time. Use open and preservable formats.

[Return to top](#top)

### Essential documentation: Rights
**Do you have documented rights in place to facilitate legal obligations of creating multiple preservation copies and format changes over time?**

Digital preservation always requires creating multiple copies and may may require format normalization over time. Intellectual property law and specialized donor agreements makes the legality of file format migration and creating multiple copies for preservation murky unless permission is explicitly given. Ensure that your rights management strategy ensures that the curator of the content will have the right to appropriately preserve the digital content.

Contact copyright@cornell.edu to obtain guidance.

- [ ] Create a standard agreement for content depositors to transfer rights to the content that allow curator or repository staff to perform preservation activities.
- [ ] Decide who is on the hook for vetting or defining rights that are transferred.

[Return to top](#top)

### Essential documentation: Accessibility and review

**Is essential documentation of your repository appropriately available and accessible?**

All forms of documentation should exist outside your repository, and the availability of documentation affects a wide variety of stakeholders. This strategy will allow the referencing of important information by developers in the case of failure of the repository system. It can also allow for more effective participation of users when submitting content, and can assist in managing expectations about collecting scope and delivery mechanisms.

- [ ] Store these types of documentation outside the repository
        * Manifests for repository content covering both data and metadata
        * Schema and data arrangement
        * Defined roles and representatives , decision making processes, technical infrastructure, policies
- [ ] Review all documentation periodically and keep it updated
- [ ] Clearly record where documentation is kept, and record access credentials where needed for future repository managers.
- [ ] Review where documentation is kept over time with an eye toward resilience over time.
- [ ] Turn all preservation decisions and strategies into a plain-language document for curators, content creators, and users to clearly establish expectations.
- [ ] Refer to the Policy and documentation section of this handbook

[Return to top](#top)

[Return to home](index.md)
