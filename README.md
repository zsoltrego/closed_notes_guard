# Installation

## Compatibility
Redmine 6.1.x

### If installation dir "/var/lib/redmine" with Passenger:

```sh
$ cd /var/lib/redmine/plugins
$ git clone https://github.com/zsoltrego/redmine_closed_notes_guard.git
$ cd ..
$ bundle config set --local without 'development test'
$ bundle install
$ bundle exec rake redmine:plugins RAILS_ENV=production
$ touch tmp/restart.txt
```

### Test

1. Login with a standard user.
2. Create a test ticket and write some notes.
3. Close the ticket.
4. Check the ticket to see if you can write notes.
5. For settings open Admin → Plugins → Closed Notes Guard → Configure.
