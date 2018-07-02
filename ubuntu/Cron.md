# Cron

* [crontab.guru](https://crontab.guru/#*/5_*_*_*_*)
* [How do I set up a Cron job? (askubuntu.com)](https://askubuntu.com/a/2369)
* [How To Use Cron To Automate Tasks On a VPS (digitalocean.com)](https://www.digitalocean.com/community/tutorials/how-to-use-cron-to-automate-tasks-on-a-vps#examples)
* [CronHowto (help.ubuntu.com)](https://help.ubuntu.com/community/CronHowto)

## Formtat

```
m h  dom mon dow   command
```

## Example script

```shell
#!/bin/bash
cd /app
echo "DUB" > /app/cron-dub.log
```

## [To run a command every 5th minute on the hour:](https://crontab.guru/#*/5_*_*_*_*)

```
*/5 * * * * sh /app/cron-mix.sh
```

## Every minute

```
* * * * * sh /app/cron-mix.sh
```

## To run a command every Tuesday at 4:00am, you’d use:
```
0 4 * * 2 sh /app/cron-mix.sh
```

## Successfully added

```
no crontab for root - using an empty one
crontab: installing new crontab
```

## Failure

```
Do you want to retry the same edit? (y/n) y
crontab: installing new crontab
"/tmp/crontab.ny6t0g/crontab":23: bad minute
```

## `crontab` commands

* -e - edit.
* -l - list.
* -r - delete.


## Service

### Status

```shell
service cron status
```
> [FAIL] cron is not running ... failed!

### Start

```shell
service cron start
```
> [ ok ] Starting periodic command scheduler: cron.
