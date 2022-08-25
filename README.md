## How To Secure The Cookie
This is the most common way to set cookie in PHP, empty Variables will hold their default value

```setcookie($name, $value, $expire, $path, $domain, $secure, $httponly)```

## From Where This Vulnerability Come

A Insecure Way Could Look Like THis

```setcookie("NameOfCookie, "ValueOfCookie")```

## How To Secure The Cookie

It's Easy You Just Need To Replace The ```setcookie($cookieName, $cookieValue, 0, '/', $domain).``` to ```setcookie($cookieName, $cookieValue, 0, '/', $domain, false, false)```
