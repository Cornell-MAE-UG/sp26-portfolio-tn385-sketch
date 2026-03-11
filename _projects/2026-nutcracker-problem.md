---
layout: project
title: "Lever Nutcracker Design"
description: Nutcracker Calculations
technologies: [Statics, Design]
image: /assets/images/nutcracker.jpg
---


**1. The Problem Statement & Objective (Find)**

I had to to determine the necessary geometry (arm lengths and gap dimensions) of a simple lever nutcracker that can crack a macadamia nut using hand grip strength. I needed it to be so that the mechanical advantage of the lever is enough to crack the nut without exceeding someone's maximum grip strength.



**2. Constraints & Input Parameters (Given)**

| Parameter | Value | Source |
|---|---|---|
| Load required to crack macadamia nut | **222.18 kg** | Schrauf et al., *Anim Cogn* 11, 413–422 (2008) |
| Maximum human grip strength | **~45 kg** | Mathiowetz et al., *Am J Occup Ther* 39(11), 789–798 (1985) |
| Size of macadamia nut (diameter) | **~2 cm** | Typical macadamia nut dimensions |
| Distance from joint to nut (ℓₙ) | **5 cm** | Assumed from standard nutcracker geometry |



**3. My Approach**

**Part A:**

The nutcracker is modeled as a simple lever with the pivot (joint) at one end, the nut positioned near the joint, and the hand applying force at the far end. By taking a moment balance at the joint, we can find the required arm length ratio to achieve the necessary mechanical advantage.

![Part A calculations]({{ "/assets/images/part-a-calculations.jpg" | relative_url }}){: .inline-image-r style="width: 200px"}

**Part C:**

Instead of hand grip, an IP65 Mini Linear Actuator replaces the input force. The same moment balance applies, but now Fᵢ = 76.6 kg (169 lbs, the actuator's rated max load).

![Part C calculations]({{ "/assets/images/part-c-calculations.jpg" | relative_url }}){: .inline-image-r style="width: 200px"}



**4. Diagram**

![With Linear Actuator]({{ "/assets/images/linear-actuator.jpg" | relative_url }}){: .inline-image-r style="width: 200px"}


**5. Discussion on Usability of Design**

**Hand-Grip**
The hand-powered design results in a nutcracker 24.7 cm long, with the 2 arms spreading 9.87 cm apart at the tip in the closed (cracking) position. When it is open open, the gap is much wider. This means that someone has to stretch their had really wide before they squeeze it. The tool is also really bulky. In theory it is valid, but its not practical for everyday use.

**With Linear Actuator**
Replacing the hand grip with the IP65 Mini actuator makes the necessary arm length to 14.49 cm. The 1-inch stroke helps as well. This design is more practical because it is smaller and easier to use. The cons to this design is that now it's not as simple and needs a power source, but the math shows that it works better.


**Where I got my Numbers From**

- Schrauf, M. et al. "Do capuchin monkeys use weight to select hammer tools?" *Animal Cognition* 11, 413–422 (2008). [https://doi.org/10.1007/s10071-007-0131-2](https://doi.org/10.1007/s10071-007-0131-2)
- Mathiowetz, V. et al. "Grip and pinch strength: normative data for adults." *American Journal of Occupational Therapy* 39(11), 789–798 (1985).
- Progressive Automations — IP65 Mini Linear Actuator: [progressiveautomations.com](https://www.progressiveautomations.com/collections/linear-actuators)
