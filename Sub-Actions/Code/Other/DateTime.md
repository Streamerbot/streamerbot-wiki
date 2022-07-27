---
title: Custom Date and Time format strings
description: 
published: true
date: 2022-07-27T23:41:16.498Z
tags: 
editor: markdown
dateCreated: 2022-07-27T23:41:16.498Z
---



| Format | Description | Example
|:--:|:--|:--- 
| *d*{.datatype} | The day of the month, from 1 through 31.<br /><br /> More information: [The "d" Custom Format Specifier](#dSpecifier). | 2009-06-01T13:45:30 -> 1<br /><br /> 2009-06-15T13:45:30 -> 15 |
| *dd*{.datatype} | The day of the month, from 01 through 31.<br /><br /> More information: [The "dd" Custom Format Specifier](#ddSpecifier). | 2009-06-01T13:45:30 -> 01<br /><br /> 2009-06-15T13:45:30 -> 15 |
| *ddd*{.datatype} | The abbreviated name of the day of the week.<br /><br /> More information: [The "ddd" Custom Format Specifier](#dddSpecifier). | 2009-06-15T13:45:30 -> Mon (en-US)<br /><br /> 2009-06-15T13:45:30 -> Пн (ru-RU)<br /><br /> 2009-06-15T13:45:30 -> lun. (fr-FR) |
| *dddd*{.datatype} | The full name of the day of the week.<br /><br /> More information: [The "dddd" Custom Format Specifier](#ddddSpecifier). | 2009-06-15T13:45:30 -> Monday (en-US)<br /><br /> 2009-06-15T13:45:30 -> понедельник (ru-RU)<br /><br /> 2009-06-15T13:45:30 -> lundi (fr-FR) |
| *f*{.datatype} | The tenths of a second in a date and time value.<br /><br /> More information: [The "f" Custom Format Specifier](#fSpecifier). | 2009-06-15T13:45:30.6170000 -> 6<br /><br /> 2009-06-15T13:45:30.05 -> 0 |
| *ff*{.datatype} | The hundredths of a second in a date and time value.<br /><br /> More information: [The "ff" Custom Format Specifier](#ffSpecifier). | 2009-06-15T13:45:30.6170000 -> 61<br /><br /> 2009-06-15T13:45:30.0050000 -> 00 |
| *fff*{.datatype} | The milliseconds in a date and time value.<br /><br /> More information: [The "fff" Custom Format Specifier](#fffSpecifier). | 6/15/2009 13:45:30.617 -> 617<br /><br /> 6/15/2009 13:45:30.0005 -> 000 |
| *ffff*{.datatype} | The ten thousandths of a second in a date and time value.<br /><br /> More information: [The "ffff" Custom Format Specifier](#ffffSpecifier). | 2009-06-15T13:45:30.6175000 -> 6175<br /><br /> 2009-06-15T13:45:30.0000500  -> 0000 |
| *fffff*{.datatype} | The hundred thousandths of a second in a date and time value.<br /><br /> More information: [The "fffff" Custom Format Specifier](#fffffSpecifier). | 2009-06-15T13:45:30.6175400 -> 61754<br /><br /> 6/15/2009 13:45:30.000005 -> 00000 |
| *ffffff*{.datatype} | The millionths of a second in a date and time value.<br /><br /> More information: [The "ffffff" Custom Format Specifier](#ffffffSpecifier). | 2009-06-15T13:45:30.6175420 -> 617542<br /><br /> 2009-06-15T13:45:30.0000005 -> 000000 |
| *fffffff*{.datatype} | The ten millionths of a second in a date and time value.<br /><br /> More information: [The "fffffff" Custom Format Specifier](#fffffffSpecifier). | 2009-06-15T13:45:30.6175425 -> 6175425<br /><br /> 2009-06-15T13:45:30.0001150 -> 0001150 |
| *F*{.datatype} | If non-zero, the tenths of a second in a date and time value.<br /><br /> More information: [The "F" Custom Format Specifier](#F_Specifier). | 2009-06-15T13:45:30.6170000 -> 6<br /><br /> 2009-06-15T13:45:30.0500000 -> (no output) |
| *FF*{.datatype} | If non-zero, the hundredths of a second in a date and time value.<br /><br /> More information: [The "FF" Custom Format Specifier](#FF_Specifier). | 2009-06-15T13:45:30.6170000 -> 61<br /><br /> 2009-06-15T13:45:30.0050000 -> (no output) |
| *FFF*{.datatype} | If non-zero, the milliseconds in a date and time value.<br /><br /> More information: [The "FFF" Custom Format Specifier](#FFF_Specifier). | 2009-06-15T13:45:30.6170000 -> 617<br /><br /> 2009-06-15T13:45:30.0005000 -> (no output) |
| *FFFF*{.datatype} | If non-zero, the ten thousandths of a second in a date and time value.<br /><br /> More information: [The "FFFF" Custom Format Specifier](#FFFF_Specifier). | 2009-06-15T13:45:30.5275000 -> 5275<br /><br /> 2009-06-15T13:45:30.0000500 -> (no output) |
| *FFFFF*{.datatype} | If non-zero, the hundred thousandths of a second in a date and time value.<br /><br /> More information: [The "FFFFF" Custom Format Specifier](#FFFFF_Specifier). | 2009-06-15T13:45:30.6175400 -> 61754<br /><br /> 2009-06-15T13:45:30.0000050 -> (no output) |
| *FFFFFF*{.datatype} | If non-zero, the millionths of a second in a date and time value.<br /><br /> More information: [The "FFFFFF" Custom Format Specifier](#FFFFFF_Specifier). | 2009-06-15T13:45:30.6175420 -> 617542<br /><br /> 2009-06-15T13:45:30.0000005 -> (no output) |
| "FFFFFFF" | If non-zero, the ten millionths of a second in a date and time value.<br /><br /> More information: [The "FFFFFFF" Custom Format Specifier](#FFFFFFF_Specifier). | 2009-06-15T13:45:30.6175425 -> 6175425<br /><br /> 2009-06-15T13:45:30.0001150 -> 000115 |
| "g", "gg" | The period or era.<br /><br /> More information: [The "g" or "gg" Custom Format Specifier](#gSpecifier). | 2009-06-15T13:45:30.6170000 -> A.D. |
| "h" | The hour, using a 12-hour clock from 1 to 12.<br /><br /> More information: [The "h" Custom Format Specifier](#hSpecifier). | 2009-06-15T01:45:30 -> 1<br /><br /> 2009-06-15T13:45:30 -> 1 |
| "hh" | The hour, using a 12-hour clock from 01 to 12.<br /><br /> More information: [The "hh" Custom Format Specifier](#hhSpecifier). | 2009-06-15T01:45:30 -> 01<br /><br /> 2009-06-15T13:45:30 -> 01 |
| "H" | The hour, using a 24-hour clock from 0 to 23.<br /><br /> More information: [The "H" Custom Format Specifier](#H_Specifier). | 2009-06-15T01:45:30 -> 1<br /><br /> 2009-06-15T13:45:30 -> 13 |
| "HH" | The hour, using a 24-hour clock from 00 to 23.<br /><br /> More information: [The "HH" Custom Format Specifier](#HH_Specifier). | 2009-06-15T01:45:30 -> 01<br /><br /> 2009-06-15T13:45:30 -> 13 |
| "K" | Time zone information.<br /><br /> More information: [The "K" Custom Format Specifier](#KSpecifier). | With <xref:System.DateTime> values:<br /><br /> 2009-06-15T13:45:30, Kind Unspecified -><br /><br /> 2009-06-15T13:45:30, Kind Utc -> Z<br /><br /> 2009-06-15T13:45:30, Kind Local -> -07:00 (depends on local computer settings)<br /><br /> With <xref:System.DateTimeOffset> values:<br /><br /> 2009-06-15T01:45:30-07:00 --> -07:00<br /><br /> 2009-06-15T08:45:30+00:00 --> +00:00 |
| "m" | The minute, from 0 through 59.<br /><br /> More information: [The "m" Custom Format Specifier](#mSpecifier). | 2009-06-15T01:09:30 -> 9<br /><br /> 2009-06-15T13:29:30 -> 29 |
| "mm" | The minute, from 00 through 59.<br /><br /> More information: [The "mm" Custom Format Specifier](#mmSpecifier). | 2009-06-15T01:09:30 -> 09<br /><br /> 2009-06-15T01:45:30 -> 45 |
| "M" | The month, from 1 through 12.<br /><br /> More information: [The "M" Custom Format Specifier](#M_Specifier). | 2009-06-15T13:45:30 -> 6 |
| "MM" | The month, from 01 through 12.<br /><br /> More information: [The "MM" Custom Format Specifier](#MM_Specifier). | 2009-06-15T13:45:30 -> 06 |
| "MMM" | The abbreviated name of the month.<br /><br /> More information: [The "MMM" Custom Format Specifier](#MMM_Specifier). | 2009-06-15T13:45:30 -> Jun (en-US)<br /><br /> 2009-06-15T13:45:30 -> juin (fr-FR)<br /><br /> 2009-06-15T13:45:30 -> Jun (zu-ZA) |
| "MMMM" | The full name of the month.<br /><br /> More information: [The "MMMM" Custom Format Specifier](#MMMM_Specifier). | 2009-06-15T13:45:30 -> June (en-US)<br /><br /> 2009-06-15T13:45:30 -> juni (da-DK)<br /><br /> 2009-06-15T13:45:30 -> uJuni (zu-ZA) |
| "s" | The second, from 0 through 59.<br /><br /> More information: [The "s" Custom Format Specifier](#sSpecifier). | 2009-06-15T13:45:09 -> 9 |
| "ss" | The second, from 00 through 59.<br /><br /> More information: [The "ss" Custom Format Specifier](#ssSpecifier). | 2009-06-15T13:45:09 -> 09 |
| "t" | The first character of the AM/PM designator.<br /><br /> More information: [The "t" Custom Format Specifier](#tSpecifier). | 2009-06-15T13:45:30 -> P (en-US)<br /><br /> 2009-06-15T13:45:30 -> 午 (ja-JP)<br /><br /> 2009-06-15T13:45:30 ->  (fr-FR) |
| "tt" | The AM/PM designator.<br /><br /> More information: [The "tt" Custom Format Specifier](#ttSpecifier). | 2009-06-15T13:45:30 -> PM (en-US)<br /><br /> 2009-06-15T13:45:30 -> 午後 (ja-JP)<br /><br /> 2009-06-15T13:45:30 ->  (fr-FR) |
| "y" | The year, from 0 to 99.<br /><br /> More information: [The "y" Custom Format Specifier](#ySpecifier). | 0001-01-01T00:00:00 -> 1<br /><br /> 0900-01-01T00:00:00 -> 0<br /><br /> 1900-01-01T00:00:00 -> 0<br /><br /> 2009-06-15T13:45:30 -> 9<br /><br /> 2019-06-15T13:45:30 -> 19 |
| "yy" | The year, from 00 to 99.<br /><br /> More information: [The "yy" Custom Format Specifier](#yySpecifier). | 0001-01-01T00:00:00 -> 01<br /><br /> 0900-01-01T00:00:00 -> 00<br /><br /> 1900-01-01T00:00:00 -> 00<br /><br /> 2019-06-15T13:45:30 -> 19 |
| "yyy" | The year, with a minimum of three digits.<br /><br /> More information: [The "yyy" Custom Format Specifier](#yyySpecifier). | 0001-01-01T00:00:00 -> 001<br /><br /> 0900-01-01T00:00:00 -> 900<br /><br /> 1900-01-01T00:00:00 -> 1900<br /><br /> 2009-06-15T13:45:30 -> 2009 |
| "yyyy" | The year as a four-digit number.<br /><br /> More information: [The "yyyy" Custom Format Specifier](#yyyySpecifier). | 0001-01-01T00:00:00 -> 0001<br /><br /> 0900-01-01T00:00:00 -> 0900<br /><br /> 1900-01-01T00:00:00 -> 1900<br /><br /> 2009-06-15T13:45:30 -> 2009 |
| "yyyyy" | The year as a five-digit number.<br /><br /> More information: [The "yyyyy" Custom Format Specifier](#yyyyySpecifier). | 0001-01-01T00:00:00 -> 00001<br /><br /> 2009-06-15T13:45:30 -> 02009 |
| "z" | Hours offset from UTC, with no leading zeros.<br /><br /> More information: [The "z" Custom Format Specifier](#zSpecifier). | 2009-06-15T13:45:30-07:00 -> -7 |
| "zz" | Hours offset from UTC, with a leading zero for a single-digit value.<br /><br /> More information: [The "zz" Custom Format Specifier](#zzSpecifier). | 2009-06-15T13:45:30-07:00 -> -07 |
| "zzz" | Hours and minutes offset from UTC.<br /><br /> More information: [The "zzz" Custom Format Specifier](#zzzSpecifier). | 2009-06-15T13:45:30-07:00 -> -07:00 |
| ":" | The time separator.<br /><br /> More information: [The ":" Custom Format Specifier](#timeSeparator). | 2009-06-15T13:45:30 -> : (en-US)<br /><br /> 2009-06-15T13:45:30 -> . (it-IT)<br /><br /> 2009-06-15T13:45:30 -> : (ja-JP) |
| "/" | The date separator.<br /><br /> More Information: [The "/" Custom Format Specifier](#dateSeparator). | 2009-06-15T13:45:30 -> / (en-US)<br /><br /> 2009-06-15T13:45:30 -> - (ar-DZ)<br /><br /> 2009-06-15T13:45:30 -> . (tr-TR) |
| "*string*"<br /><br /> '*string*' | Literal string delimiter.<br /><br /> More information: [Character literals](#Literals). | 2009-06-15T13:45:30 ("arr:" h:m t) -> arr: 1:45 P<br /><br /> 2009-06-15T13:45:30 ('arr:' h:m t) -> arr: 1:45 P |
| % | Defines the following character as a custom format specifier.<br /><br /> More information:[Using Single Custom Format Specifiers](#UsingSingleSpecifiers). | 2009-06-15T13:45:30 (%h) -> 1 |
| &#92; | The escape character.<br /><br /> More information: [Character literals](#Literals) and [Using the Escape Character](#escape). | 2009-06-15T13:45:30 (h \h) -> 1 h |
| Any other character | The character is copied to the result string unchanged.<br /><br /> More information: [Character literals](#Literals). | 2009-06-15T01:45:30 (arr hh:mm t) -> arr 01:45 A |