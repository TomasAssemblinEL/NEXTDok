Assemblin EL AB verksamhetssystem
===============

Syfte Verksamhetshandboken är vårt verktyg för att styra utförandet av de produkter och tjänster som företaget tillhandahåller, så att kvalitetsmål och kvalitetspolicy uppnås, samt så att miljöpåverkande verksamhet utförs enligt gällande lagar, miljöpolicy, och fastställda miljömål.
Genom Assemblin ELs verksamhetssystem:

*fastställs och dokumenteras våra rutiner.

*informeras kunder och anställda om våra policys, samt de åtgärder vi vidtagit för att upprätthålla och vidmakthålla dessa.

*säkerställs kvaliteten i våra produkter och tjänster.

*säkerställs att aktiviteter som påverkar den yttre miljön genomförs enligt upprättat miljöprogram och uppställda mål.

Omfattning Kvalitets- och miljöledningssystemen är uppbyggda enligt och motsvarar kraven i systemstandarderna SS-EN ISO 9001:2008 och SS-EN ISO 14001:2004. Systemen omfattar samtliga avdelningar inom Assemblin EL  AB.
Verksamhetshandboken: Beskrivning av kvalitets- och miljöledningssystemen i sin helhet.

.. image:: images/appArch.png

The most common interactions are:

* Browsers communicate with web applications

* Web applications communicate with web APIs (sometimes on their own, sometimes on behalf of a user)

* Browser-based applications communicate with web APIs

* Native applications communicate with web APIs

* Server-based applications communicate with web APIs

* Web APIs communicate with web APIs (sometimes on their own, sometimes on behalf of a user)

Typically each and every layer (front-end, middle-tier and back-end) has to protect resources and
implement authentication and/or authorization – often against the same user store.

Outsourcing these fundamental security functions to a security token service prevents duplicating that functionality across those applications and endpoints.

Restructuring the application to support a security token service leads to the following architecture and protocols:

.. image:: images/protocols.png

Such a design divides security concerns into two parts:

Verksamhetspolicy
^^^^^^^^^^^^^^
Authentication is needed when an application needs to know the identity of the current user.
Typically these applications manage data on behalf of that user and need to make sure that this user can only
access the data for which he is allowed. The most common example for that is (classic) web applications –
but native and JS-based applications also have a need for authentication.

The most common authentication protocols are SAML2p, WS-Federation and OpenID Connect – SAML2p being the
most popular and the most widely deployed.

OpenID Connect is the newest of the three, but is considered to be the future because it has the
most potential for modern applications. It was built for mobile application scenarios right from the start
and is designed to be API friendly.

Verksamhetsmål 2017
^^^^^^^^^^
Applications have two fundamental ways with which they communicate with APIs – using the application identity,
or delegating the user’s identity. Sometimes both methods need to be combined.

OAuth2 is a protocol that allows applications to request access tokens from a security token service and use them
to communicate with APIs. This delegation reduces complexity in both the client applications as well as the APIs since
authentication and authorization can be centralized.

Ekonomiskt ansvar Attestmatris
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
OpenID Connect and OAuth 2.0 are very similar – in fact OpenID Connect is an extension on top of OAuth 2.0.
The two fundamental security concerns, authentication and API access, are combined into a  single protocol - often with a single round trip to the security token service. 

We believe that the combination of OpenID Connect and OAuth 2.0 is the best approach to secure modern
applications for the foreseeable future. IdentityServer4 is an implementation of these two protocols and is
highly optimized to solve the typical security problems of today’s mobile, native and web applications.

Medarbetare inom Assemblin AB
^^^^^^^^^^^^^^^^^^^^^^^^^^^^
IdentityServer is middleware that adds the spec compliant OpenID Connect and OAuth 2.0 endpoints to an arbitrary ASP.NET Core application.

Typically, you build (or re-use) an application that contains a login and logout page (and maybe consent - depending on your needs),
and the IdentityServer middleware adds the necessary protocol heads to it, so that client applications can talk to it using those standard protocols.

.. image:: images/middleware.png

The hosting application can be as complex as you want, but we typically recommend to keep the attack surface as small as possible by including
authentication related UI only.

Arkiveringsregler
^^^^^^^^^^^^^^^^^
Text kommer

Verksamhetshandbok samt Q-dokument
^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Text kommer

Kompetenskrav och utbildningsplaner
^^^^^^^^^^^^^^^^^^^^^^^^^^^^


