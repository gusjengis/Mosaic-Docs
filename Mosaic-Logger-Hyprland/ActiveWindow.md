timestamp: i64
program: String
title: String

[Log](Log)(ActiveWindow) {
	timestamp: ActiveWindow.timestamp
	data.push([Datum](Datum)::[Label](Label)(ActiveWindow.program))
	data.push([Datum](Datum)::[Description](Description)(ActiveWindow.title))
}

[Interval](Interval)(Prev_ActiveWindow: [Log](Log), ActiveWindow: [Log](Log)){
	start: Prev_ActiveWindow.timestamp
	end: ActiveWindow.timestamp
	data: Prev_ActiveWindow.data
}