# backup-scripts

## Usage

Install it as a daily cron job
```
curl https://raw.githubusercontent.com/pboos/backup-scripts/refs/heads/main/backup.sh -o /usr/local/bin/backup
chmod +x /usr/local/bin/backup

tee /etc/cron.daily/backup <<-'EOF'
#!/bin/bash

/usr/local/bin/backup -c /etc/backup.config
EOF
chmod +x /etc/cron.daily/backup
```

### Setup configuration
```
/usr/local/bin/backup  --init /etc/backup.config
```

And then edit `/etc/backup.config`.
