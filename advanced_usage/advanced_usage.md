!SLIDE title_slide

# (Advanced) Usage



!SLIDE

# Behavior Driven <br> System Administration

* Write tests first (describe what you want)
* Let your ops people configure the system
* Run the tests (until everything's green)



!SLIDE

# Test your (play|cook)books

* Write tests
* Provision your machine (with Chef, Ansible, Puppet, ...)
* Run the tests (until everything's green)
* Build Continuous Integration pipeline



!SLIDE

# Monitoring

* Write tests
* Have Jenkins run tests every X hours
* Set up a dashboard for results



!SLIDE

# Test Kitchen

* Orchestrate testing of infrastructure code on multiple platforms
* Easy configuration with `.kitchen.yml` file
* Great support for Chef cookbook testing
* see [http://kitchen.ci/](http://kitchen.ci/)
