# Synth

Synth was built with ease of use in mind. Here you'll find a full list of all the quirks and features Synth has to offer.

While Synth may look finished, *we still have plenty of ideas, plans, and upcoming features for Synth* so please stay tuned for those! Also, if you find any issues with the bot, be sure to make a ticket in the issues section for this repository

## Purpose

Synth aims to provide all your bot needs. I've always found it a pain managing multiple bots with their prefixes and confusing features. It all becomes too much too quick. The focus of Synth is to eliminate the need of many bots by consolidating all the important features that many different bots provide into one bot.

**You could shop at six stores, or just one.** - that's the idea

## Planned Features

Head over to the project for this repository to check out some of the stuff we have planned for Synth.

### Setup

To run Synth, you'll need to download and install the latest MySQL server. You can download a copy [here](https://dev.mysql.com/downloads/installer/). You'll also need a copy of node.js. You can also find that [here](https://nodejs.org/en/download/). Then, you'll need to create your own `.env` file. This file will store sensitive information about Synth and your database (bot token, database username and password, etc.) To set up the file, just copy and paste this text and insert your own data into it. Put the file anywhere in the main directory for Synth.

```
TOKEN = Your bot token here
USER = Your database user here
PASSWORD = Your database password here
DATABASE = Your database name here
```

Next, head to your MySQL server `my.ini` file. The default install location for the file is `C:\ProgramData\MySQL\MySQL Server X.Y\my.ini`. You'll need to add these lines of code to the file.

* Under `\[client\]`:
    `default-character-set = utf8mb4`

* Under `\[mysql\]`:
    `default-character-set = utf8mb4`

* Under `\[mysqld\]`:
    ```
    character-set-server = utf8mb4
    collation-server = utf8mb4_unicode_ci
    init_connect = 'SET collation_connection = utf8mb4_unicode_ci'
    init-connect = 'SET NAMES utf8mb4'
    ```

After all that's set up, open the MySQL terminal and `schema.sql` in the main directory of Synth. Log into the MySQL server and copy and paste the contents of `schema.sql` into the terminal. Once that's done. Open up the command prompt, CD into the folder where synth is stored, and run the `node .` command.