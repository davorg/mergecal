# mergecal

Simple program to merge iCal files.

## Description

I keep my life in Google. My wife keeps hers in iCloud. We wanted access
to each others' calendars. But the useful bits of my calendar are spread
across several different Google calendars and I wanted to combine them
into a single iCal feed that my wife could subscribe to.

I was surprised to see that this didn't seem to exist as a service (or,
at least, if it does, half an hour of Googling couldn't find it - I think
Yahoo! Pipes would have done it). But half an hour of Perl hacking produced
this simple program which uses the
(Text::vFiles::asData)[https://metacpan.org/release/Text-vFile-asData]
module.

There's a very simple config file. Give your new combined calendar a title
and a list of iCal URLs. Run the program like this:

    $ mergecal config.json > combined.ics

Then put `combined.ics` somewhere on the web so iCloud (or whatever) can
see it.
