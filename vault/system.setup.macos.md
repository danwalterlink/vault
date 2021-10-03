---
id: edu8qw1tgsjub51732c6vjy
title: macOS
desc: ''
updated: 1656437563241
created: 1656433122774
---


A quick Google search uncovered the simple change. Add the following line to /etc/pam.d/sudo:

auth sufficient pam_tid.so