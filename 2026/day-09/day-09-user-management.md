# TASK 1 

## Users & Groups Created
- Users: tokyo, berlin, professor, nairobi
- Groups: developers, admins, project-team

## Group Assignments
[List who is in which groups]
- id tokyo
uid=1001(tokyo) gid=1001(tokyo) groups=1001(tokyo),1004(developers),1007(project-team)
tokyo primary group is tokyo | Secondary groups - developers and project-team

- id berlin
uid=1002(berlin) gid=1002(berlin) groups=1002(berlin),1004(developers),1005(admins)
Primary group = berlin| Secondary group = developers, admins

- id professor
uid=1003(professor) gid=1003(professor) groups=1003(professor),1005(admins)
Primary group = professor | Secondary group = professor, admins

- id nairobi
uid=1004(nairobi) gid=1006(nairobi) groups=1006(nairobi),1007(project-team)
Primary group = nairobi | Secondary group = nairobi, project-team

## Directories Created
[List directories with permissions]

- sudo mkdir -p /opt/dev-project
drwxrwxr-x  2 root developers   4096 Feb 19 12:59 dev-project/
- sudo mkdir -p /opt/team-workspace (-p enables us to make parent directory and we can create subdirectories using this)
drwxrwxr-x  2 root project-team 4096 Feb 19 13:07 team-workspace/

## Commands Used
- useradd = for creating user (-m for creating home directory)
- groupadd = for creating group
- usermod = for changing groups of any user (-a appends the group to primary group)
- chmod = for modifying the file permissions
- chown = for changing ownership of the file (ownership of user and group)
- chown root:root file_name = here user is root and group is root
- chown root:group file_name = here user is root and group is group
(if -r used then it will modify all subdirectory or files inside files)
- passwd = for changing password

## What I Learned
[3 key points]

* I leanrt user management
* I learnt to modify file and group ownerships
* Learnt to make sub directories