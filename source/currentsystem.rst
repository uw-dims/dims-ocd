.. currentsystem:

Current system or situation
===========================

Background, objectives, and scope
---------------------------------

Homeland Security Presidential Directive 7 (`HSPD-7`_), released in 2003, set
in motion a number of policy changes and created awareness of a new problem --
the term for which is now ingrained into our lexicon: critical infrastructure
protection. That document specifies the actions to be taken to identify,
prioritize, and address the vulnerabilities to the systems and services that
have relevance to the American way and quality of life. Local (city and county)
government provides systems and services that maintain and improve the quality
of life at the scale at which citizens identify most directly. eGovernment
services allow citizens to pay bills, obtain a business license, communicate
with elected officials, etc. Local government arguably maintains 85% of
critical infrastructure, yet its protection is largely unaddressed. While the
rest of the world is focused on nation-state hackers versus Supervisory Control
and Data Acquisition (SCADA) systems or cardholder data breaches, local
governments with their silos, poor budgets and priorities that change with the
political wind are attempting to protect water purification, traffic
management, public safety communications and a great many other services -- the
loss of which would arguably have an impact including loss of life. Local
government is acknowledged in HSPD-7 as being integral to critical
infrastructure protection, however no reasonable effort has been made to
address cyber defenses on the local scale. Efforts to date to secure cyberspace
have called for a comprehensive system that protects federal government
agencies. A "comprehensive system" for securing the United States electronic
infrastructure that does not include local governments, however, is not truly
comprehensive.

Taking this all into consideration, two things become clear:

+ Critical infrastructure dependencies on local government must be addressed

+ Local governments need assistance with detective controls -- security
  monitoring -- and with response capabilities

Both these issues may be addressed by extending a concept that is common to
corporate IT organizations into the local government sector: managed security
service. Specifically, were a central location available for securely routing
activity logs, firewall and IDS alerts, and other forms of information
typically collected (but not analyzed) on networks, and then made available to
local governments as near real-time alerts and a portal for situational
awareness, the gaps between the criticality of the systems and services, and
the degree to which critical infrastructure elements are being protected can be
addressed.

The Public Regional Information Security Event Management (PRISEM) system was
designed to address gaps in capabilities between federal and local government
entities. PRISEM extends a concept common to corporate IT organizations –
managed security services – into the local government sector. It enhances
security oversight and controls and improves the ability to detect and respond
early to threats against critical infrastructure. It moves beyond basic
information sharing and creates an action-oriented alliance that leverages
limited expertise across resource-constrained local government IT
organizations. It creates a partnership between a top-tier research university,
federal law enforcement fusion center, and private sector organizations. Its
benefits will include increased security and compliance capabilities, increased
productivity, improved performance, and lower costs for participants.

The intent of the PRISEM system is to combine standard security devices event
log data using a commercial Security Information Event Management (SIEM)
system, fed in part by event log data from the DHS-funded NetFlow based  system
(formerly known as :term:`Einstein 1`), correlating these events using the SIEM to
detect structural bot activity that has a high probability of being an infected
computer. It uses the Collective Intelligence Framework (CIF) database system
to produce watchlists for real-time monitoring, as well as to provide
historical attack context. A geographic front end provides a regional context
to alerts in the system for at-a-glance situational awareness. The system now
allows indicators of compromise (IOCs) to be used for both finding events that
were missed in the past and/or watching for new events in the future.

The primary mission of the PRISEM system is threefold:

+ To *enhance the information security capabilities* of local government and
  address exposures to critical infrastructure, systems and services without
  significantly raising cost, by providing the means to obtain visibility into
  attacks against information technology resources;

+ To *provide a method for reporting* cyber-security event or trend information
  in a consistent and automated fashion, for further evaluation by intelligence
  or law-enforcement communities in a manner that is respectful of national and
  international standards of individual privacy; and

+ To *create an action-oriented operational setting* for the deployment of
  research-grade technologies that were funded by the federal government, in
  order to evaluate their effectiveness and assist with their transition into
  commercial products.

PRISEM is the first regional government collaboration to enter into a
Cooperative Research and Development Agreement (CRADA) with US-CERT to receive
de-classified IOCs. The intent is to receive and send these indicators using
MITRE Corporation’s Structured Threat Information eXpression (STIX) format. The
goal is to eventually link the IOCs with Tools/Tactics/Procedures (TTPs) and
Courses of Action (CoA) to provide actionable intelligence to PRISEM members
(see Figure 2).

In 2008 DHS released a document called the National Response Framework (FEMA,
2008). The relationship building between hometown security and Homeland
security began to form an enduring partnership.  As part of its commitment to
hometown security, "DHS has worked to get tools, information, and resources out
of Washington, D.C. and into the hands of our federal, state, local, tribal and
territorial law enforcement partners."  The PRISEM project, initiated this same
year, is an example of this effort to bring these resources to the SLTT
government level. It has served this purpose, but to date only in the Puget
Sound region.  Fast forward to February 2013. The President of the United
States issues two new policies: 1) Executive Order 13636: Improving Critical
Infrastructure Cybersecurity 2) Presidential Policy Directive 21: Critical
Infrastructure Security and Resilience.

These two documents (known as *EO 13636* and *PPD 21*) reflect the
acknowledgement that:

+ America's national security and economic prosperity are dependent upon the
  operation of critical infrastructure that is increasingly at risk to the
  effects of cyber attacks.

+ The vast majority of U.S. critical infrastructure is owned and operated by
  the private sector and/or State, Local, Territorial, and Tribal (SLTT)
  government entities, not by the federal government.

+ A strong partnership between the public and private sector, as well as
  between SLTT government entities in regions of the country, is crucial in
  reducing the risk to these vital systems.

Knowledge is becoming a critical success factor for organizational performance.
Many public and private organizations are sharing knowledge as one of the means
to collaborate and gain sustainable competitive advantage over these threats.
Advances made in information and communication technology (ICT) is aiding these
efforts. The need for infrastructure protection and real-time to near-real-time
automated response to cyber threats to enable expedient top-level decisions has
become imperative. However, a widely accepted framework for visualization,
analytics, situational awareness, enabling intraregional response to shared
threats does not exist today. To address these concerns, a system called the
Distributed Incident Management System (DIMS) will be built. DIMS will be based
mostly on existing technology and emerging standards. The primary users of DIMS
are the Computer Security Incident Response Teams (CSIRTs) who need to maintain
the security and functionality of a diverse and complicated, yet
institutionally critical cyber infrastructure. DIMS will be based on open
source technology and standards.


Operational policies and constraints
------------------------------------

Policies
~~~~~~~~

+ EO 13636 and PPD 21 provide guidance on how the federal government will work
  with private sector operators of critical infrastructure systems in order "to
  prepare for, prevent, mitigate, and respond to threats."

+ Policies for each of the SLTT government and private sector entities
  participating in the PRISEM system, and the PRISEM participant agreement,
  have privacy impacts when sharing information outside the project.

Assumptions
~~~~~~~~~~~

+ It is assumed that the Ops-Trust portal system will be easy enough to
  refactor to accommodate the required API for user interface enhancements that
  underlie the DIMS front-end.

+ In addition, a successful application penetration test result (and
  remediation of critical security flaws that these tests may uncover) is a
  pre-requisite for the Ops-Trust stewards to allow the code to be released to
  the general public.

+ We assume that the stakeholders who have expressed an interest in providing
  requirements and beta-testing feedback will follow through. It will be
  important to have at least two groups (beyond the Ops-Trust community and
  US-CERT) perform some "live-fire" structured information sharing experiments
  in order to fully exercise the data sharing aspects of DIMS. It is hoped that
  an organization like NCFTA, who is already familiar with the Ops-Trust portal
  system, can facilitate development and testing of the specific information
  sharing features that are part of their daily business processes.

Constraints
~~~~~~~~~~~

+ The DIMS team is operating under an NDA with the City of Seattle for access
  to their data in the PRISEM system for development purposes. Anonymization
  features described in this document are intended to facilitate sharing within
  these policy constraints.

+ The DIMS team is operating under an NDA with the Ops-Trust organization for
  access to the source code for their portal. Ops-Trust will decide when and
  how to release the source code to the general public, pending modifications
  and application penetration testing to be performed by the DIMS team.

+ The DIMS team is operating under export control restrictions that apply to
  any/all encryption software used in the system. Based on consultation with UW
  Export Control authorities, the DIMS team will design the system such that it
  can be released as open source without encryption software included (but will
  list its pre-requisite status, where it can be obtained, and how it can be
  installed by the end user), or will deliver pre-installed/configured versions
  of the system only under export control restricting agreements negotiated by
  the appropriate authorities at the UW.


Description of current system or situation
------------------------------------------

.. todo::

    This paragraph shall provide a description of the current system or
    situation, identifying differences associated with different states or
    modes of operation (for example, regular, mainte-nance, training, degraded,
    emergency, alternative-site, wartime, peacetime). The distinction between
    states and modes is arbitrary. A system may be described in terms of states
    only, modes only, states within modes, modes within states, or any other
    scheme that is useful. If the system operates without states or modes, this
    paragraph shall so state, without the need to create artificial
    distinctions. The description shall include, as applicable:

    + The operational environment and its characteristics

    + Major system components and the interconnections among these components

    + Interfaces to external systems or procedures

    + Capabilities functions of the current system

    + Charts and accompanying descriptions depicting inputs, outputs, data flow,
      and manual and automated processes sufficient to understand the
      current system or situation from the user's point of view.

    + Performance characteristics, such as speed, throughput, volume,
      frequency

    + Quality attributes, such as reliability, maintainability, availability,
      flexibility, portability, usability, efficiency

    + Provisions for safety, security, privacy, and continuity of operations in emergencies

..

More specifically, there are gaps in functionality in the existing sub-systems
that DIMS will address. The three primary sub-systems are: (1) the Ops-Trust
portal; (2) The Collective Intelligence Framework (CIF) database; and (3) the
PRISEM system. Each of these will be examined in turn.

Ops-Trust portal Code Base
~~~~~~~~~~~~~~~~~~~~~~~~~~

+ Handles adding users by nomination + vouching workflow processing
+ Segregates trust groups (public or hidden) per administrator defined policy
+ Facilitates encrypted communication via email, and out-of-band contact via phone, IM, etc.
+ Provides a secure wiki for holding information contributed by users and other group knowledge
+ Holds attributes about users:

    + Name, nick-name (handle) to identify them in wiki
    + Telephone number for out-of-band communication
    + Closest airport to facilitate meeting in person when on the road
    + PGP (or GPG) encryption key
    + Instant messaging system username

What does the Ops-Trust portal do now?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The Ops-Trust portal currently does a good job of the nomination and vouching
workflow that allows user accounts to be set up and attributes populated. It
then does a good job of segregating trust groups from each other, including
facilitating encrypted email communications and storing data in a wiki.

There are several weaknesses or limitations to the way the Ops-Trust portal
works and is used. All IOC data is passed around at present is in arbitrary
forms (ASCII text columnar data in random field orderings, CSV files, PDF
files, etc.) and may be in the body of an email, as a MIME attachment, or in a
file specified by a URL in the body of the message. Often long lines of
columnar data get wrapped and are difficult to read or parse with scripts.
Cutting/pasting into security systems is difficult, if not impossible when
thousands of lines of data are included in some random field in a large
columnar list. Traffic Light Protocol (TLP)  tagging is done in random ways (if
done at all), and TLP tags in the body of a message do not get included when an
attached file is saved to disk. The subject line of emails includes the list
and it, and the list trailer at the bottom of the email, must be manually
scrubbed when forwarding a message off-list. Users must read every message in a
thread in order to keep up on new data that may involve hosts or networks that
the reader is responsible for protecting, and widespread and rapidly
progressing events can generate dozens or even hundreds of messages in a day,
which is difficult to keep up with.

What is lacking from the Ops-Trust portal?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The principle mechanism lacking from the Ops-Trust portal is the ability to
pre-process IOC data sent by users so as to notify each user when a thread
pertains to them (because IOCs match pre-defined lists that the user cares
about), and more specifically, which email messages contain IOCs of interest.
The data necessary to do such filtering and altering is not stored in the
Ops-Trust portal database, nor is there a standardized mechanism for passing
machine-parseable data into the portal to facilitate workflow automation. The
Ops-Trust portal is also monolithic and focused on managing the trust groups
and users, not on making data analytics and visualization capabilities
available to help process the IOC data that is available throughout the user
base. It does not have capabilities to anonymize data, nor to associated TLP
tags with data such that filtering and anonymization does not rely solely on
humans knowing when/how to filter and anonymize data, and on them never making
mistakes.

How does it need to change?
^^^^^^^^^^^^^^^^^^^^^^^^^^^

The Ops-Trust portal, written in Perl with a PostgreSQL database backend, needs
to be refactored, using a model-view-controller framework (MVC) framework such
as Catalyst (http://www.catalystframework.org/), to separate the front end UI
capabilities from the back-end database and portal workflow processes so as to
provide an API that alternate UI components can access via a standardized
mechanism such as a RESTful HTTPS interface. The UI needs to be refactored to
improve usability and provide access to both user and administrator functions.
It needs to have additional user attributes added to facilitate the filtering
and notification process described above, as well as to have workflow
processing features added to perform some of the manual filtering and searching
capabilities. The account management features need to be extended to support
AAA and RBAC features that use mechanisms such as roles and TLP tagging to
ensure exported data is filtered and/or anonymized in accordance with
user-defined policies. Once the MVC conversion has been completed, and some of
the additional attributes and features necessary to semi-automate information
sharing, an application penetration test needs to be performed to satisfy
requirements of the authors for publicly releasing the code as an open source
project.

Why is this relevant?
^^^^^^^^^^^^^^^^^^^^^

Adding features to enable trusted sharing of machine-parseable IOCs between
instances of the Ops-Trust portal makes it possible to scale trusted
information sharing to a larger population than the existing Ops-Trust group is
capable of growing. Having additional attributes for users enables workflow
automation of notification of IOCs relevant to their constituencies, which
speeds response. Eventually, features that ensure the chain-of-custody and
provenance of security data that can be used as evidence in criminal or civil
legal proceedings, combined with the machine-parseable nature of the data
exchange, will facilitate reporting computer crimes to law enforcement in a
manner that speeds their investigations and helps more accurately scope and
prioritize investigations.

COLLECTIVE INTELLIGENCE FRAMEWORK (CIF) DATABASE
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

+ "Indicators of Compromise"
+ Hashes of malicious software
+ IP addresses, CIDR network address blocks, and DNS domain names associated with malicious activity (e.g., from sandboxes)
+ Builds context about attacker activity over time
+ Produces feeds of indicators for watchlists, searching hard drives, rules for security devices, etc.

What can CIF do now?
^^^^^^^^^^^^^^^^^^^^

CIF provides a database of historic IOCs obtained from feeds that it consumes
on a regular basis. In turn, CIF produces feeds of IOCs that can be used for
watchlists, access control lists, IPS rules, etc. The PRISEM system uses CIF to
produce watchlists that are used by the Python based :term:`Botnets System` detectors
processing real-time NetFlow V5 records sent from network devices for real-time
detection of suspect flows. CIF correlates data in its tables, associating IOCs
from multiple sources, as well as enriching the data by looking up ASNs, domain
name to IP address associations, etc. Users can enter IOC data using CIF’s
browser plug-in, the CIFglue application from Verizon, or through the CIF API.

The PRISEM system also processes "SEARCH" records that are added to CIF when
someone searches, putting those IP addresses or CIDR blocks that are searched
for, but produce no results, into a watchlist. A more accurate way to do this
is to have users explicitly put suspicious IP addresses or CIDR blocks into CIF
with special tagging that is then used to generate a watchlist.

What is lacking from CIF at present?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

While not a lack of features in CIF, per se, the way CIF is being used is
lacking in potential. While the PRISEM uses CIF to generate watchlists for
real-time network flow detectors, and creates a special watchlist for "SEARCH"
records as described above to watch for highly suspicious events, PRISEM users
(and the vendor portal) are not taking advantage of the full power of
watchlists because users must know how to manually enter data using one of the
secondary CIF-specific mechanisms listed above as the vendor portal does not
currently provide this ability.

CIF is also not being used to store security event information related to
alerts that are positively identified by analysts as being true-positive
indicators of compromise (or confirmation of IOCs sent to the system or entered
manually by analysts.) Were these events to be stored, they would be correlated
with other IOCs and could be published as a feed to interested outside parties.

How does it need to change?
^^^^^^^^^^^^^^^^^^^^^^^^^^^

It is unknown how much data can be put into CIF before it reaches performance
or storage limits. As part of the PRISEM deployment of CIF, mechanisms were put
in place to regularly log the sizes of certain database tables and the database
itself, and to log the amount of time it takes to pull feeds from outside
sources, to perform correlation, and to index database tables (all processes
that run from :term:`cron` on a scheduled basis). This information has only been used
to answer questions at given points in time, but the intention was to perform
linear regression on this data on a regular basis to estimate when resource
limitations will be hit (e.g., when the disk drive is expected to be filled to
100%, or when the CPU processing capacity approaches 100% on a continual
basis.) This would allow better monitoring of resources, tuning of system
parameters, and estimation of hardware capacity required as the PRISEM
population increases. All of these features would be made available to the CIF
developers to extend the capability of all CIF users to be pro-active about
their deployment infrastructure.

Why is this relevant?
^^^^^^^^^^^^^^^^^^^^^

As CIF is a "work in progress" and constantly undergoing development, the
community of users is often called upon to help identify bug fixes and feature
additions that can be made available to the CIF development team via :term:`Git` "pull"
requests. This helps improve the generally available release of CIF and
minimizes the need to maintain add-on patches independent of CIF releases.
Since the intention of DIMS is to be replicated in many regions, each of which
constitutes a different mix of participants, security data sources feeding the
central SIEM, etc., mechanisms to better identify capacity requirements and
monitor runtime resource usage for minimum downtown becomes critical. The same
machine learning algorithms used for resource monitoring are also useful for
clustering and classification of security event data, so their implementation
in a generalized framework increases the flexibility of their application.

THE PRISEM SYSTEM
-----------------

+ Event collection, correlation, archiving
+ Distillation of hundreds of alerts per day from (low) tens of millions of events per day
+ Integrates the NetFlow :term:`Botnets System` behavioral detection capability
+ Requires intensive administration and coding when provisioning new tenants
+ Proprietary vendor portal the principal user interface

What can PRISEM do now?
^^^^^^^^^^^^^^^^^^^^^^^

The PRISEM system has demonstrated that sharing event logs within a trust
community improves the situational awareness across regional SLTT government
entities, that collaborative response improves everyone's capacity to respond
and recover, and that situational awareness reports being fed back to the
federal government through participation in Fusion Center activities. There are
as many as five regional SLTT collaboration efforts that the PRISEM leadership
has interacted with and who have expressed an interest in replicating what has
been done within PRISEM (see Section :ref:`` 2.2 Users and Other Stakeholders).

.. todo::

   FIX CROSS REFERENCES

..

What is lacking from PRISEM at present?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

There are limitations in what PRISEM is capable of doing, primarily based on
the commercial off the shelf SIEM system at its core, and the reliance on a
proprietary vendor portal for the user interface that PRISEM participants use
on a daily basis. There is no flexible and secure real-time communication
vehicle that PRISEM participants use on a regular basis, and interaction among
PRISEM participants and analyst resources could be much higher. Also related to
the use of the vendor portal is a limitation on the visualization and analytic
capabilities. The portal only supports what the vendor has programmed it to
support. There is no easy way to integrate newly developed features,
visualization tools, or analytic algorithms that operate on the PRISEM
datasets.

How does it need to change?
^^^^^^^^^^^^^^^^^^^^^^^^^^^

The underlying inter-process communication added to the PRISEM system in recent
months provides a flexible and extensible mechanisms for Remote Procedure Call
(RPC) invocation, as well as logging of information about queries and response
times that can serve to estimate wait times for longer queries. This message
bus architecture is also programming language agnostic, operating system
agnostic, and is using a structured command structure that allows
self-description of the data being sent between programs to facilitate merging
results from multiple processes (e.g., the “identify friend or foe” capability,
anonymization and statistics, partitioning and filtering based on participant
network allocation attributes, etc.) A new user interface that supports all of
these capabilities in a flexible framework architecture will allow seamless
integration between any SIEM product, any vendor portal, and any open source
security tools that are appropriate for processing the kind of data held within
PRISEM.

Why is this relevant?
^^^^^^^^^^^^^^^^^^^^^

Adding a layer of abstraction above the SIEM and vendor portal allows
flexibility for any SIEM, or any managed security service vendor, to be
employed to build a PRISEM-like regional collaborative group. There are many
competitors in this field, and none of them combines the features of universal
compatibility, affordability across the full range of small to large SLTT
collaborative groups, and ease of migration or interoperability as regional
collaborative groups spontaneously form and grow. What do you do if two groups
using two different SIEM products and two different vendor portals wish to
merge? What do you do if the SIEM you are using reaches its end-of-life and is
now longer supported, necessitating a migration of over a year’s worth of
normalized log data to be translated to a new product? What do you do if a
group decides they want to replicate the PRISEM model, and now has to scope out
a SIEM deployment and/or managed security service vendor contract for
provisioning and support? These are all realistic questions, very hard to
answer in the short term, very costly to enter in to, and take a significant
effort to reach a go/no-go decision point. An abstraction layer that focuses on
standardized data interchange, vendor-agnostic interfaces to data, and an open
framework for new features, solves many of these problems and provides the
affordability, flexibility, and scalability that is needed to reach national
scope.



Users or involved personnel
---------------------------

.. todo::

   This paragraph shall describe the types of users of the system, or personnel
   involved in the current situation, including, as applicable, organizational
   structures, training/skills, responsibilities, activities, and interactions
   with one another.

..

Support concept
---------------

.. todo::

   This paragraph shall provide an overview of the support concept for the
   current system, including, as applicable to this document, support
   agency(ies); facilities; equipment; support software; repair/replacement
   criteria; maintenance levels and cycles; and storage, distribution, and
   supply methods.

..

.. _HSPD-7: http://www.dhs.gov/homeland-security-presidential-directive-7
