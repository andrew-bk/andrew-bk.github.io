---
layout: post
title: Subtract tow dates with Apache Drill
tags: [apache drill]
---

Apache Drill is a fantastic SQL on Hadoop solution and comes with a large nmber of SL functinos for manipulating your data.
However, despite a variety of date functions there is no simple way to calculate the difference between two dates or timestamps
and get the result as a number.

    SELECT DATEDIFF(check_in_date, check_out_date) FROM hotel_booking;

Drill provides the AGE() function for substracting two dates.  However this results in a coded alphanumeric string whose data type is INTERVAL

For example

    SELECT AGE(check_in_date, check_out_date) FROM hotel_booking;

    | expr$01 |
    | P0Y0M0D3 |


The quick and dirty approach is use the UNIX_TIMESTAMP() function to convert


This is the first post

These are the tings I could write about:

- apache drill date arithmetic using the timestamp rather than AGE, issue with the interval
- jsonpath
- drill
- apache zeppelin
-
-
- spark
- ignite
-