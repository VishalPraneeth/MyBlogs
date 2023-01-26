# The Evolution Of Docker Containers

Hello👋 In this blog, I am going to narrate to you the story of containers.

As most of you think that Docker is where the story of containers started, that's definitely not true. It began much earlier in... in fact, in the 1970s, when the chroot was introduced. Now, chroot was a Linux/UNIX utility, and with chroot, what you could do was even if you're not a root user, you could switch your root in your home directory and become sort of an admin in that restricted area actually. It was more or less like a filesystem - a namespace that we call in today's world. And that was the beginning of it all.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1674745720979/2e5a5972-56da-4fcf-bfc4-cc667b62de5d.png align="center")

Later, between 2001 and 2004, Solaris came with its own zones. So, you had Solaris with zones, and we had BSD with something called jails.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1674745943326/887be3d0-471b-470e-ac3e-9988befdbe4c.png align="center")

BSD came up with its own mechanism called jails, which is very similar to what we call as Linux containers. The only thing about containers in general is, and this is also called operating system virtualization, so, the technology involved in operating system virtualization restricts you to running let's say a Solaris on top of Solaris, or it could be a BSD on top of BSD here.

### You cannot run a Linux container on top of Solaris or BSD, or you cannot run Linux in a BSD jail and Solaris zone, and vice-versa.

There was a company called Virtuozzo, that created their open-source version of the container system called Open Virtuozzo, they called it OpenVZ.

### Why OpenVZ failed?

Even though you could run Linux containers with it, it was quite complex. And then you had to recompile the kernel in order to use OpenVZ. You had no ecosystem, so you had to build your own images, and distribute them yourself, there was no container orchestration engine like Kubernetes or anything on a similar line. So, using and running it in production was a challenge.

In 2005, Google built its own cluster manager and started migrating its workloads to containers somewhere around the 2003-2004 timeline. And what they created was a cluster manager called Borg. We talked about Docker in 2012 but Google has been using and running its applications on top of containers in production environments since 2004. Isn't that fantastic?

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1674746597225/d0ade9e2-dd88-4a79-b52a-7e9d2e911a13.png align="center")

And what Google also did was, as part of creating and running this Borg system, they created something, a feature of the Linux kernel, where you could isolate the process, and you could also restrict the resources for a container. So, resource restriction and resource management became easier. They created something called process groups to restrict the CPU memory and all of that for a container and contributed back to the Linux kernel.

In 2008 what came out of this was a software called as LXC.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1674747623817/7e920832-f349-4edf-ab00-4454b03aba88.png align="center")

A lot of companies started leveraging LXC, and they started building their solutions on top of LXC. One such company was "dotCloud", what they had was a browser-based collaboration tool. So, through your browser, you could have an IDE, and you could write the code here, and then in another terminal, you could execute it as well. Now, that feature, where you could execute the code in a terminal using a Linux shell, was built on top of LXC.

By the end of 2012, they were almost running out of funds, they were almost on the verge of bankruptcy, and that's when the founder of dotCloud brought his team together, and what they decided to do was open source the technology that they were using to run this terminal. And they named it, you might have already guessed

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1674748151005/d0bf9e97-f5a1-42f7-aafc-c96a63eada42.png align="center")

### And the rest is history after they open sourced it became very very popular very quickly, and dotCloud was renamed to Docker Inc.

### Would be continuing with more stuff about Docker, other DevOps tools, and projects in my upcoming blogs. Make sure to check out and share your feedback!