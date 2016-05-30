+++

author = "Ganesh Kadam"
categories = ["TechNotes"]
date = "2016-04-26T1:00:12+05:30"
description= "February Python Pune Meetup 2016"
linktitle = "/categories/TechNotes/"
title = "Gerrit Isue"
type = "post"
tags = ["Git","Gerrit"]

+++

I was working on shell a script. Now that it was complete I need to send that script for review.So I started to work on this. Unfortunately I got the following error which took me almost took a day to resolve on my side. I decided not to ask my mentors until and unless I am not able to rsolve this issue. This has been common issue amongst all of us interns!

    [gkadam@dhcp201-114 cert-openstack-scripts]$ git review -R
    Could not connect to gerrit.
    Enter your gerrit username: gkadam@redhat.com
    Trying again with ssh://gkadam@redhat.com@code.engineering.redhat.com:22/cert-openstack-scripts
    <traceback object at 0x7fa7a448cb00>
    We don't know where your gerrit is. Please manually create a remote
    named "gerrit" and try again.
    Could not connect to gerrit at ssh://gkadam@redhat.com@code.engineering.redhat.com:22/cert-openstack-acripts
    Traceback (most recent call last):
    File "/usr/bin/git-review", line 11, in <module>
    sys.exit(main())
    File "/usr/lib/python2.7/site-packages/git_review/cmd.py", line 1534, in main
    sys.exit(e.EXIT_CODE)
    AttributeError: 'GitReviewException' object has no attribute 'EXIT_CODE'

After going through lots of google serarches I realized that, the things that were going wrong are already mentioned in the error code that I was getting. Before this I made a very silly mistake of deleting the existing file in that directory from which I have to send the file for review. So just after knowing this issue, I copied the new script in to the same directory again. Then I renamed to it's earlier name and performed following steps :

1.  Cloned the repository to new location :

<!-- -->

    [gkadam@dhcp201-114 ~]$ git clone ssh://gkadam@code.engineering.redhat.com:22/cert-openstack-scripts
    Cloning into 'cert-openstack-scripts'...
    Checking connectivity... done.
    warning: remote HEAD refers to nonexistent ref, unable to checkout.

1.  Added the remote repository as we can see in the above error!

<!-- -->

    [gkadam@dhcp201-114 cert-openstack-scripts]$ git remote add gerrit ssh://gkadam@code.engineering.redhat.com:22/cert-openstack-scripts

1.  Then did a git review after adding the script and commiting it in that dierctory :

<!-- -->

    [gkadam@dhcp201-114 cert-openstack-scripts]$ git review -R
    Your change was committed before the commit hook was installed.
    Amending the commit to add a gerrit change id.
    remote: Processing changes: new: 1, refs: 1, done.
    remote: (W) 9dedc09: commit subject >65 characters; use shorter first paragraph
    remote: (W) 9dedc09: too many commit message lines longer than 70 characters; manually wrap lines
    remote:
    remote: New Changes:
    remote:https://code.engineering.redhat.com/gerrit/73014 Add user validation, and create functions : create_member,create_network and remote:
    To ssh://gkadam@code.engineering.redhat.com:22/cert-openstack-scripts
    * [new branch]      HEAD -> refs/publish/master

This was the workaround for my problem that I was facing.

Here is the link to the similar issue on git : [Git remote HEAD Issue](https://help.github.com/articles/error-remote-head-refers-to-nonexistent-ref-unable-to-checkout/)
