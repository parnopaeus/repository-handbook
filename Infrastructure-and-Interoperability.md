<a name="top"> </a>
# Introduction
The infrastructure (servers, software, and practices) that support a repository are the unseen foundation of the repository service; this foundation is the "building" in which the content is housed. When everything is going well, nobody is aware of the infrastructure, people visit the house and interact with the contents to get what they need. When something goes wrong, everyone is painfully aware of it, and interaction with the content can be hampered or lost. Repository managers are not expected to be technically accomplished, but do need to have a basic working knowledge of the architectural design of their repository, so that they can choose an architecture that best fits the needs of their uses, and assist with "home repairs" at times when they are needed. Partnering with IT, services providers and/or vendors is inevitable, especially as the service is affected by tool selection, architectural and cost constraints, and unanticipated events. The grasp of the repository manager of the basic challenges and constraints of architectures and technical solutions will directly impact success in communicating with the IT support provider who maintains the system.

The repository manager is the appropriate representative of the service to the user community, whether that be in times of service stability (regarding features and usability), service change (regarding migrations and new features) or service events (like unexpected outages). The repository manager will need to be able to communicate these events effectively to the user community so that technical staff can maintain focus on the support of the technological system(s) in play.

This document can help repository managers as they contemplate designing a new repository, or in response to significant changes in the repository they run. Events such as these may trigger review:

* Recurrent or catastrophic failures of components that support the repository service.
* A large architectural overhaul of a technological component of the repository
* Commercial changes affecting repository components, such as a major acquisition
* Staffing changes inside your repository team; loss of a team member with specialized, necessary skills.
* Loss of funding to support staffing levels, contracts, or systems.
* Note that in the case of extreme changes in the categories above, the repository manager may want to contemplate leveraging their exit plan.

### Contents in this section

* [Infrastructure](#infrastructure)
* [Implementation decisions](#implementation-decisions)
* [Technical constraints](#technical-constraints)
* [Integration](#integration)

## Infrastructure
There are a range of options for in-sourcing and out-sourcing of repository infrastructure. Each option on the continuum offers a different level of control, and a different type of direct responsibility.

* An in-sourced solution allows the greatest amount of local control and opportunity for customization of the functionality and for the security of assets and metadata housed in the repository, but it also requires the greatest commitment of staffing resources. There is also the risk of developing technical debt if sufficient staffing isn't allocated to maintaining the infrastructure.
* When considering an out-sourced solution, the repository manager must ensure issues are addressed at a contractual level as there is less direct control over the infrastructure environment. A fully out-sourced solution minimizes the burden of maintenance, but adds the risks associated with loss of control. Outsourced solutions face threats associated with acquisitions, which include loss of control of features and interface design, and even the loss of control for various uses of the content and metadata in the repository.
* Infrastructure is often a combination of in-sourced and out-sourced components. Mixed models of support are acceptable, common, and may meet your needs best.

**Definition of service**

Complete the Service planning and Defining scope sections of this handbook to assure that you have a scope for your repository. A review of your repository policies may also be helpful, since the architecture should support them. Then consider the additional topics below.

**Features**

Properly scoped features can support the needs of the repository's users, and contain costs through the prevention of scope creep.

- [ ] Undertake a systematic analysis of user needs for features for the anticipated content of your repository.
- [ ] Rank the features in terms of their priority (must have immediately, nice but can defer for a time, nice but not essential). Explicitly identify what features will NOT be developed (these are out of scope)
- [ ] Use the findings as input to determine appropriate architectures. See "Integrations" at the foot of this document for some special considerations regarding some features that can be provided through other large-scale services.

**Cost tolerance**

Explore the costs and offerings of the investment of resources, and characterize those resources. Remember that costs need to be reviewed periodically, as financial needs and budgetary support can change.

- [ ] Identify what portions of your infrastructure will be out-sourced
   * Does out-sourced infrastructure exist that meets the needs of your user community of focus?
   * Is funding available for outsourcing? How much? Consider staff effort for
     * system design
     * system implementation
     * ongoing support
    * Outsourcing requires a point person for vendor contact, including escalating bugs that are discovered, service issues, and desires for new features. Determine who will serve in this role.
- [ ] Identify what portions of your infrastructure should be in-sourced
  * Does in-sourced infrastructure exist that meets the needs of your user community of focus?
  * Is staff effort available for the support of these components? How much? Consider system implementation and ongoing costs for support services.
  * Coordination will be required across departments within your organization. Determine who will perform this function.
- [ ] If your infrastructure utilizes in-sourced and out-sourced components, draw a diagram to express how the components fit together, the flow of data, and area of responsibility for support and funding. This can bring clarity to missing pieces of the overall infrastructure.

**Level of service**

What level of expectation will you promise to meet for your end users? This affects decisions regarding Monitoring/Availability/Performance.

- [ ] Determine what kind of alerts will you require to alert you or IT minders to the health of the system
- [ ] Make a threat matrix that describes what are the threats to your services, user tolerance for the loss of those services, the likelihood of loss, and likely time required to restore them to better inform your plans for restoration of services.
- [ ] Explore the support plan for each component of your service and determine if the restoration plan aligns with the information in the matrix created above.

[Return to top](#top)

## Implementation decisions
In this context, "Implementation" is intended to describe the choices associated with assembling the infrastructure components to support the repository service, not the act of system implementation itself.

**Service continuity planning** lays the foundation of keeping the service running according to acceptable parameters of availability.

- [ ] Use the threat matrix created above to plan for outages and events
- [ ] Document plans and share with appropriate stakeholders
- [ ] Review and update plans periodically

**Lifecycle planning** devises plans for keeping the architecture up to date, in good condition, and reasonably secure. It keeps on top of developments that can be beneficial for user communities.

- [ ] Monitor development roadmaps for suitable architectures
- [ ] Participate in user communities, forums, and membership calls.
- [ ] Periodically evaluate responsiveness of support for infrastructure components; adjust if it lacks alignment with identified repository needs.
- [ ] Develop an Exit plan; see "Exit planning" in the Service planning section of this handbook.

**Change management** creates templates for how to introduce service changes to users.

- [ ] Think through possible untoward effects of upgrades and system changes, and make plans for rollback, and identify appropriate points for rollback decisions.
- [ ] Document change plans
- [ ] Consider implementing a formal change management process.
- [ ] Develop testing protocol for the repository components in use. Testing is ideally automated, but can also be manual. If manual, use of standardized scripts is encouraged.

**Operations support** makes sure the effort to support the system and its service is aligned with its needs.

- [ ] Expect problems identified through service continuity planning and staff for them.
- [ ] Evaluate stack requirements carefully (examples: linux distro, hydra stack, java requirements)
  - [ ] Ensure that the components fit within the landscape of the mainstream of supported systems
  - [ ] Ensure that staff possess the proper technical skills/get relevant training
  - [ ] Ensure that components work well together

[Return to top](#top)

## Technical constraints
These are not standalone items, but integrated into all components of the infrastructure. They should be reviewed periodically to ensure that the institutional needs are being met.

**Backups**

Backups of a repository can protect against a few different types of risk. The primary situations to cover are disaster recovery and undesired content changes (either due to accidental changes, or malicious activity by outside entities). Sometimes a single backup solution will cover both of those scenarios, and sometimes a different approach is needed to protect against different risks.

Either way, it is critical to backup both data and metadata in ways that they can be restored coherently with respect to each other. The application components also will need to be either restored from backup or reliably rebuilt in a disaster scenario. Backups are not preservation.

- [ ] Review backup strategy periodically to assure it aligns with needs.
- [ ] Run periodic tests of backup to assure data can be appropriately recovered within the time specified in recovery plans.

**Security**

There was a time when security could be considered secondary priority for library resources that were designed to be made available to the public. However, due to the change in the security threat landscape, that is no longer the case. Those responsible for repository services need to attend to basic security principles to protect:

  * **Data Integrity:** Steps must be taken to ensure that the content hosted by the institution has not been altered.
  * **Reputation:** If a system hosted by the institution is compromised and is used as a launch point for further attacks or for visibly malicious activity, the institutional reputation suffers.
  * **Protection of Intellectual property/subscription services:** Where copyrighted materials are hosted with restricted access, those restrictions must be protected

- [ ] Identify your security liaison.
- [ ] Keep systems up to date with patches and appropriate configurations
- [ ] Request a regular security review that covers all components of repository infrastructure
  - [ ] Ask the Library Security Liaison for help.

[Return to top](#top)

## Integration
A single repository architecture rarely provides for all the needs of a specific user community or set of assets. For this reason, integration with other technical architectures may be desired. Considerations for several commonly found integration areas are listed below.

**Discovery** can be accomplished by indexing repository contents and then searching in a local interface, but this has the effect of silo-ing the assets within the repository alone. There are a couple of common methods to open up the silo and make the resources discoverable from outside the repository:

  * Allow for crawling by indexers (ex: Google)
  * Make index of resources available to other discovery layers.
  * Consider the use of a handles to allow for stable URLs for resources. (Can assist in exit strategies should that become necessary.)

**Extract, Transform, Load (ETL).** These processes coordinate lifecycle management and complex workflows where repositories and metadata stores are linked serially or recursively. For instance, metadata may be created in one system, but must be populated to another as the system of record. (ex: Voyager migration to Archivespace) Likewise metadata from one system might be used to augment a second system (ex: Scholars and Symplectic Elements). ETL differs from migration in that it is periodic, and keeps live systems in synchrony. ETL processes can affect data and metadata alike; preservation systems often employ periodic, automated extracts of both data and metadata from live repository sites for preservation purposes.

**Authentication/Authorization.** A repository often has the ability to authorize access based on user affiliation, or to grant/limit access by community affiliation. This can be accomplished by local accounts on the system, but it usually makes sense to integrate with other campus wide identity provisioning systems, especially if affiliations in that system can be re-purposed in the repository. Significant economies of scale in terms of administration support through this type of integration. ex: Shibboleth

[Return to top](#top)
