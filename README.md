[![Build Status](https://travis-ci.org/LibreIT/ansible-smartd.png?branch=master)](https://travis-ci.org/LibreIT/ansible-smartd)

smartd
========

Configure smartd (smartmontool) for each HDDs/SSDs with scheduled auto-check (short and long).


Requirements
------------

HDDs/SSDs with S.M.A.R.T. enabled.
(if S.M.A.R.T. is not supported/enabled, role fails.)

Role Variables
--------------

    smartd:
      short_test_month: '..' # month to start short test (two decimal digits: 01 - 12)
      short_test_dom: '..'   # day of the month to start short test (two decimal digits: 01 - 31)
      short_test_dow: '.'    # day of the week to start short test (one decimal digit: 1 - 7)
      short_test_hour: '02'  # hour of the day to start short test (two decimal digits: 00 - 23)
                             # note: if this variable is not defined the value is random
    
      long_test_month: '..'  # month to start long test (two decimal digits: 01 - 12)
      long_test_dom: '..'    # day of the month to start long test (two decimal digits: 01 - 31)
      long_test_dow: '1'     # day of the week to start long test (one decimal digit: 1 - 7)
                             # note: if this variable is not defined the value is random
      long_test_hour: '03'   # hour of the day to start long test (two decimal digits: 00 - 23)
                             # note: if this variable is not defined the value is random

A randomization of scheduled time (hour,dow) is enabled to avoid to test many disks in the same time. 

Note: "." (dot) are like "?" wildcard in smartd config.

License
-------

GPLv3

Author Information
------------------

Calogero Lo Leggio (kalos) - http://LibreIT.org
