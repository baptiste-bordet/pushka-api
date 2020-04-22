# Pushka Strapi application

## DB dump

### connection to heroku

`heroku ps:exec`

and go to `.tmp` directory

### send the file encrypted

`cat data.db | gpg -ac -o- | curl -X PUT -T "-" https://transfer.sh/pushkaDB.gpg`

if `Inappropriate ioctl for device` error, execute `export GPG_TTY=$(tty)`

### download the file on the local machine

`curl https://transfer.sh/6Izov/pushkaDB.gpg | gpg -o- > dump.db`
