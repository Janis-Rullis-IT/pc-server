# RAID-on-SSD

* https://www.kjctech.net/why-raid-5-is-ok-on-ssd-drives/#:~:text=Surprisingly%2C%20it%20seems%20to%20be,failed%20drive%20is%20hugely%20reduced.

A single solid state drive (SSD) RAID array can offer performance which is comparable to many HDD RAID arrays, and is therefore often seen as an alternative to an SSD RAID array.

* https://www.enterprisestorageforum.com/storage-hardware/ssd-raid.html
* https://ssdcompares.com/best-raid-choice-ssd-array/
* https://insights.samsung.com/2020/08/04/is-it-time-to-replace-your-raid-storage-with-ssds-3/
* https://superuser.com/a/232344
* https://www.diskinternals.com/raid-recovery/move-from-hdd-raid-to-ssd/
* https://www.starwindsoftware.com/blog/raid-5-was-great-until-high-capacity-hdds-came-into-play-but-ssds-restored-its-former-glory-2
* https://www.diskinternals.com/raid-recovery/raid-1-vs-raid-5/
* https://www.diffen.com/difference/RAID-1-vs-RAID-5

## 5 or 10 (1+0)

### 5 if 3 SSDs, 10 if 4 SSDs

* https://www.diskinternals.com/raid-recovery/raid-5-vs-raid-10/

* 10 is faster but not storage effective (min 4 disks, lose half the storage).

## 5 or 0 ?

### 5 it is

* 5 is faster but has a lot of writes to provide the speed and mirroring.
* 1 is just mirroring to the 2nd HDD.

### Will the speed gained from 5 will be worth the writes?

#### Yes, it is

> SSD lifetime depends on writes.
* RAID 5 just like RAID 0 uses stripping which is SPEED!

Nearly 2x the speed.

![https://www.enterprisestorageforum.com/imagesvr_ce/9609/RAIDBenchmarks.png](https://www.enterprisestorageforum.com/imagesvr_ce/9609/RAIDBenchmarks.png)
