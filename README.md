# fix-files-permissions
fix files and folder permissions after migration 


# Reset WordPress file and folder permissions with SSH
For security reasons, files and folders on servers have permissions that determine who can read, write, access, and modify these files and folders. Permissions are presented with numerical values, and, for WordPress, they should be set to 755 for folders and 644 for files (in older Web Hosting accounts and Managed WordPress, these values are 705 for folders and 604 for files). Insufficient permissions can cause errors on the site and when their values are wrong, it can be a potential security risk. If you want to find out more about the meaning behind these values, you can check out this article on wordpress.org. Here’s how to reset permissions through SSH using BASH commands.

# Connect to your hosting account with SSH.
Use the command ls to list files and folders, and cd and ../ to move through directories until you are in the directory with WordPress installation.

Use the command pwd to find the path to the current folder (directory).

# Enter the following commands:

# To change permissions for folders:

`find /path/to/current/directory/ -type d -exec chmod 755 {} \;`

In the command above, you should replace /path/to/current/directory/ with the actual path from Step 3.

# To change permissions for files:

`find /path/to/current/directory/ -type f -exec chmod 644 {} \;`

In the command above, you should replace /path/to/current/directory/ with the actual path from Step 3.
You'll see a message confirming the changes were successful.
