# **OHIF Advisory Board – Meeting Notes**

**Date:** May 13, 2026

**Attendees:** 

* Gordon Harris  
* Rob Lewis  
* Alireza Sedghi  
* Andrey Fedorov  
* Bill Wallace  
* Dan Rukas  
* Salim Kanoun  
* Mo Al-Sad  
* Simon Doran  
* Ibrahim Mohamed  
* Denny Speigelberg  
* Benoit Tricot  
* James Hanks

# **1\. AI-Assisted Development**

**Discussion**

* The community is increasingly using AI agents to fork and modify OHIF; the project should embrace this rather than resist it.  
* Low-quality AI-generated PRs are a growing concern; guardrails are needed to keep contributions architecturally coherent.  
* Open question: how to incentivize community members using AI to contribute back rather than maintain private forks?

**Suggestions**

* Add/continually manage agent instruction files (e.g., CLAUDE.md, AGENTS.md, architecture manifest) to OHIF and Cornerstone repos covering architecture, extension patterns, and PR conventions.  
* Add codemod for each release with scripts and instructions to provide agents during migration  
* Define internal criteria for a “successful contribution” so AI-driven PRs can be triaged consistently. (ie, does it meet needs, solve existing problem)  
* Increase transparency of internal issue tracking so LLMs and contributors can see work in progress before duplicating effort. Adding community triage list

# **2\. Community Engagement**

**Discussion**

* Usage metrics continue to climb while traditional engagement (office hours, channel questions) is declining.  
* Office hours attendance has dropped; biweekly cadence is hard to remember and easy to miss for a full month.  
* Incentives differ by audience: academics value publications and citable work; commercial contributors value long-term community maintenance and visibility.

**Suggestions**

* Focus on community messaging (social media, etc): articles/posts, etc can describe incentive for contributing back, benefits of working with the open source team  
* Rework office hours to a consistent weekly cadence and publish topics in advance (Slack post, etc)  
* Invite contributors and companies using OHIF to present use cases in office hours or dedicated sessions.  
* Build a network-of-expertise directory of contributors by domain specialty (radiotherapy, nuclear medicine, PET/CT, etc.) to enable scientific collaboration and consulting.  
* Solicit a short best-practices write-up from commercial contributors on open-source contribution workflows.

# **3\. Contributor Workflow & PR Efficiency**

**Discussion**

* PRs that should take days frequently stretch to weeks due to scope creep and review delays; one or two such experiences cause contributors to disengage.  
* Commercial contributors face internal pressure when timelines slip, making fast turnaround critical for sustained engagement.  
* Automated PR review (Greptile, Claude) is helping but is still being tuned.

**Suggestions**

* Continue expanding the automated PR review process and set an internal target for time-to-first-review.  
* Aim to accept contributions at a minimal-working-state threshold rather than blocking on non-essential refinements.  
* Review accepted and pending PRs to identify recurring change patterns; let those patterns inform extension-point design. We can also close outdated or out of scope PRs. 

# **4\. Extension Model**

**Discussion**

* The current extension library has not gained traction because it is not a true plugin interface — no dynamic loading without recompile, and not everything is tweakable from an extension.  
* A Slicer-style extension ecosystem could decentralize development and simultaneously address contributor incentives, stagnant PRs, and unaddressed use cases.  
* Contributors bypass the extension model and modify core because the architecture is not well understood; documentation gaps affect both human and AI contributors.  
* A successful relaunch requires the framework to be technically capable, seeded with strong demonstration extensions, iterated over time, and supported by a marketplace/community story.

**Suggestions**

* Starting with Bill’s proposal PR regarding enabling dynamic extension loading via URL, explore sustainable changes to the extension model that the team can practically execute given current resources.   
* Review and define the extension model: required use cases, needed extension points, and enforcement (e.g., reject PRs that modify core when an extension would suffice).  
* Seed the extension library with high-quality demo extensions before re-promoting it to the community.  
* Revisit the gallery page on the public website to ensure the community can clearly access one-click runnable examples and understand the path to create new extensions.  
* Explore decomposing OHIF toward a headless library model so third parties can build custom viewers with AI assistance, with the core team acting as architectural consultants.