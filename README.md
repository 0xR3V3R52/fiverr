## How To Secure The Cookie
  This is the most common way to set cookie in PHP, empty Variables will hold their default value

    ```setcookie($name, $value, $expire, $path, $domain, $secure, $httponly)```

 # From Where This Vulnerability Come

    A Insecure Way Could Look Like THis

      ```setcookie("NameOfCookie, "ValueOfCookie")```

  # How To Secure The Cookie

      It's Easy You Just Need To Replace The ```setcookie($cookieName, $cookieValue, 0, '/', $domain).``` to ```setcookie($cookieName, $cookieValue, 0, '/', $domain, false, false)```

## Composer Configuration Disclosure
  # File Path: 
  ```https://careingtondentalsavings.com/wp-content/plugins/jetpack/composer.json```
  # Why This File Exist ?
     This File Have Package Name And Some Version And Configuration That Don't Have Any Impact Or Any Damage To Your Server
  # Solve
     There Is No Impact So There Is No Problem You Can Let it with no damage
     
## Information Disclosure
 # Found At: 
    ```https://careingtondentalsavings.com/wp-json/oembed/1.0/embed && https://careingtondentalsavings.com/wp-json/wp/v2/users```
 # First Url:  
    ```https://careingtondentalsavings.com/wp-json/oembed/1.0/embed```
          - After Some Enumeration I Found The Url Can Take An Url: https://careingtondentalsavings.com/wp-json/oembed/1.0/embed?url= But We Can't Exploit It There Is No Impact Here
 # Second Url: 
   ```https://careingtondentalsavings.com/wp-json/wp/v2/users ```
         - After Enter At This Url You Will Find Some Sensitive Data Email And Users For The Wordpress Users
         image: https://user-images.githubusercontent.com/110203763/186719191-e5a336e5-afea-471b-92bf-dd81b28303d7.png
     # How We Can Solve This Issue
         - solution: read this blog > https://www.getastra.com/blog/knowledge-base/disable-wp-api-json-in-wp/
     

## Cookie Is Not Set To Be HttpOnly
    #Set HttpOnly cookie in PHP
        The following line sets the HttpOnly flag for session cookies - make sure to call it before you call session_start():
        ```ini_set("session.cookie_httponly", True);```
    # This is the most common way to set cookies in PHP, empty variables will hold their default value.
       ```setcookie($name, $value, $expire, $path, $domain, $secure, $httponly);```
       
    # Solving Problem Solution:
         solution: ```setcookie($cookieName, $cookieValue, 0, '/', $domain, false, true)```        

## Cookie-Based Cross Site Scripting (XSS)
   Found At: https://careingtondentalsavings.com/search/search.cgi
   #Impact: 
    There is not impact here and it's already solved by wordpress
