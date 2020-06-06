# AlienArenaBackup - backup script for Alien Arena (1.3)
Creates a hot backup of your Alien Arena installation and optionally copies it to a offsite server.

Official support sites: [Official Github Repo](https://github.com/fstltna/AlienArenaBackup) - [Official Forum](https://alienarena.gameplayer.club/index.php/forum/alien-arena-tools) ![Alien Arena Logo](https://FPS.GamePlayer.club/aa2k12logo2.jpg) 

---

1. Create the "aaowner" if not alredy there
2. Make sure ssh-keygen is installed: "apt install ssh-keygen"
3. Run "ssh-keygen" and when asked for the password just press enter twice
4. Run "ssh-copy-id -i ~/.ssh/id_rsa.pub your-destination-server" - This will ask you for your remote password. This is normal.
5. Edit the settings at the top of alienarenabackup.pl if needed
6. After the first run edit the ~/.aabackuprc and change your settings if you want to use the offsite backup feature. The next run it should save to your remote host.
7. create a cron job like this:

        1 1 * * * /home/aaowner/AlienArenaBackup/alienarenabackup.pl

8. This will back up your Alien Arena installation at 1:01am each day, and keep the last 5 backups.

If you need more help visit https://alienarena.gameplayer.club/index.php/forum/alien-arena-tools and check out this website: https://superuser.com/questions/555799/how-to-setup-rsync-without-password-with-ssh-on-unix-linux
