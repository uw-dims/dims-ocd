.. _justifications:

Justification for and nature of changes
=======================================

.. todo::

   This section shall be divided into the following paragraphs.

..

.. _changejustification:

Justification for change
------------------------

.. todo::

   This paragraph shall:

   + Describe new or modified aspects of user needs, threats, missions,
     objectives, environments, interfaces, personnel or other factors that
     require a new or modified system

   + Summarize deficiencies or limitations in the current system or situation
     that make it unable to respond to these factors

..

PRISEM is the first regional government collaboration to enter into a
Cooperative Research and Development Agreement (CRADA) with US-CERT to receive
de-classified IOCs. The intent is to receive and send these indicators using
MITRE Corporation’s Structured Threat Information eXpression (STIX) format. The
goal is to eventually link the IOCs with Tools/Tactics/Procedures (TTPs) and
Courses of Action (CoA) to provide actionable intelligence to PRISEM members
(see Figure 2).

.. todo::

   FIX FIGURE CROSS REFERENCE

..

In 2008 DHS released a document called the National Response Framework (FEMA,
2008). The relationship building between hometown security and Homeland
security began to form an enduring partnership.  As part of its commitment to
hometown security, "DHS has worked to get tools, information, and resources out
of Washington, D.C. and into the hands of our federal, state, local, tribal and
territorial law enforcement partners." [Dep13]_ The PRISEM project, initiated
this same year, is an example of this effort to bring these resources to the
SLTT government level. It has served this purpose, but to date only in the
Puget Sound region.

Fast forward to February 2013. The President of the United States issues two
new policies:

#. Executive Order 13636: Improving Critical Infrastructure Cybersecurity [Exe13a]_ and
#. Presidential Policy Directive 21: Critical Infrastructure Security and Resilience. [Exe13b]_

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

.. _changedescription:

Description of needed changes
-----------------------------

.. todo::

   This paragraph shall summarize new or modified capabilities/functions,
   processes, interfaces, or other changes needed to respond to the factors
   identified in :ref:`changejustification`.

..

As mentioned in the previous section, MITRE has been working with US-CERT to
develop standards that enable the kind of response and recovery process called
for by EO 13636 and PPD 21. To that end, they have illustrated how STIX can be
applied to four specific use cases that bridge local to national response.
These use cases (shown in Figure 1, taken from the STIX web site) are:
*Analyzing Cyber Threats* (UC1); *Specifying Indicator Patterns for Cyber Threats*
(UC2); *Managing Cyber Threat Response Activities* (UC3); and *Sharing Cyber
Threat Information* (UC4). (MITRE)

.. todo::

   STIX USE CASES FIGURE

..

MITRE defines *observable* as, "[an] event or stateful property that is observed
or may be observed in the operational cyber domain, such as a registry key
value, an IP address, deletion of a file, or the receipt of an http GET. STIX
uses Cyber Observable eXpression (CybOX) to represent Observables."  The
PRISEM system collects logs that contain the IP addresses of the source and
destination of events and flows, along with other information about specific
security events (sometimes including domain names, URLs, services being used,
and observed attack signatures).

MITRE defines *indicator* as, "[a] pattern of relevant observable adversary
activity in the operational cyber domain along with contextual information
regarding its interpretation (e.g., this domain has been compromised, this
email is spoofed, this [:term:`cryptographic hash` of a file] is associated with this trojan, etc.),
handling, etc. An Observable pattern captures what may be seen; the Indicator
enumerates why this is Observable pattern is of interest." (`STIX FAQ #B1`_)
One job of an analyst using the PRISEM system is to take *indicators* that are
shared by outside sources, which are used to trigger alerts within the PRISEM
system, and connect them with those logs that include related observables and
other context (such as the information stored in the Collective Intelligence
Framework database) and distill them into analytic products like situational
Indicators of Compromise, or IOCs, can also be described as "a forensic
artifact or remnant of an intrusion that can be identified on a host or
network. [IOCs] tie to observables and observables tie to measurable events or
stateful properties which can represent anything from the creation of a
registry key on a host (measurable event) to the presence of a mutex (stateful
property)." (Gragido, 2012) IOCs can include several pieces of raw intelligence
that manifest at various points in time on information systems under attack,
including "MD5 [and other :term:`cryptographic hash` values for files], File names, Packer
types, Registry keys, Mutexes, DNS strings, and IP Addresses." (Mandiant, 2011)

IOCs are the lowest-level pieces of evidence used to paint a much larger
picture as part of the response and remediation process (Aldridge, 2012).  They
are the needles to attempt to find in a haystack, not a request to go find
needles. Many of these indicators are found within the file system of a
compromised computer, while others can be found in network flows and server
logs that include transport and network layer information (e.g., IP addresses
and IP protocol and port numbers.)

A workflow or workflow process is the set of steps that someone goes through to
perform a complex task, such as fulfilling an order for an online purchase, or
performing forensic analysis of event logs and network flow data to confirm
compromise, determine root cause, and learn the extent of a breach. Microsoft
describes it this way: "Workflow is fundamentally about the organization of
work. It is a set of activities that coordinate people and/or software.
Communicating this organization to humans and automated processes is the
value-add that workflow provides to our solutions.  Workflows are fractal. This
means a workflow may consist of other workflows (each of which may consist of
aggregated services). The workflow model encourages reuse and agility, leading
to more flexible business processes." (Microsoft Developer Network n.d.)

In the case of the forensic analysis process that underlies response as
described above, the workflow is fractal in terms of including other workflows,
but is also a recursive process. This process can start with one or more IP
addresses or network address blocks that are suspicious.  This can lead to a
set of potentially compromised computers who had communication to that single
IP address.  Looking at the flows to/from those suspect computers results in a
larger set of potentially malicious computers that are related to the first IP
address, but were not known at the start. The developing network of malicious
activity grows with each iteration in the discovery process and each new search
result builds on previous knowledge.  As the network increases in size, the
analyst wants to filter out known good hosts, and highlight the known bad
hosts, in order to find new suspect hosts to evaluate (and then hopefully move
to the known good or known bad sets.) Keeping track of the growing body of
known good and known bad is a requirement of the workflow for this discovery
process.



.. todo::

   FIGURE Relationship of STIX Elements (Source: Bret Jordan, Blue Coat Systems)

..

The objective of the DIMS system is to support the following high-level
missions and needs, which incorporate the four use cases described above as
defined by MITRE:

#. To facilitate collaborative response to shared threats by supporting
   real-time and near real-time communications, situational awareness in
   graphical and text report formats, and role-based controlled access to
   security event and alert data housed in a shared SIEM system. (UC1 and UC3)

#. To provide a framework for visualization and analytic tools that result in a
   shared view of common threats, in a manner that compares and contrasts each
   participant with others in the system to help them understand whether
   certain threats are widespread and common, or may be targeted to a specific
   sector, organization, or physical locality. (UC3)

#. To facilitate the real-time and near real-time operational sharing of
   actionable information in the form of structured IOCs and Observables that
   support triage, response and recovery, and determinations of events of such
   criticality that they require reporting to federal authorities. These IOCs
   and observables may come from US-CERT (as part of the CRADA between US-CERT
   and the PRISEM project), may come from other trust groups (be they
   sector-specific, regional, or self-organized), or may come from federal law
   enforcement agents in the local field office. As IOCs and Observables are
   linked with TTPs and COAs (see Figure 2 for an example of this linkage), the
   users can more quickly and efficiently respond and recover. (UC2, UC3, and
   UC4)

#. To facilitate tracking of remediation efforts across participants. It is a
   common occurrence to receive a report with a list of IP addresses and/or
   domain names of suspected compromised or abused hosts. Having a mechanism to
   automatically determine which IP addresses are of interest to which
   participants by comparing those addresses to assigned network blocks or top
   level domains makes it easier to know when attention should be paid to data
   coming in to the system. Similarly, after remediation it is possible to
   toggle the status of these hosts and automatically keep track of when a site
   has completed cleanup, what percentage of known compromised hosts have yet
   to be mitigated, and how quickly they are being cleaned up. This information
   speeds up overall response and provides metrics by which to compare process
   improvements over time. (UC1 and UC3)

#. While not directly mapping to one of MITRE’s use cases, the DIMS effort is
   intended to enable integration of complementary open source security tools
   and put these tools back into the community as open source tools, and/or
   transition these tools into commercially available products that advance the
   state of the art in distributed incident response.

.. _changepriorities:

Priorities among the changes
----------------------------

.. todo:;

   This paragraph shall identify priorities among the needed changes. It shall,
   for example, identify each change as essential, desirable, or optional, and
   prioritize the desirable and optional changes.

..

Changes considered but not included
-----------------------------------

.. todo::

   This paragraph shall identify changes considered but not included in
   :ref:`changedescription`, and rationale for not including them.

..

Assumptions and constraints
---------------------------

.. todo::

   This paragraph shall identify any assumptions and constraints applicable to
   the changes identified in this section.

..

.. _STIX FAQ #B1: http://stix.mitre.org/about/faqs.html#B1
.. _STIX FAQ #B2: http://stix.mitre.org/about/faqs.html#B2

.. [Dep13] Department of Homeland Security. Strengthening the Security and Resilience of the Nation's Critical Infrastructure. http://www.dhs.gov/strengthening-security-and-resilience-nation's-critical-infrastructure, August 2013.
.. [Exe13a] Executive Office of the President. Executive Order No. 13636. http://www.fas.org/irp/offdocs/eo/eo-13636.pdf, February 2013.
.. [Exe13b] Executive Office of the President. Presidential Policy Directive – Critical Infrastructure Security and Resilience/PPD-21. http://www.whitehouse.gov/the-press-office/2013/02/12/presidential-policy-directive-critical-infrastructure-security-and-resil, February 2013.

