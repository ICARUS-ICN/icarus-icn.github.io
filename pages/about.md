---
layout: home
title: ICARUS
description: Information-Centric sAtellite-netwoRk for vehicUlar communicationS
#background: /assets/img/chuttersnap-146799-unsplash.jpg
permalink: /about/
---

{: .alert .alert-info}

During the last decade, access to space has become more affordable. Launch
prices have fallen below ten thousand dollars per kilogram of useful load for
Low Earth Orbit (LEO) satellites, a reduction that is expected to continue
for the foreseeable future. This price reduction has created the proper
opportunities for private entities to launch a new generation of satellite
constellations and provide advanced wideband communications services.

These new satellite communication (SatCom) networks can play a significant role
in fleet management applications (cars, trucks, trains, vessels, farm
equipment...), aeronautical/maritime tracking systems, and in disaster
management scenarios, since they can ensure connectivity in remote areas where a
terrestrial infrastructure is difficult or impossible to deploy or even
transport, or, in any case, they can provide a complementary role to 5G
terrestrial networks. For this kind of application, the use of High Altitude
Platforms (HAPs) or Low/Medium Earth Orbit (LEO/MEO) constellations is
recommended since they can deliver a high throughput service with low latency.

SatComs can therefore extend and complement terrestrial networks in unserved or
under-served geographic areas. In fact, standardization actors, such as 3GPP,
have begun to design solutions to use these new communication paths. In the case
of cellular networks, the novel Work Item on Non-Terrestrial Networks aims to
introduce a satellite component in the 3GPP 5G standard (New Radio, as per 3GPP
nomenclature). However, typical satellite channel impairments, as large path
losses, variable delay, and Doppler shifts, pose severe challenges to the
realization of a satellite-based 5G network. 

The core goal of the ICARUS project
is to enable solutions for high bandwidth SatComs in under-served areas for
fleets of vehicles. The design of a comprehensive solution in this context
requires close cooperation between multiple knowledge areas, going from the
physical substrate to the more abstract technologies dealing with application
logic. Thus, the proposed system could leverage the high capacity of the Ka
frequency band in the radio link, employ advanced medium access control (MAC)
protocols with improved efficiency, exploit the existence of
inter-satellite-links (ISL), and take advantage of the resiliency and native
multicast capabilities of the information centric networking (ICN) paradigm. In
particular, the project will address the following technical challenges: 

* The use of higher frequencies in the millimeter bands, mmW, more specifically,
  Ka- and, eventually, Q/V or W-band, poses new challenges. Furthermore, given
  the lack of measurements from non-GSO (non-Geostationary orbits), existing
  channel models are not totally suitable for the new satellite networks made up
  of several non-GSO satellites. Even though there have been a number of
  experiments, the most recent one ESA's Alphasat, where tropospheric effects
  have been assessed at mmW, there is a lack of solid knowledge of the effects
  on non-GEO configurations, especially LEO, given the very short passage times
  over the measurement earth station. Problems arise from the varying path
  length to be expected from rise to setting of the satellite on the local
  horizon, the presence of faster scintillations in clear air conditions and
  different dynamics of rain attenuation due to the fast passage of the
  satellites. This also includes the spatial structure of rain cells for
  hand-over, thus avoiding deep fade events. All these and other effects, to be
  mentioned later in this proposal, have an impact on the link budget (reduction
  and fast variations of available margins) as well as in the application of
  Fade Countermeasures (FCM) such as Adaptive Coding and Modulation (ACM). **New
  experimental channel data and models** are thus required for the initial
  phases of system conception. This also includes the development of time-series
  simulators for dynamic system assessment through software and hardware
  emulators.

*  Develop **new MAC protocols** for data transmission from the user terminals
   to the satellite constellation. In this direction of the communication, the
   satellite channel will be shared by a large number of terminals extended over
   a wide area trying to send small amounts of data occasionally, but the number
   of nodes and their geographic distribution is unknown and continually
   changing. To complicate the scenario even further, the relatively high delays
   in the satellite channels and the increased Doppler effects, especially with
   LEO/MEO constellations, impose an extra challenge from the MAC sublayer
   viewpoint. All these factors make the design of a MAC protocol for upstream
   transmission both critical and challenging. In this project we will search
   for advanced MAC protocols that can adapt to a variable number of mobile
   devices in a scenario with high power imbalance conditions, uneven long
   delays and poor-quality channel estimations. 

*  Design mechanisms for the **efficient transmission of legacy IP traffic over
   an ICN backend.** Even though the ICN networking paradigm provides clear
   advantages over the current IP networking stack, it cannot be expected that
   it will replace the current IP-based technologies overnight. So, any new
   networking technology must be capable of carrying current network traffic
   with negligible degradation. This part of the project will define
   translations mechanisms to map IP traffic to ICN concepts. It is a secondary
   goal for these translation mechanisms to be able to take advantage of the
   mobility, multi-path and multicast capacities of the ICN substrate so that
   even legacy traffic can receive a better service than what would otherwise be
   possible with a standard IP stack. 

*  Develop new **routing protocols** for multi-hop traffic transmission in the
   satellite network. Data transmission inside a swarm of satellites, each
   acting as an individual router, and with constant neighboring changes due to
   their inherent mobility, cannot rely on the same solutions as a classical
   static network. In a Satcom network, however, the mobility patterns are
   predictable and thus the solutions have to be different from those of other
   mobility scenarios, such as mobile wireless sensor networks, if we are to
   obtain the best possible performance. The usage of an ICN network further
   complicates the issue. In an ICN network, information must follow the reverse
   path of interest queries or this traffic will not be able to reach the
   original requesting clients. Due to the highly dynamic topology, it is
   possible that the satellite servicing a given client when a request was made
   gets replaced by a different satellite when the requested information is due
   to arrive. In this project we will propose modifications to the routing
   mechanisms of ICN networks to overcome this issue. 

*  Create a **simulation testbed** of the whole system. As it is not possible to
launch a satellite constellation in order to test all the project contributions,
we will augment an existing discrete network simulator, such as with mobility
models to simulate the position of the individual satellites, an accurate model
of the Ka-band both in the inter-satellite and in the satellite-ground
directions and updated routing software for the ICN routers. We will employ the
testbed to obtain performance measures of the transmission of legacy IP traffic
over the SatCom using as traffic sources/destinations individual nodes of a
transport fleet.


