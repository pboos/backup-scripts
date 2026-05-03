# backup-scripts

## Usage

Install it as a daily cron job
```
curl https://raw.githubusercontent.com/pboos/backup-scripts/refs/heads/main/backup.sh -o /usr/local/bin/backup.sh
chmod +x /usr/local/bin/backup.sh

tee /etc/cron.daily/backup.sh <<-'EOF'
#!/bin/bash

/usr/local/bin/backup -c /etc/config.backup
EOF
chmod +x /etc/cron.daily/backup.sh
```

### Setup configuration
```
/usr/local/bin/backup  --init /etc/config.backup
```

And then edit `/etc/config.backup`.
