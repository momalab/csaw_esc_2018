**Update 1: Registration deadline extended to September 17 and reports due date to September 24, 2018.**

CSAW 2018 Embedded Security Challenge (ESC)
===========================================

**Teams are encouraged to start investigating the challenge as early as possible.** 

*It is also recommended to 'watch' this repository on GitHub, as the challenge may be updated periodically*.

For registration information, policies, deadlines, deliverable details, and for information for contacting CSAW organizers, visit the [logistics](logistics.md) page.


## Overview

The Embedded Security Challenge (ESC) returns in 2018 for the 11<sup>th</sup> time, and we are proud to announce another exciting and educational global competition! ESC is part of [CSAW](https://csaw.engineering.nyu.edu/about), which is founded by the department of Computer Science and Engineering at NYU Tandon School of Engineering, and is the largest student-run cyber security event in the world, featuring international competitions, workshops, and industry events.


ESC 2018 will be a world-wide event held simultaneously in four regions: US-Canada, Europe, Middle East & North Africa, and India, with the finals taking place on November 8-10, 2018. The venues for each region are:

-   **CSAW US-Canada**: NYU Tandon School of Engineering, USA.
-   **CSAW Europe**: Grenoble Institute of Technology - ESISAR, France.
-   **CSAW MENA**: Higher School of Communication of Tunis - SUP'COM, Tunisia.
-   **CSAW India**: Indian Institute of Technology Kanpur, India.

The competition is organized in all regions under the supervision of Professor Michail Maniatakos (NYU Abu Dhabi), and the global challenge lead is Tasos Keliris, who is also the US-Canada region challenge lead. In Europe, the competition is organized by Professor Vincent Beroulle. In the MENA region, the competition is coordinated by Professor Mohamed Hamdi, with Marouene Boubakri as the regional challenge lead. In India, ESC is supervised by Professor Sandeep Shukla, with Rohit Negi as the regional challenge lead.

This year's ESC focuses on the security implications of the wide deployment of Internet-of-Things (IoT) devices, and how IoT devices can expand the threat landscape enabling covert data exfiltration attacks. The competition focuses on the **exploration, design, and experimental demonstration of covert data exfiltration attacks against IoT devices - smart light bulbs in particular - that can leak secret information through side-channels, bridging air-gapped networks**.


ESC 2018 Challenge Description
==============================

<p align=center a href="url"><img src="bulb.gif" align="center" height="300" width="300" ></a></p>

The theme of this year's ESC competition is **covert data exfiltration from Internet-of-Things (IoT) devices**. IoT devices are physical devices that have embedded electronics and software, and can interconnect and exchange data allowing enhanced dynamic automation and control actions. These devices are becoming ubiquitous, with several billion devices already deployed and several more billions projected to be deployed in the near future. A significant concern regarding IoT devices is their usually poor security posture, stemming from quick time-to-market requirements and lack of appropriate regulations. As IoT devices are being increasingly deployed in diverse environments, they introduce additional security threats to these environments.

The ESC 2018 competition considers the expansion of the threat landscape caused by IoT devices, and invites contestants to **develop covert attacks that (mis)use IoT devices - smart bulbs in particular - to exfiltrate data through side-channels from air-gapped networks**. 

The following (fictional) motivational scenario sets the stage for the ESC 2018 competition:

*Lean Enterprise Advanced Knowledge Solutions (LEAKS) is a private technology company that gets awarded most of the defense and military contracts of the country of IoTilandia. Given the sensitive nature of its contracts, LEAKS employs a complete air-gap separation for all its internal networks, ensuring no data is leaked through public connections.*

*A recent presidential order requires that all IoTilandia companies, including LEAKS, "IoTize" [sic] their infrastructure by making everything smarter; coffee makers, fridges, chairs, and light bulbs. To abide to this presidential order, LEAKS has installed sophisticated **smart light bulbs** in their offices and connected them to their internal network.*

In the CSAW Embedded Systems Challenge 2018 (ESC18), you are tasked to exploit these newly installed smart light bulbs to exfiltrate IoTlandia secrets, bridging the air-gapped networks of LEAKS.


## Assumptions & Requirements

The assumptions and high-level requirements for the attacks we invite the contestants to propose and implement are:
-   The focus of the competition is on the mechanisms and techniques of exfiltrating data, and not on identifying which data to exfiltrate. To that end, consider that you need to exfiltrate the character sequence (without the brackets): \[**Skynet is alive!**\]. How you choose to encode/modulate/transmit this sentence is entirely up to you.
-   You can exploit **any side-channels or compination thereof** you deem appropriate for exfiltrating data. The entire spectrum is your oyster!
-   You need to also consider, and where appropriate also develop, **mechanisms for receiving and decoding the transmitted data**, considering any complexity and cost tradeoffs.
-   The attacks are not limited to a specific layer of the development stack (hardware, firmware, software, network, application). You can design and implement attacks work **on any layer of the stack, including cross-layer attacks**.
-   Attacks must **covertly** exfiltrate data, meaning that they should be incospicuous and stealthy.
-   For the final phase you are asked to design and implement **at least one attack** on the physical smart light bulb provided by the organizers.
-   The smart light bulb that we will provide is tentatively the **Magic Blue Bluetooth Bulb**. We will verify the smart light bulb model at the end of the qualification phase.

See the [grading details](#grading) below to understand the impact of your design decisions on grading. 


## Challenge structure

The ESC18 competition is divided into two phases:

1. A preliminary **qualification phase**, where teams must compile and submit a written report characterizing possible side-channel attacks that (mis)use IoT devices, such as smart light bulbs, to stealthily exfiltrate secret information.

2. A **final phase**, where qualified teams are invited to the CSAW event of their region to present a live demonstration of their implementations on smart light bulbs provided by the organizers.

See below for more details on the requirements of each phase. 


### Qualification Phase

For the qualification phase, participating teams are invited to compile a **proposal** that characterizes different approaches and techniques (not necessarily only one approach/technique) that the teams aim to implement for (mis)using smart light bulbs to covertly exfiltrate data through side-channels. To that end, the proposal should also explore existing related work on the topic, focusing on (but not necessarily limited to) smart light bulbs and possible side-channel attacks against such IoT devices. The best approaches will include a discussion of related work, a clear threat model, demonstration of how and why the attacks are stealthy, at which layer they operate, what side-channels they seek to exploit, and how realistic these assumptions are. The teams are asked to clearly discuss all their assumptions and justify why their proposed approaches will be effective and stealthy. Approaches that are not realistic or require highly sophisticated equipment to carry out may not receive full consideration for the ESC competition finals.


### Final Phase

The **10 best** submissions of each region (US-Canada, Europe, MENA, India) will qualify to the final phase that requires **implementing** and **demonstrating** at least one covert side-channel data exfiltration attack on a smart light bulb provided by the organizers. The teams should also describe, and where applicable develop, a receiver that receives and decodes the leaked data (**Skynet is alive!**). The definitive goal is to implement a reliable, stealthy, and practical side-channel leakage attack. We understand that each hardware device is different, and that hardware hacking is hard. As such, after receiving the smart light bulb devices, attacks implemented for the final phase do not necessarily need to be the same as the attacks outlined in the qualification phase proposal.


## Grading


### Qualification Phase

Qualification phase reports will be evaluated by a team of experts, and will take into account the **correctness**, **potential**, **novelty**, **creativity** and **stealthiness** of the proposed strategies, as well as the completeness and quality of the compiled report.


### Final Phase

The evaluation of the finalist teams will be based on their aggregate score across five criteria. Specifically, on the day of the **live finals**, points for each attack will be awarded based on:

1. **Correctness** of the implementation and live demonstration of transmitting and receiving the data. (20%)

2. **Throughput and effectiveness** of the implemented attack, including bitrate at which the proposed method can exfiltrate data, and distance at which these data can be meaningfully received and processed by an appropriate receiver. (20%)

3. **Generality** of the implemented attack, including how easily the attack generalizes on other IoT devices, whether it can handle arbitrary data, and complexity/cost tradeoffs. (20%)

4. **Stealthiness** of the proposed attack, including how difficult it is to detect the attack with state-of-the-art techniques, at which layer of the stack the attack is deployed, how incospicuous it is, and whether it significantly impacts the normal operation of the smart light bulb. (20%)

5. **Quality, and elaboration** of the the final report submitted through the HotCRP system, which should list all assumptions, provide a thorough technical discussion, and address all the above four criteria. (20%)


If teams wish so, they are welcome to demonstrate more than one attacks during the finals. In that event, their best attack will be weighted with 75%, their second best with 75/2 = 37.5%, the third with 75/4 = 18.75%, and so on. This grading scheme implements a geometric series that converges at 150% of the total grades for one attack. It is employed to encourage teams that want to develop and demonstrate more than one attacks, but discourages brute force approaches, enforcing diminishing returns.


The evaluation of the finalists based on the above metrics will be the responsibility of a panel of **industry expert judges** in each region. During the day of the finals, each team should be able to answer the questions posed by the judges, in addition to **demonstrating live the correctness, effectiveness, and stealthiness** of their attacks on the provided smart light bulbs. Furthermore, the finalists are required prepare a **Powerpoint presentation** of their work and a **short video** to present on the day of the finals, complementing their submitted **final report**. On the day of the finals, demonstration of the proposed  attacks will be the responsibility of each team.


You can refer to the [deliverables section](logistics.md#deliverables) for more details on the qualification and final phase deliverables.


To find more information regarding how to register and participate click [here](logistics.md).