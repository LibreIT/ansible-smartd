[![Build Status](https://travis-ci.org/LibreIT/ansible-smartd.png?branch=master)](https://travis-ci.org/LibreIT/ansible-smartd)

smartd
========

Configure smartd (smartmontool) for each HDDs/SSDs with scheduled auto-check (short and long).


Requirements
------------

HDDs/SSDs with S.M.A.R.T. supported, otherwise role fails.

Role Variables
--------------

    smartd_short_test_month: '..'     # month to start short test (two decimal digits: 01 - 12)
    smartd_short_test_dom: '..'       # day of the month to start short test (two decimal digits: 01 - 31)
    smartd_short_test_dow: '.'        # day of the week to start short test (one decimal digit: 1 - 7)
    smartd_short_test_hour: 'random'  # hour of the day to start short test (two decimal digits: 00 - 23)
    
    smartd_long_test_month: '..'      # month to start long test (two decimal digits: 01 - 12)
    smartd_long_test_dom: '..'        # day of the month to start long test (two decimal digits: 01 - 31)
    smartd_long_test_dow: 'random'    # day of the week to start long test (one decimal digit: 1 - 7)
    smartd_long_test_hour: 'random'   # hour of the day to start long test (two decimal digits: 00 - 23)

A randomization of scheduled time (hour,dow) is enabled to avoid to test many disks in the same time. 

Note: "." (dot) are like "?" wildcard in smartd config. Example: smartd_short_test_month with '..' value is executed every month.

Example
========

    - hosts: example
      roles:
         - { role: kalos.smartd }


License
-------

GPLv3

Author Information
------------------

Calogero Lo Leggio (kalos) - http://LibreIT.org
