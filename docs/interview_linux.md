## Q: Why is /etc critical in production systems?
A: /etc contains system-wide and application configuration files. Production services read their behavior from these files, so incorrect configuration or permissions in /etc can prevent services from starting or cause outages.

## Q: Why is /var/log the first place DevOps looks during incidents?
A: /var/log contains system and application logs that show runtime behavior. Logs help reconstruct timelines, identify errors, and understand failures during incidents.

## Q: What is the difference between chmod 644 and chmod 755?
A: chmod 644 gives read-write permission to the owner and read-only permission to group and others. chmod 755 adds execute permission, allowing scripts or binaries to run.

## Q: Why do permission issues cause application failures?
A: Applications fail when they cannot read configuration files, write logs, or execute binaries. Linux strictly enforces permissions, so even correctly configured applications will fail without proper access.

## Q: What does /proc represent?
A: /proc is a virtual filesystem that dynamically exposes kernel and process information such as CPU, memory, and running processes. It does not store data on disk.

