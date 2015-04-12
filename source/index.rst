.. DIMS Operational Concept Description documentation master file.

.. _dimsoperationalconceptdescription:

================================================
DIMS Operational Concept Description v |release|
================================================

.. topic:: Executive Summary

    Since HSPD-7 was released in 2003, the Department of Homeland Security has
    had a core mission of working to protect the nation’s critical
    infrastructure. In 2008, the *National Response Framework* was released, and
    a project to take tools developed by DHS Science and Technology for use in
    federal government networks and put them in the hands of *State, Local,
    Territorial, and Tribal (SLTT)* government entities – known as the *Public
    Regional Information Security Event Monitoring (PRISEM)* project – was
    initiated. The intent of the *PRISEM* system is to combine standard security
    devices event log data using a commercial *Security Information Event
    Management (SIEM)* system, fed in part by event log data from the DHS-funded
    NetFlow based system (formerly known as :term:`Einstein 1`), correlating these
    events using the SIEM to detect structural bot activity that has a high
    probability of being an infected computer. It uses the *Collective
    Intelligence Framework (CIF)* database system to produce watchlists for
    real-time monitoring, as well as to provide historical attack context. A
    geographic front end provides a regional context to alerts in the system
    for at-a-glance situational awareness. The system now allows indicators of
    compromise (IOCs) to be used for both finding events that were missed in
    the past and/or watching for new events in the future.

    DHS efforts with MITRE to develop information sharing mechanisms based on
    the *Structured Threat Information eXpression (STIX)* format, leveraged by a
    *Cooperative Research and Development Agreement (CRADA)* between US-CERT and the
    PRISEM Project, are underway to bring de-classified *Indicators of
    Compromise (IOCs)* and *Observables* from DHS and FBI to regional SLTT
    government entities for confirmation of involvement of threat actors of
    national interest. As sharing of these IOCs and Observables is extended
    laterally to similar regional collaborative efforts, national scope and
    visibility of the impact of widespread threats becomes possible.

    The *Distributed Incident Management System (DIMS)* project is intended
    to take this semi-automated sharing of structured threat information,
    building on the success of the PRISEM project and leveraging an existing
    community of operational security professionals known as *Ops-Trust*, and
    scale it to the next level. DIMS will take advantage of the open "message
    bus" architecture used by PRISEM, features that support "identification of
    friend or foe," and the ability to integrate three data sources maintained
    by PRISEM (network flow history, event history, and attacker context
    history) to support the triage process, cross-organizational correlation of
    events, and anonymization to promote privacy-sensitive sharing of security
    event data. Working with the use cases defined by MITRE and PRISEM users,
    building the features necessary to simplify structured information sharing,
    and operationalizing these within these existing communities, will allow
    DIMS to fill existing gaps in capabilities and support existing missions
    that are slowed down today by many complicated, manual processes.

.. toctree::
   :numbered:
   :maxdepth: 2

   scope
   referenceddocs
   currentsystem
   justifications
   newsystem
   operationalscenarios
   impacts
   analysis
   notes
   license
   appendices

