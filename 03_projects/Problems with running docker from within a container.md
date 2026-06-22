So i have hit upon a problem with some code I an running which could lead to complexities in the organisation of the [[Hypatia Health|Hypatia Health beta]] app.

To work on the fitting module the idea I had come up with was to run a new docker container in the VM that could handle the fitting process itself and then interrogate that container from the main hypatiahealth container.

The problem is that in order to run docker commands from within a container on _sibling_ containers on the main machine we need to mount the docker socket from the outside machine inside the container.

Given the hypatiahealth container is set up to run as a non-privileged user they need to be added to the docker user group to work with the socket. **However** the group ID within the container will not necessarily be the same as the group ID in the outer layer - leading to permission issues.

So - this could be fixed at container build time by passing in the outer layers group ID and use it when creating the container docker group. This involves unnecessary builds though. Another option may be to run the whole plumber infrastrcture as root - but I don't like that idea either.

So I am looking again as to whether it makes sense to run this as a a separate AWS service, investigate scaling within docker compose or look at something like kubernetes to do autoscaling.