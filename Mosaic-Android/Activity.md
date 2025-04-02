timestamp: i64
label: String

[Log](Log)(Activity)
timestamp: Activity.timstamp
[Datum](Datum)::[Label](Label)(Activity.label)

[Interval](Interval)(Activity1, Activity)
start: Activity1.timestamp