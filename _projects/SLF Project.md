---
layout: project
title: Big Red Stompers
image: /assets/images/brslogo.png
imagealt: Big Red Stompers project cover image
technologies:
  - Fusion 360
  - 3D Printing
  - Mechanical Design
  - Prototype Testing
---

## Milestones
- [Client Pitch](#client-pitch)
- [Functional Prototype](#functional-prototype)

---

## Client Pitch
{: #client-pitch }

**Team:** Big Red Stompers  
**Clients:** Cornell CALS Extension / E&J Gallo Winery / National Grape

### Problem Statement
Spotted lanternflies (SLF) mainly target grapevines. As a result, grape farmers are trying to manage SLF populations in vineyards and nearby trees. SLF egg masses contain around 30–60 eggs, creating rapid population growth that affects later growing seasons. Current SLF population reduction methods, such as netting and manual egg removal, are difficult to scale across larger vineyards.

### Impact
Elimination of SLF eggs prevents the development of adult populations that cause the most damage to vineyards. The average SLFs per vine starts low, increasing sharply following the transition from nymph to adult stages. As a result, attacking the root cause would help protect regions like Lake Erie and the Finger Lakes from major losses between 1.5 million dollars in year one and 8.8 million dollars by year three of infestation.

### Proposed Concept: *Stomp n' Scrape*
**What it is:**  
A handheld egg-removal device.

**How it would be used:**  
Designed to crush SLF egg mass shells and immediately scrape them into a rubbing-alcohol-filled vessel to prevent hatching.

**Why it’s better than the status quo:**
- Reduces the chance of leaving viable eggs behind.
- Minimizes mess and user discomfort by sealing egg material instantly.
- Improves output and efficiency compared to manual scraping alone.

### End-of-Semester Proof of Concept
A functional prototype with a crushing feature, integrated scraper, and removable alcohol container, fabricated using 3D-printed components and accessible materials, and tested on simulated SLF egg masses to evaluate effectiveness and ease of cleaning.

### Key Risks / Unknowns
1. Egg masses harden, making it difficult to ensure they are fully damaged. Two methods to kill the egg masses are crushing them and then scraping them into rubbing alcohol to kill the remaining ones.  
2. Public aversion to killing or interacting with SLF, as crushing egg masses may be off-putting. This can be tested with user trials and user comfort feedback.  
3. Many eggs are laid on high surfaces; 98% of eggs are found at unreachable heights (+10 feet) on trees. This suggests testing attachments to extendable tools so users can reach higher egg masses.

### Questions for Client
**What is preventing you from currently targeting egg masses? Is it location, time, or resources?**  
*Decision affected:* This would affect the aspects we want to emphasize in our design, such as accessibility to higher areas and ease of cleaning, based on client demand.

**Are there methods for reaching high areas that you are currently using?**  
*Decision affected:* This would affect whether our product must account for reaching high-up areas, or whether it can be used with existing tools.

**How much would you need to reduce or eliminate SLF after they’ve already reached the grapevines?**  
*Decision affected:* This would affect our focus on egg masses and could potentially shift our direction toward the adult stage instead.

### References
- [New York State Integrated Pest Management. *Spotted lanternfly management.*](https://cals.cornell.edu/integrated-pest-management/outreach-education/whats-bugging-you/spotted-lanternfly)
- [Hayes, C. (2025, January 27). *Spotted lanternflies could cost NYS grape industry millions.* Cornell Chronicle.](https://news.cornell.edu/stories/2025/01/spotted-lanternflies-could-cost-nys-grape-industry-millions)
- [Krawczyk, G. (2023, August 30). *What should you do with spotted lanternfly egg masses?* PennState Extension.](https://extension.psu.edu/what-should-you-do-with-spotted-lanternfly-egg-masses)

### Figure
![Average SLFs per Vine (2018-2020)]({{ "/assets/images/SLF.png" | relative_url }}){: style="max-width:100%; width:450px; height:auto; display:block; margin:0 auto;"}

---

## Functional Prototype
{: #functional-prototype }

### Purpose of the Prototype
The functional prototype was built to test whether our design could combine three key functions into one handheld device: scraping spotted lanternfly egg masses off a surface, crushing them with a spring-loaded internal stomper, and collecting the residue in an attached bottle.

### Prototype Components
The functional prototype consists of:
- Housing
- Stomper face
- Compression spring (McMaster Code 8969T983)
- Knob / actuation interface
- Scraper
- Bottle thread connector

Most structural parts were 3D printed, while the spring was selected and tested separately.

### Design Intent
The design combines three main functions:
1. **Scraping** to remove the egg mass from the surface  
2. **Crushing / Stomping** to compress and destroy the egg mass material  
3. **Collection** to funnel the residue into an attached bottle for containment and later neutralization

![Average SLFs per Vine (2018-2020)]({{ "/assets/images/pic1.png" | relative_url }}){: style="max-width:100%; width:600px; height:auto; display:block; margin:0 auto;"}
![Average SLFs per Vine (2018-2020)]({{ "/assets/images/pic2.png" | relative_url }}){: style="max-width:100%; width:600px; height:auto; display:block; margin:0 auto;"}

### Assembly Process
The prototype is assembled by:
1. preparing the spring-and-rod subassembly,
2. preparing the shell casing,
3. inserting the spring-loaded plate into the housing,
4. attaching the pull knob,
5. installing the scraper,
6. attaching the scraper plate to the rigid rod.

![Average SLFs per Vine (2018-2020)]({{ "/assets/images/assembly.png" | relative_url }}){: style="max-width:150%; width:900px; height:auto; display:block; margin:0 auto;"}

### What Was Tested

#### Test 1: Sliding Rail Motion and Interference
**Part being tested:** Housing rail and slider/stomper interface.

**What was tested:**  
Whether the slider could move through its intended range of motion without excessive friction, jamming, or interference.

**How it was tested:**  
The force required to initiate motion was measured using a spring scale. In addition, five team members operated the slider and rated ease of use on a 1 to 10 scale.

**Results:**  
- Initial force required to initiate motion: **10 N**
- Mean user difficulty score before modification: **7/10**
- Mean user difficulty score after sanding the rail surfaces: **5/10**

Even after sanding, the mechanism remained outside the desired usability range of 1–4.

**Outcome for next iteration:**  
The next prototype should increase clearance tolerances and use PETG instead of PLA to improve sliding performance and reduce interference.

#### Test 2: Spring Mechanism Force and Usability
**Part being tested:** Compression spring and stomping mechanism.

**What was tested:**  
Whether the spring could be compressed by hand while still supplying enough force to crush the egg mass.

**How it was tested:**  
The team first manually tested the McMaster spring. Then a workshop spring was evaluated using Hooke’s Law based on a 500 g load and a displacement of 1.5 inches.

**Results:**  
- The McMaster spring was too stiff for practical hand use.
- The workshop spring had an estimated spring constant of about **129 N/m** or **0.74 lb/in**.
- Later trials suggested that a spring closer to **3–3.5 lbf/in** would better support the intended crushing force with about 2 inches of displacement.

**Outcome for next iteration:**  
The design should use a somewhat stiffer but still hand-operable spring and redesign the rod/attachment geometry to improve force transfer.

### Success Criteria
Our final prototype will be evaluated using the following measurable criteria:

1. **Portability**  
   The device must weigh no more than **0.5 kg** and have a length no greater than **20 cm** without the bottle attachment and **30 cm** with the bottle attachment.

2. **Egg Destruction Effectiveness**  
   The device must destroy at least **95%** of the eggs in one egg mass in a single use.

3. **Removal Speed**  
   One egg mass must be completely removed and destroyed in less than **10 seconds on average**.

4. **Residue Capture**  
   The device must funnel at least **80%** of the egg residue into the attached bottle.

### Exhibit-Day Demonstration
Our exhibit-day demonstration will focus on two visible and measurable results:
- complete egg-mass removal in under **10 seconds**
- at least **80% residue capture** in the bottle

This helps connect the prototype directly to clear success criteria during the final presentation.

### Reflection
This prototype showed that the overall concept is feasible, but also revealed two major design issues: excessive friction in the rail system and insufficient force transfer in the spring-loaded crushing mechanism. These tests helped identify the main changes needed for the next iteration and gave us measurable criteria for evaluating the final version.