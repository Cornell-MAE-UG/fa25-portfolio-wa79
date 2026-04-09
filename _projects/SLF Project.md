---
layout: project
title: Big Red Stompers
image: /assets/img/brslogo.png
imagealt: Big Red Stompers functional prototype
technologies:
  - Fusion 360
  - 3D Printing
  - Mechanical Prototyping
  - Testing
---

## Milestones
- [Client Pitch](#client-pitch)
- [Functional Prototype](#functional-prototype)

---

## Client Pitch
{: #client-pitch }

The goal of this project is to develop a portable handheld device that helps remove and destroy spotted lanternfly egg masses more effectively than scraping alone. Our team focused on combining egg-mass removal, crushing, and residue collection into a single device that is cleaner, faster, and easier to use in the field.

### Problem
Spotted lanternfly egg masses are often removed manually with scraping tools, which can be messy, incomplete, and inefficient. We wanted to create a product that would both remove the egg mass from a surface and destroy it in the same motion.

### Proposed Solution
Our concept uses three integrated functions:
1. **Scraping** to detach the egg mass from a wall or tree.
2. **Crushing/Stomping** to destroy the eggs after removal.
3. **Collection** to funnel residue into an attached bottle for containment.

### Initial Design Goals
- Make the device compact and handheld.
- Reduce mess during egg-mass removal.
- Improve destruction effectiveness compared to scraping alone.
- Provide a design that could be demonstrated clearly during exhibit day.

---

## Functional Prototype
{: #functional-prototype }

### Purpose of the Prototype
The functional prototype was built to test whether our mechanical design could successfully combine scraping, crushing, and collection into one handheld device. The prototype includes a housing, internal stomper face, compression spring, pull knob, scraper, and bottle-thread connector.

### Design Intent
The prototype is intended to perform three main functions:
- **Scraping:** remove the spotted lanternfly egg mass from the surface.
- **Crushing / Stomping:** compress the egg mass material with a spring-loaded stomper to destroy the eggs.
- **Collection:** direct residue into an attached bottle for containment.

### What Was Built
The prototype consists of:
- 3D-printed housing
- 3D-printed stomper face
- Compression spring
- 3D-printed pull knob / actuation interface
- 3D-printed scraper
- 3D-printed bottle-thread connector

### Assembly Summary
The device is assembled by:
1. placing the compression spring on the rigid rod,
2. inserting the spring-loaded subassembly into the housing,
3. attaching the pull knob,
4. installing the scraper,
5. securing the scraper plate to the rigid rod.

### What Was Tested

#### 1. Sliding Rail Motion and Interference
We tested whether the slider could move through its full intended range of motion without excessive friction, jamming, or interference.

**How it was tested**
- Measured the force required to initiate motion using a spring scale.
- Had 5 team members operate the slider and rate the difficulty from 1 to 10.

**Outcome**
- Initial motion required **10 N**.
- Mean user difficulty score before modification was **7/10**.
- After sanding the rail surfaces, the mean difficulty improved to **5/10**.
- The mechanism improved, but it still did not meet the desired usability range of **1–4**.

**Takeaway**
The next prototype should increase clearance tolerances and improve print/material quality to reduce friction and binding.

#### 2. Spring Mechanism Force and Usability
We tested whether the spring could be compressed by hand while still supplying enough force to crush the egg mass.

**How it was tested**
- First evaluated the McMaster spring by manual compression.
- Then tested a workshop spring and estimated spring constant using Hooke’s Law from a **500 g** load and **1.5 in** displacement.

**Outcome**
- The McMaster spring was too stiff for practical hand use.
- The workshop spring had an estimated spring constant of about **129 N/m** or **0.74 lb/in**.
- Later trials suggested the design likely needs a spring closer to **3–3.5 lbf/in** to more reliably generate crushing force with about **2 in** displacement.

**Takeaway**
The next prototype should use a somewhat stiffer but still hand-operable spring and improve the rod/attachment geometry for better load transfer.

### Success Criteria for the Final Prototype
We established the following quantitative criteria for evaluating the final design:

1. **Portability**  
   The device should weigh no more than **0.5 kg** and have a length no greater than **20 cm** without the bottle and **30 cm** with the bottle.

2. **Egg Destruction Effectiveness**  
   The device should destroy at least **95%** of the eggs in one egg mass in a single use.

3. **Removal Speed**  
   One egg mass should be completely removed and destroyed in under **10 seconds on average**.

4. **Residue Capture**  
   The device should funnel at least **80%** of the removed residue into the attached bottle.

### Exhibit-Day Demonstration Plan
For exhibit day, we plan to demonstrate two visible and measurable outcomes:
- complete egg-mass removal in under **10 seconds**
- at least **80% residue capture** in the bottle

This demonstration will show both the speed and cleanliness advantages of the design in a way that is easy for viewers to understand.

### Reflection
This functional prototype helped identify two major design risks: excessive friction in the sliding rail and insufficient force transfer in the spring-loaded crushing mechanism. These results directly informed the next iteration of the design and clarified what needs to improve before the final prototype.