# cgroups

- cgroups are

* namespaces isolate, cgroups control.

a company uses containers for microservices. one faulty container crashes the host due to high memory usage.
which container feature was misconfigured or missing? cgroups
which kernel mechanism should have prevented this? cgroups
would namespaces alone solve this issue?why?

a server is running three containers.
container A runs a cpu-intensive task
container B runs a web server
container C runs a database

which linux feature prevents container A from consuming all CPU?
which feature ensures container B cannot see processes of container C?
which namespace allows all three containers to use port 80 internally?
