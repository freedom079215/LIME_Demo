# LIME_demo
https://freedom079215.github.io/LIME_demo/index.html#/

# Get GA cookie
```js=
  window.onload = function(){
    if(threhold!= 1)
    {
    get_cookie();
    }
  }
  function cID(name) {
    var value = "; " + document.cookie;
    var parts = value.split("; " + name + "=");
    if (parts.length == 2) return parts.pop().split(";").shift();
  }
function get_cookie() {
    var cidL = cID("_ga");
    var cidL = cidL.split(".").length;
    var TSB_ga_Cookie = cID("_ga").split(".")[cidL-2] + "." + cID("_ga").split(".")[cidL-1];
    gtag('event', 'page_view', {
        'dimension2': TSB_ga_Cookie
        });
   }
 ```