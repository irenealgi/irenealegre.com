---
layout: post
title: "New Linesheet Visibility settings for JOOR platform"
description: Streamlined Linesheet Visibility by enabling bulk visibility setup using existing Customer Groups and filters, improving efficiency and clarity with a new dual-listbox interface and radio-button design.
permalink: joor-linesheet-visibility
---

![](images/case_studies/joor-linesheet-visibility/linesheet-visibility-thumbnail.png)


## The Context

### JOOR Platform
JOOR is a wholesale fashion platform that connects Brands (who sell products) and Retailers (who purchase products in bulk). Retailers can place orders with Brands once they are "connected" on the platform. 

### Brands and Retailers
Brands can create orders for Retailers on JOOR, provided they are "connected." Retailers can also create their own orders once they have a connection with a Brand.

### Linesheets & Styles
A *Linesheet* is a collection of products (*Styles*) organized by themes such as season, garment type, or gender. Retailers browse and shop from *Linesheets* to create their orders, similar to a fashion catalog.

### Linesheet Visibility
For a *Connection* to view and shop from a *Linesheet*, visibility must be configured. There are three visibility options available:

- **Public**: Anyone with the link can access the *Linesheet*.
- **My Connections**: All *Connections* of the Brand can view the *Linesheet*.
- **Select Connections**: Only specific *Connections* selected by the Brand can view the *Linesheet*.

## The Problem

When configuring visibility for a *Linesheet* to specific *Connections* (using the "Select Connections" option), two key problems arise:

1. **Temporary Grouping**: The *Connections* selected for a specific *Linesheet* are not saved or stored anywhere else on the platform, making them inaccessible for future use.
2. **Tedious Setup**: Since the selection is done individually for each *Linesheet*, the same group of *Connections* cannot easily be reused across multiple *Linesheets*, which makes it time-consuming for users to replicate this process every time.

### Customer Groups
*Customer Groups* are pre-defined groups of *Connections* that already exist on the platform, primarily for reporting purposes. We decided to extend this feature, allowing users to leverage these groups when setting *Linesheet Visibility*.

## Research

### What We Already Knew
Users expressed a preference for the dual-listbox interface used elsewhere on the platform for managing large data sets, as it allowed them to efficiently search, select, and move items.

### What We Did
We conducted multiple rounds of internal testing and user feedback sessions, validating our hypotheses, testing prototypes, and iterating on solutions to ensure that the final design met user needs.

### What We Discovered
Despite the dual-listbox being considered a traditional UI pattern, users found it the most intuitive for managing large sets of data. It provided an easy way to search for items, select multiple entries at once, and transfer them to a new list, which could then be edited or reviewed.

## Requirements

### Ambitious Start
Initially, we aimed to allow users to:
- Leverage existing *Customer Groups* to make it easier to assign visibility to multiple *Connections* at once.
- Allow users to create and save new *Customer Groups* for future use, with the ability to modify and re-use them.

### Scaling Back
After evaluating the scope, we decided to remove the ability to create new *Customer Groups* within this feature. This functionality already existed elsewhere on the platform, so we focused instead on enabling users to assign *Linesheet Visibility* in bulk while leveraging existing *Customer Groups*.

### Introducing Filters
During testing, we discovered that many users didn’t actively use *Customer Groups* or didn’t find them useful for their workflow. Instead, many wanted to categorize *Connections* by other criteria, such as *Price Type* (i.e., the currency assigned to each customer). We decided to incorporate filters for *Customer Groups* and *Price Types*, leaving room for additional classification options in the future.

## Workflows

### Existing Flows
I began by creating screenflows that document the current screens and illustrate ideas for integrating the new functionality into the existing flow. To leverage our existing UI for assigning visibility to groups of connections, I started by capturing screenshots of that interface and embedding them into the screenshots of the current linesheet visibility modal. I highlighted the specific screens I plan to work on by framing them in an orange rectangle for easy identification.

![](images/case_studies/joor-linesheet-visibility/initial-concept.jpg)

### Additional Flows
Phase 1 focused on enabling users to easily set up linesheet visibility for multiple linesheets and selected connections in a single step. Phase 2 was intended to introduce the ability to create customer groups directly from the new UI, replacing the existing system for creating customer groups. However, Phase 2 was ultimately abandoned due to its added complexity and the lack of sufficient time and resources for implementation.

![](images/case_studies/joor-linesheet-visibility/user-flow-4.jpg)

## Setting Up Visibility: From Toggles to Radio-Buttons

Previously, users selected visibility options using toggles for *Public* and *All Connections*. However, the design was confusing because selecting *All Connections* automatically selected *Public*, but the reverse wasn’t true. There was also no clear way to make a *Linesheet* *Private*; users had to turn off both toggles to achieve this.

![](images/case_studies/joor-linesheet-visibility/existing-linesheet-visibility-modal.png)

### New Approach
We switched to using radio-buttons, ensuring only one option can be selected at a time. We also added description text next to each option to clearly explain its function. A new *Select Connections* option was also introduced for more granular control.

![](images/case_studies/joor-linesheet-visibility/new-linesheet-visibility-modal-3.jpg)
![](images/case_studies/joor-linesheet-visibility/price-type filter-open-dropdown-open3.jpg)

## Variations on a Dual-Listbox

We explored several different approaches for the dual-listbox UI to optimize the experience:

- **Add/Remove Buttons**: Initially, we considered adding buttons next to each list item (e.g., *Add* and *Remove*) to allow users to move items with fewer clicks. However, this design was discarded because it made it more difficult to unselect items.
  
- **Checkboxes for Selection**: We also thought about using checkboxes with highlights for selecting items, but this created UI complexity and potential conflicts with checkboxes used in the *filters* section.

![](images/case_studies/joor-linesheet-visibility/checkboxes-3.png)

- **Other Discarded Ideas**: 
  - Placing *Customer Groups* at the top of the left list for quick selection.
  - Using a *Select All* option at the top of the list, combined with *Add* and *Remove* buttons in the middle, to streamline the process.

## Final Solution

### Phase 1
The first phase introduced the ability to set *Linesheet* visibility in bulk using *Bulk Actions*. We also added the *Select Connections* option to the visibility setup modal, along with a new screen to let users select from their list of *Connections*.

![](images/case_studies/joor-linesheet-visibility/linesheet-visibility-phase-1.gif)

### Phase 2
In the second phase, we added filters for *Customer Groups* and *Price Types*, allowing users to more easily organize and sift through their *Connections* based on those attributes.

![](images/case_studies/joor-linesheet-visibility/linesheet-visibility-phase-2.gif)

## Conclusion

The Linesheet Visibility improvements addressed key user pain points by enabling bulk actions and leveraging Customer Groups and Filters for better organization. Switching to radio-buttons simplified the interface, and the dual-listbox proved intuitive for managing large datasets.

Although creating Customer Groups in the modal was postponed, the phased approach delivered impactful improvements while keeping complexity low. Early feedback suggests these changes save users time and effort, with survey results expected to confirm these benefits and guide future iterations.