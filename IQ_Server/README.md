At this level it is still a docker-compose project. I've stripped this down from the reference platform project and moved the persistance to a volume instead of the local file system

The initial output of the conversion to Helm is in the Helm folder. I haven't tested this yet so I'm not sure it even runs yet.

Updating the logging to also direct policy violatiuons and audit logs to stdout in addition to trhe server log
