# bios-upgrade.md


15466  2018-09-19 10:54:03 mkdir /var/tmp/firmware
15467  2018-09-19 10:54:12 cd /var/tmp/firmware/
15468  2018-09-19 10:54:42 git clone https://github.optum.com/fecompute/OCT-Firmware-Update.git
15477  2018-09-19 10:56:44 ls -l
15480  2018-09-19 10:57:00 cd OCT-Firmware-Update/
15481  2018-09-19 10:57:02 ls -l
15482  2018-09-19 10:57:07 chmod 755 *
15484  2018-09-19 10:57:10 ls
15485  2018-09-19 11:07:29 ./firmware_update.sh
15486  2018-09-19 11:09:52 ls
15487  2018-09-19 11:10:06 ./firmware_check.sh
15488  2018-09-19 11:10:26 ls
15489  2018-09-19 11:10:30 cd Updates/
15496  2018-09-19 11:11:51 cd BIOS/
15497  2018-09-19 11:11:52 ls -l
15498  2018-09-19 11:12:34 chmod 755 *
15499  2018-09-19 11:12:37 ls -l
15500  2018-09-19 11:12:55 ./ME_lnx64.sh
15501  2018-09-19 11:16:38 cp /boot/initramfs-$(uname -r).img /boot/initramfs-$(uname -r).img.$(date +%m-%d-%H%M%S).bak
15502  2018-09-19 11:16:40 dracut -f /boot/initramfs-$(uname -r).img $(uname -r)
15503  2018-09-19 11:18:13 reboot





from Aditya Gautam to everyone:
https://github.optum.com/fecompute/OCT-Firmware-Update
from Aditya Gautam to everyone:
https://github.optum.com/OSFI-Kubernetes/Meltdown-Specter-Patching
from Aditya Gautam to everyone:
chmod -R 744 /var/tmp/firmware/OCT-Firmware-Update/*


ipmitool -H apslp0895lo.uhc.com -U admin bmc reset cold



INC9010792--apslp0895--satya
INC9010818--apslp0901--kishore
INC9011524--apslp0897--satya
INC9011565--apslp0899--Aditya

/etc/chef/ohai/plugins
