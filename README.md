# Information about branches

## Hyper-V_patches
Merge this when doing a gitsync to pull in some workarounds to make the Hyper-V/VirtualServer/VirtualPC legacy emulated network interfaces function.  It is designed to be mergeable into 2.0.x or current.

To merge automatically every time you use gitsync, create /root/.gitsync_merge if it does not exist and add this line to it:

`git://github.com/efonne/pfsense.git Hyper-V_patches`

Specify build_commit as the branch for gitsync if you only want to install the patch and do not want to update any other web GUI code.  Note that this gitsync should be performed before installing any packages that modify the web GUI code.  You may also go to System: Firmware: Updater Settings, enable gitsync on update, and add the special build_commit branch name if you want the patch to be applied any time you install a firmware update.