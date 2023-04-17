---
layout: post
title: Distributed energy storage - promise, and perils 
---



Moves towards distributed storage:
==================================
Great changes are happening in the energy sector and there have been significant developments in the debate around renewable energy in South Australia. Here are some:
 * South Australia had a state-wide blackout. 
 * Load shedding (also known as brownouts, or rolling blackouts) was applied to 90000 households in SA on the afternoon of a particularly hot day. 
 * In response, the South Australian government commissioned and insalled a large battery (the Hornsdale power reserve) 

On top of this, there were calls to the former Labor government that, as well as embracing a grid-level battery storage system, they should pursue distributed residential energy storage using a scheme such as Reposit (AGL is also rolling out such a system now, called the virtual battery). The subsequently-elected Liberal party supported this, and also proposed to subsidise home battery systems - a program that is now underway. Although not enforced, this can essentially operate as an internet-coordinated distributed power company that manages home batteries to release energy to the grid during times when the short-term cost (spot price) is high. Households can make money by doing this. Companies like Reposit also offer similar services in other states.

Why on-grid distributed storage is a great idea:
================================================
I think this is a great idea, and it's commendable that such policies have bipartisan support in South Australia. It is good for people in cities to install battery storage systems, as long as they remain connected to the grid. There are a few reasons I think this:
 * The grid is a sunk cost. It's already built so we should use it. The grid allows renewable energy sources and storage to be sized to average demand, rather than being sized to maximum demand. This is much cheaper -- if everyone went 'off grid' we would need many more solar panels and batteries than if everyone stays on grid and shares their resources.
 * Generally speaking, shared resources are used more efficiently. Let's assume that 5% of houses have a battery installed (in a few years time). We, as a society, will be much better off if those batteries are used to stabilise the grid during times of peak demand, rather than have those households disconnect from the grid. Those households should be paid for the service of course!
 * Distributed power is a good thing because it lessens the load on the grid and improves resiliance (there is not a central point to fail), it also reduces power transmission losses.

The Problem:
============
One of the big benefits of having distributed power supplies is that of resilience. If one (or a few) systems fail or are disconnected it probably doesn't matter for the grid as a whole. It lessens our dependence on the grid as a whole, and so improves resilience.

But... although such a distributed system  decreases reliance on the electricity grid, it greatly **increases** reliance on the telecommunications grid. The internet is vital to coordinate the distributed "virtual" battery. Without the distributed batteries being able to talk to each other and the central controller, which needs to get data from the grid, it is impossible for them to coordinate their activities and the system ceases to function properly (for example, with no internet, it becomes impossible for the grid to request delivery of power from the distributed storage at a time of need).

Do not believe people who tell you a system is secure. It is not secure -- it is only a matter of time until software or hardware vulnerabilities are discovered and exploited.

A mitigation:
=============
It is not possible to remove the consequences of attacks -- we can only reduce their consequence and likelihood of success. The distributed battery system needs to communicate, and that communication is inherently insecure. The system needs to be built so that it is resilient to internet-based attacks at the system level. I am not an expert in internet security, but here are my thoughts:

## The system should be designed with security in mind 
The critical aspect of the system is its ability to respond to legitimate internet instructions (only!) and react accordingly. The designers need to be aware of the inherent risk of exposing such command and control interfaces to the internet. The security team should have oversight across all teams during the development of this system. There needs to be robust testing of the system(s) (at all levels, from low level to high level) to examine the security implications of design and implementation decisions.

## The system should be heterogenous
There should be many types of devices communicating on an agreed open protocol. Having many types of devices means that, even if some of them are compromised by an attacker, they are unlikely all to fail (they will be based on different hardware and software making it unlikely that a universal security vulnerability exists). This represents security through diversity.

## The system should fail-safe
The internet should not be the only method of communication between devices. They should second-guess the instructions they receive from the cloud, by performing their own assessments of grid stability. For example, the grid can use frequency modulation to signal whether more generation capacity is needed (eg. if the frequency starts to fall from a nominal 50 Hz to 49 Hz, that is a recognised signal -- this needs to be preserved as a signalling method). In this way, the devices should use the internet as a communications channel where it is available, but not be dependent on it for all aspects of their function.

## User interface elements should be kept separate from the control systems
User interfaces are almost always less secure than system interface elements. This is because user interfaces have the added constraint of usability, which is often at odds with security requirements. User interfaces should be through a seperate cloud/web portal that has no direct connection to the system interface.

Conclusion:
===========
On many occasions, systems have been designed to use internet platforms with the unconscious assumption that the internet is both safe and persistent. The internet is neither of those things. I hope that the designers of distributed storage are mindful of this, so that their system(s) will be resilient in the face of unexpected communications downtime or malicious attacks.


![_config.yml]({{ site.baseurl }}/images/business_card_front.png)

