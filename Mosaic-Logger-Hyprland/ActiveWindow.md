timestamp: i64
program: String
title: String

[Log](Log)(ActiveWindow) {
	timestamp: ActiveWindow.timestamp
	data.push([Datum](Datum)::[Label](Label)(ActiveWindow.program))
	data.push([Datum](Datum)::[Description](Description)(ActiveWindow.title))
}