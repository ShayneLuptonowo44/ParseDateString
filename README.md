# ParseDateString
sion: 1.00. AutoIt: V3.3.8.1 ; Parse a date string to the format of YYYY/MM/DD HH:MM:SS as certain formats can use '.' or '-' in certain system locales. Func _ParseDateString($sDateString)     Return StringReplace(StringRegExpReplace(StringStripWS($sDateString, 8), '(d{4})D?(d{2})D?(d{2})(d{0,2})D?(d{0,2})D?(d{0,2})', '1/2/3 4:5:6'), ' ::', '') ; Can this be improved in anyway? EndFunc   ;==>_ParseDateString  Func Output($sString)     Return ConsoleWrite('[' &amp; $sString &amp; '] >> ' &amp; _ParseDateString($sString) &amp; @CRLF) EndFunc   ;==>Output
