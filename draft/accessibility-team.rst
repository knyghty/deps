============================
DEP XXXX: Accessibility Team
============================

:DEP: XXXX
:Author: Tom Carrick
:Implementation Team: Tom Carrick, others to be determined
:Shepherd: to be determined
:Status: Draft
:Type: Process
:Created: 2020-06-29
:Last-Modified: 2020-06-29

.. contents:: Table of Contents
   :depth: 3
   :local:

Abstract
========

This DEP proposes the formation of an Accessibility Team to encourage projects
maintained by the Django Software Foundation to be accessible to as diverse a
group as possible, particularly people with disabilities that make using the
web more difficult.

Specification
=============

The Accessibility Team (informally, a11y team) shall be formed.

Membership
----------

The team shall not have a fixed size, but instead will grow and shrink
organically as members choose to leave, and when new members are deemed to be
required by the rest of the team. Membership of the team works similarly to the
`Code of Conduct Committe <https://github.com/django/code-of-conduct/blob/master/membership.md>`_.
New members shall be chosen from a list of volunteers, or if there is a lack
of volunteers, an advertisement will be published on the Django website.
Priority will be given to volunteers who, in no particular order:

- Have disabilities that make using the web and/or web development more
  difficult.
- Have relevant, positive contributions or expertise in the field.
- Have a record of contributing to Django.

Members shall remain in the team for a fixed-term of 9 months, after which
they must opt-in to remain on the team. Membership will also be terminated by:

- Becoming disqualified due to actions taken by the Code of Conduct committe
  of the Django Software Foundation.

- A vote of the Technical Board, or full consensus of the rest of the
  Accessibility Team, if the team is considered too large, the person is not
  making positive contributions, or any other sound reason.
  (TODO: dunno about any of this)

Responsibilities
----------------

The remit of the Accessibility Team shall include all user-facing components
of projects maintained by the Django Software Foundation. This includes but is
not limited to:

- User-facing parts of Django, such as default HTML output in forms and such,
  and the django admin and its default theme, HTML, and JavaScript components.

- All websites and other software projects maintained by the DSF, such as the
  Django website, including documentation, Django Snippets, Django People,
  the issue tracker, etc.

The responsibilities of the Accessibility Team are expected to change over
time, and are to be decided by consensus of the team, with input from the
Technical Board as required. To begin, several areas have been identified:

- Deciding on any relevant accessibility guidelines to follow, such as WCAG,
  and at which conformance level.

- Implementing automated testing to catch issues, working with the ops
  team as needed to integrate this into the CI process.

- Coordinating regular manual accessibility audits on all relevant projects.

- Coordinating the fixing of accessibility issues and the improvement of the
  accessibility in general in Django and associated projects.

- Writing and maintaining documentation relating to accessibility, such as
  a statement of commitment to accessibility issues, and contribution
  guidelines.

- Reviewing accessibility fixes, improvements and other tickets that may affect
  the accessibility of the project.

To aid in reviewing, the Accessibility Team members shall be added to a team
in the GitHub organization with read access to relevant repositories, so that
they may be requested to review pull requests, at the discretion of the author,
reviewer, or other party.

Many of these duties can be implemented by any contributor, not only by the
Accessibility Team, however the Accessibility Team exists to coordinate this
work and to step in where contributors are not availble and support those who
lack the knowledge to do so themselves.


Motivation
==========

Accessible websites are not technically difficult to create, but accessibility
is often overlooked when developing features. Django is no exception to this.
The django admin currently exhibits many accessibility issues, such as forms
fields missing labels, low color contrast, a lacklustre keyboard-only
experience among other issues. Problems exist on other sites maintained by the
DSF, such as the `Django website <https://www.djangoproject.com/>`__,
`Django Snippets <https://djangosnippets.org/>`_, and others.

Rationale
=========

An alternative is to go on as usual, leaving accessibility in the hands of
individual contributors when writing and reviewing code. However, given the
accessibility issues that exist in the Djago admin and on the
`Django website <https://www.djangoproject.com/>`__, this doesn't seem to be
enough.

Another option is to implement some basic standards, such as conforming to WCAG
and setting up a CI to test. This approach is better than nothing but it
lacks a clear process for deciding on these. Ongoing maintenence would also be
necessary to keep any CI or other tooling up to date with Django's code, along
with manual audits - as
`automatic processes cannot find every issue <https://alphagov.github.io/accessibility-tool-audit/>`_
- and these could be easily forgotten.

Resources
=========

- `Diverse Abilities and Barriers (W3C)
  <https://www.w3.org/WAI/people-use-web/abilities-barriers/>`_
- `Accessibility, Usability, and Inclusion (W3C)
  <https://www.w3.org/WAI/fundamentals/accessibility-usability-inclusion/>`_
- `Web Content Accessibility Guidelines (WCAG) Overview
  <https://www.w3.org/WAI/standards-guidelines/wcag/>`_

Copyright
=========

This document has been placed in the public domain per the Creative Commons
CC0 1.0 Universal license (http://creativecommons.org/publicdomain/zero/1.0/deed).
