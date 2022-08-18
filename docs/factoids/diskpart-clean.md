---
layout: default
title: Cleaning a Disk in Dispart
nav_exclude: false
parent: Factoids
has_children: false
search_exclude: false
last_modified_date: 2022-08-14
---
# Cleaning a Disk in Diskpart
Open Command Prompt or PowerShell as admin then follow the steps below.

```
diskpart
list disk
```

[![Windows 11-2021-10-05-15-09-53.png](/assets/install-11/windows-11-2021-10-05-15-09-53.png)](/assets/install-11/windows-11-2021-10-05-15-09-53.png)

[![Windows 11-2021-10-05-15-10-13.png](/assets/install-11/windows-11-2021-10-05-15-10-13.png)](/assets/install-11/windows-11-2021-10-05-15-10-13.png)

[![Windows 11-2021-10-05-15-10-24.png](/assets/install-11/windows-11-2021-10-05-15-10-24.png)](/assets/install-11/windows-11-2021-10-05-15-10-24.png)

[![Windows 11-2021-10-05-15-10-39.png](/assets/install-11/windows-11-2021-10-05-15-10-39.png)](/assets/install-11/windows-11-2021-10-05-15-10-39.png)

Make note of the disk you want to clean from the step above.
```
sel disk #
clean
create partition=primary
format quick fs=ntfs
assign letter=E
```
Cleaning the disk will lose any data.

You can change the file type to a different one if so chooses, FAT32 or exFAT are examples.

You can also change the letter to any letter that is no in use. 