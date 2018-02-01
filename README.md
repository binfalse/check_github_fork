# Monitor the status of a fork on GitHub (and similar)

This script can be used to monitor forks on Github (and similar repository hosters).
You will automatically get notified if your for is ahead or behind its origin.

The script basically just retrieves GitHub's web page for the project and check if it can find the string

    This branch is .* behind

or

    This branch is .* ahead

If found, the script will exit with return code `1` and a message for your monitoring system (Nagios/Icinga/etc).

## Options

A few command line arguments are accepted:

* `--only-ahead` only check for forks being *ahead* and disable the check for *behind*
* `--only-behind` only check for forks being *behind* and disable the check for *ahead*
* `--critical` if the check fails it won't return code `1`, but `2`. Thus, your monitoring solution will think this is critical!
* `-h` show a help page


## LICENSE

        check_github_fork - Check status of github forks
        Copyright (C) 2018 Martin Scharm <https://binfalse.de/contact/>

        This program is free software: you can redistribute it and/or modify
        it under the terms of the GNU General Public License as published by
        the Free Software Foundation, either version 3 of the License, or
        (at your option) any later version.

        This program is distributed in the hope that it will be useful,
        but WITHOUT ANY WARRANTY; without even the implied warranty of
        MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
        GNU General Public License for more details.

        You should have received a copy of the GNU General Public License
        along with this program.  If not, see <http://www.gnu.org/licenses/>.







