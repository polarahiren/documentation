# No space left on server

### Increase server volume

- Go to [Amazon AWS](https://eu-central-1.console.aws.amazon.com/) Panel
- Go to `Volumes`
- Select volume you want to extend
- Click on `Actions > Modify Volume`
- Set your desired size and hit modify
- It will take few minutes to get effect
- After increasing volume, ssh into server and perform these steps.
  - List all disks `sudo lsblk`
  - To list storage sizes by disks `df -hT`
  - To extend disk partition run following:
    - `sudo growpart /dev/nvme0n1 1` and `sudo resize2fs /dev/nvme0n1p1`
  - Verify if partition is extended `lsblk`
  - If you need more information go [here](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/recognize-expanded-volume-linux.html?icmpid=docs_ec2_console)

### Identify big files/directories to delete them

- Go to root directory `cd /`
- Run `du -hs * | sort -rh | head -5` to list out top 5 directories with largest size
- Try to delete `php-fpm` log files
- Try to delete `npm` or `yarn` log files
- Run `sudo apt-get autoremove` to remove unused apt package files
- Remove journal files `journalctl --vacuum-time=2s`

