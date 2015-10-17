nginx-fancyindex-console
===

An old-school DOS-like console theme for [nginx fancyindex](https://github.com/aperezdc/ngx-fancyindex).

![nginx-fancyindex-console](https://cloud.githubusercontent.com/assets/1896112/10561685/f8e5762c-74fa-11e5-831f-8e57b7b748d8.png)

####NOTE:
NGX-FANCYINDEX truncates the file name to 50 characters subtracts 3 and then
appends a "..>" to the truncated name. This can be fixed by recompiling
NGX-FANCYINDEX after changing line 55 of "ngx_http_fancyindex_module.c":

From:

    #define NGX_HTTP_FANCYINDEX_NAME_LEN 50

To:

    #define NGX_HTTP_FANCYINDEX_NAME_LEN 500 (or some other number greater than 50)

#####Usage:
 - Compile nginx with the fancyindex module.
 - Include the contents of 'fancyindex.conf' in your location directive of your nginx conf.
 - copy the remaining items in your web root under 'fancyindex'.
  - header.html
  - footer.html
  - css/fancyindex.css
  - js/history.js
 - Restart your nginx server.

####Credits:

Based on [Nginx-Fancyindex-Theme](https://raw.githubusercontent.com/TheInsomniac/Nginx-Fancyindex-Theme).
