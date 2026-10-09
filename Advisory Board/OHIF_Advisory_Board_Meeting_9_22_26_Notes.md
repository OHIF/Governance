# OHIF Advisory Board – Meeting Notes

**Date:** September 22, 2026

**Advisory Board:** Simon Doran (Institute of Cancer Research), Andrey Fedorov (Brigham and Women's Hospital / Imaging Data Commons), Mohannad Hussain (Techie Maestro), Salim Kanoun (Pixilib), Steve Pieper (Isomics / 3D Slicer), Osman Ratib (OSIRIX Foundation), Denny Spiegelberg (FU Berlin), Benoit Tricot (Flywheel)

**OHIF Steering Committee:** Gordon Harris, Rob Lewis, Alireza Sedghi, Bill Wallace, Scott Morley, James Hanks

**OHIF Team:** Dan Rukas

## Updates Presented

**Funding:**

- R03 grant, year 2 of 2. Covers FHIRcast (released in 3.13), DCMJS 1.0 modernization (targeting 3.14), and dedicated test coverage.
- ITCR U24 sustainment grant, year 4 of 5.
- ITCR set-aside collaboration with FU Berlin.
- Proposals submitted to OS4LS (with IDC) and as a collaborator on a 3D Slicer proposal.

**Responses to prior feedback:**

- Updated testing contributor guidelines and an AI skill for standardized test contributions.
- Work underway on modernizing the broader contributor workflow and PR velocity.
- Internal planning on rebranding and marketing OHIF as a foundation.
- Two extensibility PRs: one merged, one in progress to simplify extension and mode creation.

**OHIF 3.14 (planned for later this year):**

- Tablet mode prototype.
- Test coverage target of ~60% by year end, toward the 80% goal.
- React 19 upgrade and codec updates.
- DCMJS 1.0 beta.

**Discussion framing:** The ITCR U24 renewal proposal is due next June. ITCR program leadership asked that it address three areas:

1. Forward-looking innovations for the community.
2. A clearly defined AI strategy.
3. A sustainment plan for OHIF beyond ITCR funding.

The board was asked for input on all three.

## 1. Communication & Transparency

**Discussion**

- Board members could not find the new testing skill and contributor guidelines mentioned in the update.
- IDC's developer had not been aware of recent PRs that responded to board feedback, one of which was already merged. Earlier notice would let board members review and take part in the work before it is integrated. *(Andrey Fedorov)*
  - James agreed and noted that an announcement of the testing skill was planned once it had been refined.

**Suggestions**

- When development is prioritized in response to board feedback, notify the board with links to the relevant PRs so members can review and participate. *(Andrey Fedorov)*
- Share links to the testing contributor guidelines and AI testing skill with the board. *(Andrey Fedorov, Benoit Tricot)*

## 2. AI-Assisted Development

**Discussion**

- AI coding has substantially changed how development is approached in 3D Slicer. Steve asked whether OHIF has seen the same shift. *(Steve Pieper)*
  - Bill confirmed it has. Tests are much easier to generate but can be over-generated, so the testing skill now favors image comparisons only where they make sense. PRs also increasingly include behavioral and user-facing specifications.
- AI token costs per developer are rising quickly. The long-term cost trajectory is uncertain, and demand for human expertise may return. *(Denny Spiegelberg)*
- Some open-source projects, such as pydicom, have stopped accepting PRs because they receive more AI-generated submissions than they can review. This dynamic needs close attention. *(Steve Pieper)*
  - Rob noted that documenting requirements and architecture gives AI-assisted work a framework to operate within. That investment is valuable however development evolves.

**Suggestions**

- Extend the AI skills approach beyond testing to other areas of contribution. *(Andrey Fedorov)*
  - James noted the team is looking at this, particularly to keep good PRs from stalling in review.
- Monitor AI-generated PR volume and review burden, and plan contribution processes so review capacity isn't overwhelmed. *(Steve Pieper)*

## 3. Forward-Looking Innovations & AI in Imaging

**Discussion**

- **AI in the viewer, not just in coding.** OHIF sits at the point of interaction between physicians and AI. It can define how clinicians use, edit, reject, and stay in control of AI results. *(Salim Kanoun)*
- **Aim higher.** AI tooling removes much of the traditional heavy lifting, such as working with DICOM by hand. That frees capacity for harder, higher-value work like niche, high-end, and scientific imaging applications. *(Steve Pieper)*
- **Where does the viewer go in 5 years?** Simon asked whether OHIF will always be only a viewer, or whether it will move toward integrated capabilities such as vision-language models. His group has done related work in this area. *(Simon Doran)*
  - Bill noted the team is actively considering this, but evidence that vision AI improves radiologist efficiency is mixed outside repetitive tasks. Any integration must be a real enhancement, not AI for its own sake.
  - Rob elaborated that the viewer is where human eyes meet the data. Enhancements could draw on aggregated data, context, and clinical decision support.
- **Plain-language image content.** LLMs could summarize what a study contains for non-radiologist stakeholders such as clinicians and nurses. Any such capability should be open source so it can mature with broad community contribution. *(Osman Ratib)*
  - Gordon noted this would bring together the AI strategy and forward-looking innovation areas.
- **AI segmentation.** From a product perspective, customers want to plug fast 3D segmentation models, including their own models, into the viewer easily. Manual brush-based segmentation is increasingly obsolete. *(Benoit Tricot)*
- **Interfaces over embedded AI.** In the public sector, directly integrated AI features, even local models, can add months to institutional software review because of concerns about data handling and endpoints. An API or interface for connecting external models is preferable. *(Denny Spiegelberg)*
- **Data management.** Open source has not yet addressed trustworthy, transparent tools for managing imaging data. This is increasingly important with AI and cybersecurity concerns. *(Osman Ratib)*

**Suggestions**

- Include AI for image interaction (human-in-the-loop use, editing, and review of AI results) in the AI strategy, not only AI-assisted development. *(Salim Kanoun)*
- Prioritize an easy, standardized way to plug in external AI segmentation models, including customer-provided models. *(Benoit Tricot)*
- Provide AI capabilities through interfaces or APIs rather than embedding them directly in OHIF, to ease institutional review. *(Denny Spiegelberg)*
- Explore LLM-based summarization of study content for non-radiologist users, developed openly. *(Osman Ratib)*
- Consider scientific and high-end imaging applications as a focus now that AI reduces traditional development overhead. *(Steve Pieper)*
- Consider open-source data management tooling as a potential innovation area. *(Osman Ratib)*

## 4. Community & Product Engagement

**Discussion**

- Salim suggested expanding the OHIF community beyond software to scientific collaboration. It could be a forum for use cases from industry and academia, informing the roadmap and helping define good AI use cases in medical imaging. *(Salim Kanoun)*
- Companies building on OHIF often see new features only at release. By then, design or UX concerns are hard to raise. *(Benoit Tricot)*

**Suggestions**

- Create a scientific community forum. For example, regular sessions where authors of significant recent medical imaging papers or projects present to the community. *(Salim Kanoun)*
- Give downstream product teams a way to see and comment on feature design earlier in the process. *(Benoit Tricot)*
- Consider a recognition or certification label for experienced OHIF contributors. It would give freelancers credibility with industry clients, and label holders could contribute back to the project. *(Salim Kanoun)*

## 5. Long-Term Sustainment Beyond ITCR

**Discussion**

- **Donations.** Orthanc has raised roughly $180K through Open Collective over a few years. Platforms like Open Collective and GitHub Sponsors add visibility and recognition that a plain donate button lacks. *(Mohannad Hussain)*
  - Gordon noted that OHIF's current donate button has only raised a modest amount to date. Donations go through MGH, a 501(c)(3). OHIF was briefly registered as its own foundation, but it was discontinued because of administrative overhead.
  - James added that a standalone foundation could open partnership opportunities MGH policy restricts, such as software discounts or AI credit programs.
  - Donations alone are unlikely to sustain the project at its current scale. *(Andrey Fedorov)*
- **Feature crowdfunding.** A Kickstarter-style mechanism would let users propose features and pledge funding, with multiple users pooling resources for shared needs. This is more motivating than a donation, plays to OHIF's strengths as a project that builds things, and reflects OHIF developers' ability to use AI efficiently on the codebase. *(Andrey Fedorov)*
  - Rob noted a natural tension between open source and funding. He added that framing support around "what do we want to create next" is more compelling than warning that the project will stop without it.
  - Scott noted that companies that have benefited from OHIF, and have sunk costs in it, have a vested interest in its health.
- **Industry participation.**
  - In 3D Slicer, most major components exist because companies building on the platform contributed the fixes and features they needed. *(Steve Pieper)*
  - Industry could submit needs that are too costly for them to build alone, and co-fund open-source implementations shared across the community. Companies will share pieces that don't affect their differentiation, and shared components also help interoperability. *(Osman Ratib)*
    - Rob asked how to help companies get comfortable sharing a platform with competitors.
    - Gordon shared that a past co-funded industry project supported Cornerstone3D's development, and noted that this approach may carry the risk of having to navigate resistance to open source within industry leadership.
- **Foundation model.** As the ecosystem grows, a foundation with contributions from industry and institutions, similar to the Linux Foundation, could make OHIF self-sustaining. *(Salim Kanoun)*

**Suggestions**

- Evaluate a modern donation platform (Open Collective, GitHub Sponsors) with visible backer recognition. *(Mohannad Hussain)*
- Explore a feature crowdfunding or pledge mechanism for community-requested features. *(Andrey Fedorov)*
- Invite industry to submit unmet needs for co-funded open-source development, focused on non-differentiating shared components. *(Osman Ratib)*
- Work toward an industry- and institution-supported foundation model as the community grows. *(Salim Kanoun)*
