# PuppetConf 2016 
Raleigh Puppet Users Group
2016-11

New CEO: Sanjay Mirchandani
Primary rolle: Scale the company

Big push on partners for sales and professional services
New TAPP (Technical Alliance Partner Program) program coming in Feb
Demo-Easel - Very simple scripted demos with (almost) no typing required


## New Release - 2016.4 (LTS → Oct 2018):
Everything else is EOL by January 2017!
Quarterly release cadence with an Long Term sSupport (LTS) release coming every 18-months

- Idempotent installer
- Situational Awareness
  - Filter intentional vs. correctional changes
  - Deploy Puppet agents even with no enforcement.  Agent/Facter reports so much info into PuppetDB
  - Audit what could be managed by puppet
  - Redact sensitive data in reports
- Direct control vs. convergence
  - Console: Node → run (single node)
  - Multiple node runs with 'puppet job' and the query language
  - puppet code deploy
puppet job run --nodes <NODE NAME> <OPTIONS>
puppet job run --query '<QUERY>' <OPTIONS>
--query 'nodes { certname ~ "web" }'
--query 'inventory { facts.operatingsystem = "CentOS" and resources { type = "Service" and title = "httpd" } }'
- Single, consistent way to manage all infrastructure
  - Manage containers
  - Build a role on a server or in a Docker container from the same manifest
- Puppet can be deployed in containers
  - Rapid test/demo environments
- Jenkins integrations
- More desktop tools for managing Puppet in the works

## Culture

Lots of talk about Imposter Syndrome and culture.

## Communicating with and getting buy-in from executives

What your CIO cares about:
- Speed from idea to revenue generation (production)
- Translate everything into $$$
- The higher up the chain, the less specifics they can manage.  Demonstrate how to make or save $$$ or simplify things like security & audits

## Videos
Videos on YouTube: 07 Nov

## PuppetConf 2017
Oct 10-12 @ Hilton Union Square, San Francisco, CA

Early Registration is already open!   http://PuppetConf.com/  $995
