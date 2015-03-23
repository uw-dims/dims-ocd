.. _newsystem:

Concept for a new or modified system
====================================

.. todo::

   This section shall be divided into the following paragraphs to describe a
   new or modified system.

..

.. _backgroundobjectivesscope:

Background, objectives, and scope
---------------------------------

.. todo::

   This paragraph shall describe the background, mission or objectives, and
   scope of the new or modified system.

..

#. The DIMS system must have the ability to process structured data that is
   entered into the system in one of several ways: (1) attached to email
   messages being sent to the Ops-Trust portal (optionally as encrypted
   attachments); (2) via CIF feed, TAXII, AMQP message bus, or other
   asynchronous automated mechanism; (3) as uploaded from a user’s workstation
   via the DIMS dashboard client; (4) via the Tupelo client or other command
   line mechanism.

#. The DIMS system must have the ability to store additional attributes for
   each user (such as which CIDR blocks they are responsible for protecting,
   which top level Domain Name System domains, and/or which high-level
   activities (e.g., campaigns) they wish to monitor. This capability allows
   the system to notify the user when there are messages or email threads of
   interest, and to facilitate providing regular tailored reports or alerts
   about activity of interest to them. These attributes also support the basis
   for role-based access controls. This real-time situational awareness
   capability is one of the most important features that will improve response
   and reaction time, as it removes the necessity to read and process every
   single message that flows through the system at a given time, or to manually
   trigger reports or searches to get situational awareness.

#. The DIMS system must be able to detect when IP addresses or domain names
   associated with a given set of CIDR blocks or top-level domains are
   involved, and to trigger one or more workflow processes. This could be to
   send an alert to a user when some entity they are watching is found in a
   communication, generate a scheduled report, or trigger some other
   asynchronous event. It may be to initiate a search of available data so the
   results can be ready for a user to view when they receive the alert, rather
   than requiring that they initiate a search at that time and have to wait for
   the results.

#. The DIMS system must have the ability to process structured data attached to
   email messages being sent to the Ops-Trust portal (optionally as encrypted
   attachments), identified by a tag in instant messages or IRC chat (e.g., a
   URL referencing a data file in a Redis or other `NoSQL` database), as well
   as detecting when IP addresses or domain names associated with a given set
   of CIDR blocks or top level domains are found in arbitrary text streams. 

#. The DIMS system must be able to keep track of multiple incidents, campaigns,
   sector-specific threat activity, or other ad-hoc groupings of security
   information as desired by DIMS users. For example, an analyst may wish to
   track ZeroAccess trojan activity, CryptoLocker extortion attempts, Zeus or
   Citadel ACH fraud attempts, etc., possibly over time periods measured in
   years.  Each user may wish to label these associated sets with their own
   labels, or may want to use a system-wide naming scheme that conforms to an
   ontology that is more rigorously defined. These sets should be easily shared
   with other users.

#. The DIMS system should support knowledge acquisition by allowing the user to
   be told, on login and when they focus on a particular incident or campaign,
   what new information has been obtained from other users of the system (or
   the system itself through automated detection and reporting) since the last
   time the user was reviewing the incident or campaign. Collaboration works
   best when team members learn from each other, and the asynchronous nature of
   a multi-user system is such that determining the delta in knowledge since an
   earlier point in time is difficult to achieve. (This is related to the issue
   of tracking incoming information in email threads listed earlier.)

#. The DIMS system should summarize any/all aggregate data that any user is
   presented with sufficient context to quickly understand the data. This
   includes (but is not limited to): Start and end date and time; Total number
   of systems within the `friend` population, and how they break down across
   participants; Total number of systems outside of the `friend` population,
   and how they break down by country/AS/IP address(es); Total number of
   systems from the `not-friend` population that are known to be malicious
   (a.k.a., `foe`), broken down by country/AS/IP address(es). When the number
   of IP addresses exceeds a certain threshold, they are summarized in
   aggregate, with a mechanism to dig down if the user so chooses. Similarly,
   context about what quantity and quality of malicious activity that is known
   about the `foe` population should also be available for easy access
   (presented if short, or drill-down provided it too voluminous). This amount
   and level of detail provides an overall `situational awareness` or scoping
   of for large volumes of security event data.  (The mechanism for such
   multi-level tabular reports is known as `break`  or `step`  reports).

#. The DIMS server components must be provisioned, configured, and administered
   from a single central location and pushed to servers in an automated
   fashion. Manual configuration and patching of hosts takes too much expert
   system administration knowledge, incurs too much system administration
   overhead, and takes too long to recover from outages or system upgrades. The
   DIMS team will be administering multiple instances of the DIMS system (for
   development, alpha testing, beta testing, a "production" PRISEM instance for
   in-field test and evaluation, and potentially 3-5 more instances at other
   regions (see the Stakeholders section). It will be impossible to manually
   manage that many deployments with current staffing levels.

#. The systems running DIMS software must support continuous integration of
   code releases, updating runtime executables, stopping and starting service
   daemons, etc., in a controlled and repeatable manner. Runtime components
   must identify the source code release from which they were built in order to
   track bugs and features across multiple deployments with a regular release
   cycle measured in weeks (2-4 weeks is anticipated). The system will be built
   using an Agile coding methodology, responding to user feedback as quickly as
   possible to ensure maximum usability and scalability.




Operational policies and constraints
------------------------------------

.. todo::

   This paragraph shall describe any operational policies and constraints that
   apply to the new or modified system.

..

Description of the new or modified system
-----------------------------------------

.. todo::

   This paragraph shall provide a description of the new or modified system,
   identifying differences associated with different states or modes of
   operation (for example, regular, maintenance, training, degraded, emergency,
   alternative-site, wartime, peacetime). The distinction between states and
   modes is arbitrary. A system may be described in terms of states only, modes
   only, states within modes, modes within states, or any other scheme that is
   useful. If the system operates without states or modes, this paragraph shall
   so state, without the need to create artificial distinctions. The
   description shall include, as applicable:
    
   + The operational environment and its characteristics
     
   + Major system components and the interconnections among these components
      
   + Interfaces to external systems or procedures
   
   + Capabilities functions of the new or modified system
   
   + Charts and accompanying descriptions depicting inputs, outputs, data flow,
     and manual and automated processes sufficient to understand the new or
     modified system or situation from the user's point of view
   
   + Performance characteristics, such as speed, throughput, volume, frequency
     
   + Quality attributes, such as reliability, maintainability, availability,
     flexibility, portability, usability, efficiency
     
   + Provisions for safety, security, privacy, and continuity of operations in
     emergencies

..

.. _users:

Users/affected personnel
------------------------

.. todo::

   This paragraph shall describe the types of users of the new or modified
   system, including, as applicable, organizational structures,
   training/skills, responsibilities, and interactions with one another.

..

The full list of stakeholders includes:

#. *PRISEM participants*: Existing participants in the PRISEM project in the
   Puget Sound will be the primary users of the DIMS system. DIMS is being
   designed to provide them with advanced mechanisms for rapid response,
   situational awareness, and communication within the trusted group. Next
   highest priority is to provide structured data interchange between the
   existing Ops-Trust portal and the DIMS system, allowing lateral sharing of
   IOCs and observables between the existing Ops-Trust community members and
   PRISEM participants as allowed by policy (or with redaction and/or
   anonymization, as appropriate.) Some features added to the Ops-Trust portal
   by the DIMS project team will be integrated in such a manner that they are
   available to Ops-Trust members without having to use the DIMS front end
   software. Those users who are not part of the existing Ops-Trust community,
   or Ops-Trust members willing to learn a new interface, can use the DIMS
   front end and will have access to a larger set of features than are
   available via the normal Ops-Trust services.

#. *PRISEM Administrators and DIMS developers*: Related to the PRISEM
   membership is an entity being formed to administer the PRISEM model in the
   form of a not-for-profit organization responsible for daily operations,
   system administration, provisioning of SIEM collectors and SIEM
   configuration, training, etc. This entity is still being formulated and does
   not exist today (however it is likely to exist before the end of the option
   year for the DIMS project.) The DIMS developers will also serve as system
   administrators, trainers, and user support for the initial DIMS deployment
   while the PRISEM stand-alone entity is being stood up.

#. *US-CERT*: Provides IOCs in STIX format to PRISEM participants as part of an
   existing Cooperative Research and Development Agreement (CRADA) between
   US-CERT and the PRISEM project. 

#. *Ops-Trust*: This is a community of several hundred operational security
   professionals from the private sector, academia, etc. They currently share
   information in ad-hoc ways, primarily through email communications and IRC
   chat.

#. *NCFTA*: This is a federal government and industry collaborative
   organization primarily focused on computer crime related information sharing
   and analysis. They are located in Pittsburgh, Pennsylvania, but interact
   with corporate and government entities from a number of countries. NCFTA has
   complementary needs to those of the PRISEM participant base (though focused
   more on investigation than day-to-day monitoring). They are eager to take
   advantage of features provided by DIMS that support the investigator and
   analyst use cases. They have offered to compare requirements and use cases
   to their own needs, to help test new Ops-Trust and DIMS features, and
   provide feedback for test and evaluation of DIMS products.

#. *Western Cyber Exchange* (WCX): WCX is a non-profit entity located in
   Colorado Springs, Colorado, that integrates horizontally on a cross-sector
   and regional basis to allow for non-traditional information sharing between
   government and industry. They have expressed an interest in replicating the
   PRISEM model and in participating in DIMS software development and testing.
   Web site: wcyberx.org 

#. *True Digital Security*: True Digital provides network security assessments,
   vulnerability analysis, network security monitoring. They operate in the
   Tulsa, Oklahoma region. Like WCX, they have expressed an interest in
   replicating the PRISEM model and in participating in DIMS software
   development and testing. Web site: truedigitalsecurity.com

#. *United States Secret Service*: Federal law enforcement agency who would
   consume cybercriminal case information from victimized SLTT entities
   (such as the PRISEM user base an other similar stakeholder groups).
   They operate on a similar model to the UC1 and UC3 entities shown
   in Figure :ref:`stixusecases`, only focused on criminal investigative
   and national security situational awareness tasks and not security
   operations tasks like other federated groups like ISACs.


.. _support:

Support concept
---------------

.. todo::

   This paragraph shall provide an overview of the support concept for the new
   or modified system, including, as applicable, support agency(ies);
   facilities; equipment; support software; repair/replacement criteria;
   maintenance levels and cycles; and storage, distribution, and supply
   methods.

..
