# PuppetConf 2016 
Raleigh Puppet Users Group
2016-11

New CEO: Sanjay Mirchandani
Primary rolle: Scale the company

Big push on partners for sales and professional services
New TAPP (Technical Alliance Partner Program) program coming in Feb
Demo-Easel - Very simple scripted demos with (almost) no typing required


## New Release - 2016.4 (LTS → Oct 2018):
[Everything else is EOL by January 2017!](https://puppet.com/misc/puppet-enterprise-lifecycle)
Quarterly release cadence with an Long Term Support (LTS) release coming every 18-months

- Idempotent installer
- Situational Awareness
  - Filter intentional vs. correctional changes
  - Deploy Puppet agents even with no enforcement.  Agent/Facter reports so much info into PuppetDB
  - Audit what could be managed by puppet
  - Redact sensitive data in reports
- Direct control vs. convergence
  - Console: Node → run (single node)
  - Multiple node runs with 'puppet job' and the query language
  - Example:
    ```
    puppet code deploy
    puppet job run --nodes <NODE NAME> <OPTIONS>
    puppet job run --query '<QUERY>' <OPTIONS>
    --query 'nodes { certname ~ "web" }'
    --query 'inventory { facts.operatingsystem = "CentOS" and resources { type = "Service" and title = "httpd" } }'
    ```
  - More info on [Puppet Orchestrator](https://docs.puppet.com/pe/latest/orchestrator_job_run.html)
- Single, consistent way to manage all infrastructure
  - Manage containers
  - Build a role on a server or in a Docker container from the same manifest
  - [Building Puppet-Based Applications Inside Docker](https://puppet.com/blog/building-puppet-based-applications-inside-docker)
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
[Videos on YouTube](https://www.youtube.com/playlist?list=PLV86BgbREluVjwwt-9UL8u2Uy8xnzpIqa)
Keynotes are up NOW!  Session recordings will be available 07 Nov.

## PuppetConf 2017
Oct 10-12 @ Hilton Union Square, San Francisco, CA

Early Registration is already open!   http://PuppetConf.com/  $995

## Related information

- https://github.com/jjpryor/rpug-2016-11/
- [Videos on YouTube](https://www.youtube.com/playlist?list=PLV86BgbREluVjwwt-9UL8u2Uy8xnzpIqa)
- [PuppetConf 2016 Wrapup](https://rnelson0.com/2016/10/26/puppetconf-2016-wrap-up/) by Puppet's MVP for 2016
- PuppetConf [Twitter feed](https://twitter.com/puppetconf)
- [PuppetConf recap](https://cwatson.org/2016/10/puppetconf-2016-san-diego/) by Craig Watson
- [Day 1 keynotes](https://puppet.com/blog/puppetconf-2016-keynotes-day-1-puppet-and-digital-transformation)
- [Day 2 keynotes](https://puppet.com/blog/puppetconf-day-2-keynotes-azure-nano-server-salesforce-docker-mind-cio)
- [Puppet Enterprise 2016.4 Highlights](https://puppet.com/blog/docker-image-build-orchestration-corrective-change-reporting-puppet-enterprise-2016-4)
- [Jenkins Puppet plugin](https://wiki.jenkins-ci.org/display/JENKINS/Puppet+Enterprise+Pipeline+Plugin) enabling Jenkins to promote Puppet code and deploy to nodes
- The [NTP module](https://puppet.com/blog/ntp-puppet-4-language-update) has been updated with all the new Puppet 4 goodness.  This is a great place to see some of the new language features in use!
- [Puppet Enterprise Lifecycle](https://puppet.com/misc/puppet-enterprise-lifecycle) for releases
