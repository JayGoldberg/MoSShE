# MoSShE
Lightweight, secure server monitoring 

2003- by Volker Tanger <volker.tanger@wyae.de>

MoSShE (MOnitoring in Simple SHell Environment) is a simple,
lightweight (both in size and system requirements) server monitoring
package designed for secure and in-depth monitoring of single or
multiple typical/critical internet systems. 

As most of the servers/services I want to monitor are remote systems,
traditional NMS (relying on close-looped and/or unencrypted sessions) are
either big, complicated to install for safe remote monitoring, ressource
intense (when doing remote checks), lack a status history or a combination
thereof.

Thus I wrote this small, easily configured system. It originally was
intended for monitoring of single a handful of typical internet
systems. With the more recent system and grouping features monitoring
of serious numbers of systems is easily possible.

MoSShE supports email alerts and SLA monitoring out of the box - and
whatever you can script. 

The system is programmed in plain (Bourne) SH, and to be compatible
with BASH and Busybox so it can easily be deployed on embedded systems.

Monitoring is designed to be distributed over multiple systems,
usually running locally. As no parameters are accepted from outside,
checks cannot be tampered or misused from outside. 

The system is designed to allow decentralized checks and evaluation as
well as classical agent-based checks with centralized data
accumulation. 

Agent data is transferred via HTTP (pull-mode) or FTP, SSH, SCP, ...
in push-mode, so available web servers can be co-used for agent data
transfer. Additionally each agent creates simple (static) HTML pages
with full and condensed status reports on each system, allowing simple
local checks.

