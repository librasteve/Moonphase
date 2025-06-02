# Moonphase

# Synopsis

```raku
use Moonphase;

my @tests = ( 
    { :desc("New Moon (approx.)"),       :ts(1704067200) }, # Jan 1, 2024
    { :desc("First Quarter (approx.)"),  :ts(1704585600) }, # Jan 7, 2024
    { :desc("Full Moon (approx.)"),      :ts(1705017600) }, # Jan 12, 2024
    { :desc("Last Quarter (approx.)"),   :ts(1705449600) }, # Jan 17, 2024
    { :desc("Random date"),              :ts(1711920000) }, # April 1, 2024
    { :desc("Unix Epoch"),               :ts(0) }            # Jan 1, 1970
);

for @tests -> %test {
    my $radians = moonphase(%test<ts>);
    say "%test<desc>:";
    say "  Timestamp: %test<ts>";
    say "  Moon phase (radians): $radians";
    say "  Degrees: { $radians * 180 / pi }"; 
    say ""; 
}
```

# Description

Adapted from "moontool.c" by John Walker: See http://www.fourmilab.ch/moontool/

Inspired by https://github.com/oliverkwebb/moonphase/tree/main

Copyright 2024 Henley Cloud Consulting Ltd. 

