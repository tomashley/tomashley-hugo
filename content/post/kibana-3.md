+++
date = "2013-07-17T00:23:51Z"
description = "Latest Logstash dashboard"
keywords = ["kibana", "logstash"]
title = "Kibana 3"

+++

Tonight I finally got my first preview of a working Kibana 3.

I tried running up a Vagrant box using the new [Kibana 3 Chef cookbook](https://github.com/lusis/chef-kibana) from Lusis

The issue with this was I forwarded port 80 in VirtualBox to 8080 on my Host.
I'm not sure whether Nginx or the Angular code in Kibana was dropping the port, but I could not list the _aliases route to proxied Elasticsearch because the port was dropping.

To get it to work I was forced to proxy Elasticsearch from my host on port 80.

It was a hack job, but gave me the preview I needed. Kibana 3 looks awesome, so I will now move it into production!
