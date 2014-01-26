smartd
========

Configure smartd (smartmontool) for each HDDs/SSDs with scheduled auto-check (short and long).


Requirements
------------

HDDs/SSDs with S.M.A.R.T. enabled.
(if S.M.A.R.T. is not supported/enabled, role fails.)

Role Variables
--------------

  **smartd_short_test_month** - month to start test (two decimal digits: 01 - 12)

  **smartd_short_test_dom** - day of the month to start test (two decimal digits: 01 - 31)

  **smartd_short_test_dow** - day of the week to start test (one decimal digit: 1 - 7)

  **smartd_short_test_hour** - hour of the day to start test (two decimal digits: 00 - 23)  
  If this variable is not defined the value is random

  **smartd_long_test_month** - month to start test (two decimal digits: 01 - 12)

  **smartd_long_test_dom** - day of the month to start test (two decimal digits: 01 - 31)

  **smartd_long_test_dow** - day of the week to start test (one decimal digit: 1 - 7)  
  If this variable is not defined the value is random

  **smartd_long_test_hour** - hour of the day to start test (two decimal digits: 00 - 23)  
  If this variable is not defined the value is random  

A randomization of scheduled time (hour,dow) is enabled to avoid to test many disks in the same time. 

Note: "." (dot) are like "?" wildcard in smartd config.

License
-------

GPLv3

Author Information
------------------

Calogero Lo Leggio (kalos) - http://LibreIT.org
