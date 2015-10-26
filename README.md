# YYYY-date
Simple example of the pitfalls of using *YYYY* versus *yyyy* when formatting dates

From: https://developer.apple.com/library/ios/documentation/Cocoa/Conceptual/DataFormatting/DataFormatting.html

There are two things to note about this example:
It uses *yyyy* to specify the year component. A common mistake is to use *YYYY*. *yyyy* specifies 
the calendar year whereas *YYYY* specifies the year (of “Week of Year”), used in the ISO year-week 
calendar. In most cases, *yyyy* and *YYYY* yield the same number, however they may be different. 
Typically you should use the calendar year.

What does this mean? Basically, any day (starting with Sunday) in the week of January 1 will report
the same year as January 1. 
So for December 29, 2014...Since January 1, 2015 is a Thursday, then all days from Dec 28, 29, 30, and 31 will report 2015 as the date.
