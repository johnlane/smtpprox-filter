smtpprox-filter
===============

trivial transparent SMTP proxy content filter

About smtpprox
--------------

smtpprox is a trivial transparent SMTP proxy, an SMTP server and
client combination. It uses its own SMTP server and client modules
which are designed to expose every step of the protocol dialogue to
the calling program, which provides for the greatest flexibility in
hooking in envelope and content controls and scanning.

For efficiency reasons, it pre-forks and serves from a pool of
servers, Apache-style.

smtpprox-filter adds a content filtering mechanism where the DATA
part of the SMTP conversation is passed through a filter pipeline,
the filters being provided as command-line arguments.

Any executables that read stdin and writes stdout can be used as
a filter.

smtpprox-filter adds a --helo option to specify the fqdn sent to
connecting clients and in HELO/EHLO responses sent as a client.

Author
------

smtpprox was written by Bennett Todd, <bet@rahul.net>. The extensions
forming smtpprox-filter were contributed by John Lane, <john@lane.uk.net>.

About this repository
---------------------

This github repository is a fork of jnorell/smtpprox extended to
provide the content filter functionality.

smtpprox Copyright
------------------

   This code is Copyright (C) 2001 Morgan Stanley Dean Witter, and
   is distributed according to the terms of the GNU Public License
   as found at <URL:http://www.fsf.org/copyleft/gpl.html>.


   This program is distributed in the hope that it will be useful,
   but WITHOUT ANY WARRANTY; without even the implied warranty of
   MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
   GNU General Public License for more details.

