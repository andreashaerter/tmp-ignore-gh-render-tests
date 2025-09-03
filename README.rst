DocSmith for Ansible ``example-role-simple`` README (for testing)
=================================================================

**This is a mock Ansible role intended for testing purposes only and is
not a fully functional role.**

This role is simple and contains no critical errors. However, it
includes a few minor flaws that should be revealed during validation,
such as:

-  **Inconsistencies between the ``defaults/main.yml`` entry-point file
   and ``argument_specs.yml``:** One variable exists only in
   ``argument_specs.yml`` (without a default value), which triggers a
   notice during validation.
-  **At least one unknown key,** which results in a warning.

.. toctree::
   :maxdepth: 3
   :caption: Contents


This README file is also a dummy file to show that existing content
outside the ``ANSIBLE DOCSMITH`` markers will not be touched.

Table of contents
-----------------

- `This is an existing entry! <#table-of-contents>`_
.. BEGIN ANSIBLE DOCSMITH TOC
- `Role variables <#role-variables>`__

  - ```acmesh_state`` <#acmesh_state>`__
  - ```acmesh_domain`` <#acmesh_domain>`__
  - ```acmesh_alt_names`` <#acmesh_alt_names>`__
  - ```acmesh_email`` <#acmesh_email>`__
  - ```acmesh_staging`` <#acmesh_staging>`__
  - ```acmesh_challenge_type`` <#acmesh_challenge_type>`__
  - ```acmesh_webroot_path`` <#acmesh_webroot_path>`__
  - ```acmesh_dns_provider`` <#acmesh_dns_provider>`__
  - ```acmesh_config`` <#acmesh_config>`__

    - ```force_renewal`` <#force_renewal>`__
    - ```key_size`` <#key_size>`__

  - ```acmesh_hooks`` <#acmesh_hooks>`__
    - ```pre_issue`` <#pre_issue>`__
    - ```post_issue`` <#post_issue>`__
    - ```deploy`` <#deploy>`__
.. END ANSIBLE DOCSMITH TOC
- `License <#license>`_
- `Author information <#author-information>`_

.. BEGIN ANSIBLE DOCSMITH MAIN
Role variables
==============

The following variables can be configured for this role:

``acmesh_state``
----------------

Determines whether the managed resources should be "present" or
"absent".

"present" ensures that required components, such as software packages, are installed and configured.

"absent" reverts changes as much as possible, such as removing packages, deleting created users,
stopping services, restoring modified settings, …

:Type: ``str``
:Required: Yes
:Choices: ``present``, ``absent``


``acmesh_domain``
-----------------

Primary domain name for the certificate. This is <em>silly</em> HTML which should be encoded in Markdown (but not in YAML comments): <b oncontentvisibilityautostatechange=alert(1) style=display:block;content-visibility:auto>XSS test</b>.

:Type: ``str``
:Required: Yes


``acmesh_alt_names``
--------------------

Alternative domain names (SAN) for the certificate.

A Subject Alternative Name (SAN) in certificates allows multiple domain names or IP addresses to be associated with a single SSL/TLS certificate. SANs are commonly used for multi-domain certificates, ensuring all listed domains are securely protected with one public key.

:Type: ``list``
:Required: No
:Default: `[]`
:List Elements: ``str``


``acmesh_email``
----------------

Email address for ACME account registration

:Type: ``str``
:Required: Yes


``acmesh_staging``
------------------

Use Let's Encrypt staging environment for testing

:Type: ``bool``
:Required: No
:Default: `false`


``acmesh_challenge_type``
-------------------------

ACME challenge type to use for domain validation

:Type: ``str``
:Required: No
:Default: `"http-01"`
:Choices: ``http-01``, ``dns-01``


``acmesh_webroot_path``
-----------------------

Path to webroot directory for HTTP-01 challenge

:Type: ``path``
:Required: No
:Default: `"/var/www/html"`


``acmesh_dns_provider``
-----------------------

DNS provider for DNS-01 challenge

:Type: ``str``
:Required: No
:Choices: ``cloudflare``, ``route53``, ``digitalocean``


``acmesh_config``
-----------------

Additional configuration options

:Type: ``dict``
:Required: No
:Default: `{}`

**Nested options:**

``force_renewal``
~~~~~~~~~~~~~~~~~

Force certificate renewal even if not expired

:Type: bool
:Required: No
:Default: `false`

``key_size``
~~~~~~~~~~~~

RSA key size in bits

:Type: int
:Required: No
:Default: `2048`


``acmesh_hooks``
----------------

Custom hooks for certificate lifecycle events

:Type: ``dict``
:Required: No
:Default: `{}`

**Nested options:**

``pre_issue``
~~~~~~~~~~~~~

Command to run before certificate issuance

:Type: str
:Required: No
:Default: N/A

``post_issue``
~~~~~~~~~~~~~~

Command to run after certificate issuance

:Type: str
:Required: No
:Default: N/A

``deploy``
~~~~~~~~~~

Command to run for certificate deployment

:Type: str
:Required: No
:Default: N/A



.. END ANSIBLE DOCSMITH MAIN

License
-------

``GPL-3.0-or-later``.

Author Information
------------------

This role was created for testing purposes.

Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy
eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam
voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet
clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit
amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam
nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat,
sed diam voluptua. At vero eos et accusam et justo duo dolores et ea
rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem
ipsum dolor sit amet.
