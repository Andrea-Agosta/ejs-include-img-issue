
# ejs-include-img-issue
Repository created be include in a question for [Stackoverflow](https://stackoverflow.com/questions/68002696/ejs-includes-header-but-in-some-page-dont-load-image)

### Question
My project and for some reason when I include the header and footer on `home.ejs`, I can see the image on the `navbar`, but if I do the same in `terms-condition.ejs`, node load the page correctly with the `footer` and the `navbar`, but the `logo-image` isn't shown in the page. The only difference between `home.ejs` and `terms-condition.ejs` is that the last one is in a subfolder of `/views`.



## Solution by [Viral Patel](https://stackoverflow.com/users/14079497/viral-patel)

You need to prefix the  `images/Stack_Overflow_icon.svg`  with  `/`  i.g.  `/images/Stack_Overflow_icon.svg`. In your code, did you notice that the  `styles.css`  loading correctly because you've prefix it with  `/`.

You're facing this issue because the file  `terms-condition.ejs`  is within a folder whereas  `home.ejs`  not.

P.S. You should always put  `node_modules`  in  `.gitignore`  file.

