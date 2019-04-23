---
layout: post
title: "Monzo Oven"
description: "Monzo Oven Exercise"
permalink: monzo
---

After a crazy night out, Monzo's CEO has decided to pivot the company from the financial market to the far more interesting field of kitchen appliances.

Our first project is to **design the companion iPhone or Android app for the revolutionary Monzo next-gen smart oven.**

## What we have and what we can do

The only interactive bit on it is the handle to open the door. All the remaining functions must be entirely managed from the app (and that's what we need you to design).

Thanks to wireless connectivity and a bunch of inputs and sensors the oven can potentially communicate all this information to and from the app. These are not requirements, just the ingredients we can take advantage of.

- Indicate power level for top, bottom and fan
- Indicate levels of dirt
- Indicate air temperature (oven temperature)
- Indicate food temperature
- Indicate weight of the food
- Indicate whether something is burning (via smoke detector)
- There is also a built-in camera that functions as an oven window.

## Interviewing users

I am designing an app with **Isabel** in mind. Isabel is a female in her 60s who loves technology but is not too fussed about cooking. Upon hearing about this design challenge, she was very keen to try the oven out and disappointed when she learned that this was a concept and that the oven does not exist.

Isabel expressed an interest in managing an oven from an app (she owns an iPhone XR), and being able to change temperature as and when needed, as well as being able to switch off her oven if she ever forgets to. She also found the smoke detector functionality very useful.

Isabel did not see the use in scheduling an oven in advance, as she struggled to imagine when that would be useful.

> I would never leave food in the oven so as to start cooking it later on. That's strange, and a little bit gross. I would also never leave my house with the oven in progress, as that could be dangerous!


## Main user flow and screens

The main user flow is pretty straightforward, and follows what most users would do handling a conventional oven:

![](images/case_studies/monzo/oven-flow.png)

From considering the user flow, I decided that there would be four main screens:

![](images/case_studies/monzo/monzo-oven-screens.png)

## Assumptions and compromises

In order to continue with the task, I had to make some assumptions and discard a few options/solutions/features.

### Scheduling your cooking

I am making the choice not to include scheduling capabilities for the MVP. However, users can still schedule using a reminder app, calendar or alarm and start the oven from wherever they are should they want to.

### Viewing levels of dirt

Originally I considered having a screen for the sole purpose of viewing how dirty the oven is (in %). However, I eventually compromised on having that information be accessed through the _Support_ screen.

In terms of data display, **the oven will only display whether it needs to be cleaned or not.** A push notification will inform the user when the oven requires a clean.

**The oven is also self-cleaning**, meaning that the action of cleaning it can be triggered via the _Support_ screen as well. All the information will be included as part of the notification, and the notification should take the user straight to that menu.

### Oven modes

Inspired by my own oven at home, I kept the modes simple: Heating, Grilling and Defrosting.

**Defrosting should be making use of the incorporated scale**, whereby the oven would be defining temperature and time values, however that screen has not been included in the mockups.

### Food temperature

Ideally, I would have liked to include a capability whereby the user can set an alarm to alert them if or when the food reaches a certain temperature, which is particularly useful when baking or cooking certain meats. This feature has not been included due to time constraints, which means the user would need to monitor food temperature themselves if required.

### Push notifications

Push notifications should inform the user of the following:

- Oven is ready to use (has completed heating up).
- Time is up (accompanied by an alarm).
- Food is burning (accompanied by an alarm).
- Oven requires cleaning.

### Warranty & Support

The oven will come with some sort of warranty, and the related documentation will be accessible from the app.

There will also be an FAQ section and contact details should the customer not be able to sort an issue out by themselves.

## Sketches/Wireframes

![](images/case_studies/monzo/monzo-oven-first-sketches.png)

## Final screens

![](images/case_studies/monzo/monzo-oven-start.png)

<ol>
  <li>Switch on.</li>

  <li>Timer starts running for 5 minutes during pre-heating. The user can choose to go ahead and introduce the food in the oven anyway.</li>

  <li>At any time, the user can turn the oven off.</li>

  <li>Once the pre-heating has completed, the timer starts running. Both temperature and timer mirror the setup from the <em>Settings</em> screen. This screen is considered the <em>Main</em> screen.</li>

  <p><img src="images/case_studies/monzo/monzo-oven-cook.png" alt=""></p>

  <li>I have simplified the original icons and replaced them with iOS's segmented controls.</li>

  <li>Air temperature can be controlled with this slider. This value does not change unless the user chooses to, meaning that whenever they come back to the app the previous temperature will still be there. This slider can be changed at any time, and changes will be reflected on the <em>Main</em> screen.</li>

  <li>The timer can be controlled with this slider. This slider is animated and <em>moves backwards</em>, meaning that unless the user chooses to end the process sooner than what was pre-set, it will reach a stage of 0m – and then the alarm with set off. This slider can be changed at any time, and changes will be reflected on the <em>Main</em> screen.</li>

  <li>This functions as a traditional oven window. Thanks to the camera, the user can see what's in the oven (as long as it's on top). The user won't be able to see whatever is below the first shelf.</li>

  <li>This feature is display-only, and it informs the user on the current food temperature.</li>
</ol>


[View the final prototype](https://invis.io/P9RMAOPGU4M#/358956016_Oven-Switch_On){:target="_blank"}

## Into the future...

There are many things I would have added to this MVP had I had the time, including the following:

- Mocking up the _Support_ screen and the Self-Cleaning functionality.
- Including a feature that enables the user to set an alarm if or when the food reaches a certain temperature.
- Defining a brand and style guide and designing the iconography accordingly. The current icons function as placeholders rather than final icons.
- Scheduling capabilities for users that are not like Isabel.

## ...and beyond!

- The app could incorporate a library of recipes so that the user could just select whatever they want to cook, and the oven would change the settings depending on the weight of the food, temperature, etc.
- Using the recipe library, you could tell it what you have in the fridge and it would make meal suggestions based on what's available.
- The app could also sync with other kitchen appliances to let them know when they should start their own process (e.g. a Thermomix).
