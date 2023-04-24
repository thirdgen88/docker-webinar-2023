# Inductive Automation Webinar April 2023 - Ignition+Docker

Welcome to the demo repo for the IA webinar held in April 2023.  Just a quick note, this repo may not be kept up-to-date as time goes on.  This is also just a demo, there may be additional things you need to do on your own.  Ideally, other more permanent and supported sources will exist for that purpose.  But this will serve to share the resources from the demo that Kevin Collins, Joe Dolivo, and Keith Gamble presented during that session.

## Overview

There are multiple sub-folders under this solution, and each of them contain a Docker Compose stack.  Some of the stacks (such as [`proxy`](proxy), [`mailhog`](mailhog), and [`portainer`](portainer)) are meant to be longer living services that the other "project" stacks might use/share.  Most everything uses the [`proxy`](proxy) stack to enable everything to flow through the Traefik Reverse Proxy, so make sure to start that one first.

## Link to Webinar

https://www.inductiveautomation.com/resources/webinar/ignition-docker-how-to-use-containers-for-faster-development
