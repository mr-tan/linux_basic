## Security and File Permissions ##

### WHAT: ###

CronJobs:

- schedule a repeating task
- crond service 

---

```bash
# Start Cron job 
[~]$ crontab -e

# Do not use sudo for cron job
# Add configuration
# m h   dom mon dow     command
  0 21  *   *   *       uptime >> /tmp/system-report.txt

# List crontab option
[~]$ crontab -h

# List all schedule jobs in cron
[~]$ crontab -l

# List cron jobs of the other user
[~]$ crontab -u <bob> -l

# View log files for cron jobs
[~]$ tail /var/log/syslog

# When cron ran
[~]$ cat /tmp/system-report.txt

```




