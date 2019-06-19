---
layout: post
title: "N-Sure: an app to keep track of your insurance policies"
description: "Monzo Oven Exercise"
permalink: thought-machine
---

### Problem statement

Keeping track of all the various personal insurance policies that we have is difficult. Take a typical couple who have children, a house, a cat and a car. For such a household the following types of insurance are pretty likely to be in place all the time:

1. Buildings insurance
2. Contents insurance
3. Car insurance
4. Life insurance
5. Appliances insurance
6. Pet insurance

There will also be some types of insurance which are only added some of the time, such as travel insurance​.

Although some of these insurance products might be sourced from the same provider, it is more likely that there will be 5 or more different providers in use at the same time. Each policy also has different coverage schedules, different claims procedures, different renewal dates and different costs to pay for.

People will have different solutions in place to keep track, perhaps an email folder or even a file folder but very few would say they are on top of the admin or know where the right information is when you need it, say when needing to claim or change provider.

### Scenario

You are joining a startup which is looking to take advantage of new legislation requiring insurance providers to standardise their policy language and provide public APIs. This company has built techniques to import any insurance policy either through forwarded insurance policy emails or through a lookup of provider + policy ID.

The company is calling on you to help design their native app that will allow users to track and manage their insurance policies.

### Design task

To get the ball rolling on your first day your new boss asks you to pick a journey that you think would be important within their app and create three short deliverables:

1. A short research proposal which describes your selected journey and sets out what questions you would have for users to hone your design for it. (Max 300 words)
2. A wireflow that sets out how you would structure the journey (low fidelity, hand drawn is fine)
3. A high fidelity mock for a key screen (or multiple if you wish) within your journey, including explanatory notes as required

Your boss tells you to take no more than half a day on this task and asks that you assemble your deliverables as a single web page for review.

## The task

For my first project at N-Sure, I'd like to tackle the 'Add New Insurance Policy' journey, which should take the user from the moment they choose to add a new policy all the way to them viewing the information about their policy.

In order to find out what the best solution for this flow would be, I'd need to speak to the Product Manager and/or partners so that I can answer the following:

- What's the minimum information that we need to ask the customer in order to add a new policy to the N-Sure app
- How much information can we get from the insurer (provided the customer has given us their policy ID and/or has forwarded the emails related to the policy)
- Will the customer be able to manage their policy (change details, renew, cancel) from the N-Sure app?
- If not, should the app keep the customer's log in credentials for any given policy provider's website so that they can quickly access the insurer's app/website from the N-Sure app?

Once I've covered that section of the research, I'd like to speak to potential N-Sure customers to find out the following:

- How do they currently keep track of all their policies. How do they know when to renew them? Do they rely on the insurer giving them a call, do they add it to their calendars, or do they just have great memory?
- What would they expect the app to do. Should it just display information, like a catalog would, or should they be able to manage their policies from within the N-Sure app?

I'd also like to test the following:

- How comfortable would they be with giving us access to their inbox and/or forwarding the N-Sure team emails from their insurance company?
- Is our concept trustworthy, or are we asking for too sensitive information?

## Jenna needs to add a new policy to her tracker

Jenna just got a new motorcycle and has put it under insurance.

Already being an N-Sure user, Jenna only needs to add her new motorcycle insurance to the N-Sure tracker.

![](images/case_studies/n-sure/flows.png)
![](images/case_studies/n-sure/wireflows.png)

Here are a three mockups displaying the home screen, the screen where you can choose what type of insurance you will add, and the screen where you input the information to find your policy.

The step where the user selects how they are going to search for the information (policy ID vs forwarding emails) has been omitted.

![](images/case_studies/n-sure/insurancemockup.png)

Left to right:

- Home Screen, or main screen, where the user can view all of their current insurance policies and when they are due for renewal. From here they can access each of them individually to view more details.
- Screen that displays all the types of policy they can add to the tracker. The ones that display a yellow tick have already been added. When a type of policy is selected, the colour of the list component switches to yellow for a second and then transitions into the next screen.
- Screen where the user can input their policy ID. There is a Search Button hidden beneath the keyboard.
