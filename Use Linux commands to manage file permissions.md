
# Scenario

You are a security professional at a large organization. You mainly work with their research team. Part of your job is to ensure users on this team are authorized with the appropriate permissions. This helps keep the system secure. 

Your task is to examine existing permissions on the file system. You’ll need to determine if the permissions match the authorization that should be given. If they do not match, you’ll need to modify the permissions to authorize the appropriate users and remove any unauthorized access.

# Project Description

Show permissions for files and directories, including hidden ones, for the _projects_ directory.

## Check file and directory details


Input ``` ls -la ```. The ``` -l ``` option will list files and directories along with their permissions. The ``` -a ``` option will include any hidden files or directories. You can combine the options using ``` -la ``` instead of separating them ``` -l -a ```.

Output 
```
drwxr-xr-x 3 researcher2 research_team 4096 May 19 16:26 .
drwxr-xr-x 3 researcher2 research_team 4096 May 19 16:59 ..
-rw--w---- 1 researcher2 research_team   46 May 19 16:26 .project_x.txt
drwx--x--- 2 researcher2 research_team 4096 May 19 16:26 drafts
-rw-rw-rw- 1 researcher2 research_team   46 May 19 16:26 project_k.txt
-rw-r----- 1 researcher2 research_team   46 May 19 16:26 project_m.txt
-rw-rw-r-- 1 researcher2 research_team   46 May 19 16:26 project_r.txt
-rw-rw-r-- 1 researcher2 research_team   46 May 19 16:26 project_t.txt
```

## Describe the permissions string

Permissions for a file or directory are represented by a 10-character string. A directory with all permissions enabled would be represented with the following string: ``` drwxrwxrwx ```

* The 1st character indicates the file type. The ``` d ``` indicates it’s a directory. When this character is a hyphen (-), it's a regular file. 

* The 2nd-4th characters indicate the read (r), write (w), and execute (x) permissions for the user. When one of these characters is a hyphen (-) instead, it indicates that this permission is not granted to the user.


* The 5th-7th characters indicate the read (r), write (w), and execute (x) permissions for the group. When one of these characters is a hyphen (-) instead, it indicates that this permission is not granted for the group.

* The 8th-10th characters indicate the read (r), write (w), and execute (x) permissions for the owner type of other. This owner type consists of all other users on the system apart from the user and the group. When one of these characters is a hyphen (-) instead, that indicates that this permission is not granted for other.

 _Note: These bullet points are copied from the Google Cybersecurity Course._

 ## Change file permissions

 The ``` chmod ``` command is used to change permissions for files and directories. To change permissions for a user, group, or other, this will be represented using ```u ```, ```g ```, or ```o ``` in the command.
 
 You can use operators such as ``` + ```, ``` - ```, or ``` = ``` to add, remove, or set the permissions equal to the value specified. The final argument for the ``` chmod ``` command specifies which file or directory to change permissions for.

To demonstrate this concept for the ``` project_k.txt ``` file from above and removing _write_ privileges for the group and other: ``` chmod g-w,o-w project_k.txt ```

The 10-character string for this file would change from ``` -rw-rw-rw- ``` to ```-rw-r--r-- ```

## Change file permissions on a hidden file

The same concept applies when changing permissions on a hidden file. However, you must use the ``` -a ``` option when listing files to include hidden files. 

The ``` . ``` that precedes the hidden file or directory name must be included in the ``` chmod ``` command.

## Change directory permissions

The same process from file permission modification can be used for directories. As always, the specified directory must be typed exactly how it is named in the filesystem in order for the command to work.

