# SAS-SSD

![https://cdn.statically.io/img/hddmag.com/wp-content/uploads/2016/03/sata-vs-sas.jpg](https://cdn.statically.io/img/hddmag.com/wp-content/uploads/2016/03/sata-vs-sas.jpg)

![https://i0.wp.com/i.stack.imgur.com/bFfIY.jpg](https://i0.wp.com/i.stack.imgur.com/bFfIY.jpg)

* https://forums.servethehome.com/index.php?threads/sas-v-sata-power-plug.16277/
* https://searchstorage.techtarget.com/definition/SAS-SSD-Serial-Attached-SCSI-solid-state-drive
* https://hddmag.com/sas-vs-sata/

## SATA drive to SAP interface

### Yes, SATA drive can be connected to SAP backplane

* https://serverfault.com/questions/52092/can-sas-drives-be-used-with-sata-controllers
* https://en.wikipedia.org/wiki/Serial_Attached_SCSI

SAS offers optional compatibility with Serial ATA (SATA), versions 2 and later. This allows the connection of SATA drives to most SAS backplanes or controllers. The reverse, connecting SAS drives to SATA backplanes, is not possible.

* https://www.seagate.com/gb/en/support/kb/connecting-sata-drive-to-sas-controller-006170en/

SAS controllers enable the use of SATA drives to expand the storage capacity with cost-effectiveness. 
The use of SATA hard drives on SAS controllers is made possible by the fact that both share the same infrastructure and have similar features.
 
* **SATA drives may be plugged into SAS controllers.**
* SAS drives cannot be plugged into SATA controllers.
 
There is a difference between the SAS and SATA connectors, and both includes power and data. On SATA drives, there is a separation between power and data, while with SAS drives it is unified. See figure:

## Why SATA SSD?

* Waaaay cheaper. Use in RAID 10 and have all the perks as in SAS but 10x cheaper.
