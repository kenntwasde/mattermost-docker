### 10.06.2016/MN
	* Mattermost 3.0.3
		* [upgrade statements](http://docs.mattermost.com/administration/upgrade.html)
		* [mattermost Changelog V3.0.3](http://docs.mattermost.com/administration/changelog.html#release-v3-0-3)
	* if you want to upgrade from 2.2.0
		* SAVE everything!
		* docker-compose build   # build new version
		* docker-compose start db
		* docker-compose run --entrypoint /bin/bash app
		* (in container) cd /mattermost/bin
		* (in container) ./platform -upgrade_db_30      # do db-upgrade
		* (in container) exit
		* docker-compose stop; docker-compose up  # or start
### 24.04.2016/MN
* added docker-compose-behindnginx.yml
	- uses version '2'
	- use loopback for port binding (no public accessable ports!)
### 22.04.2016/MN
* forked from mattermmost/mattermost-docker
* mattermost V2.2.0
- added .gitignore - files
