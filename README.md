# JavascriptWordLimit
Java script word limit in HTML form fields.


#Javascript word limit
--------

*By Prakash Bhandari
(http://www.prakashbhandari.com.np/)*

*Licensed under the MIT license: http://opensource.org/licenses/MIT*


Overview
--------
Java script word limit in HTML form fields.

Call function on KeyUp
--------

```html
<form action="">
<input  onkeyup="limitText(this.form.user_name,'name_limit',3)" name="user_name" type="text" value="">"
</form>
```


Include the javascript code in html page

```javascript
<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js"></script>
<script language="javascript" type="text/javascript">
    limitText = function(limitField, limitCount, limitNum){
        var words =  limitField.value.split(' ');
        if (words.length > limitNum) {
            words.splice(limitNum);
            limitField.value = words.join(" ");
        }
        else {
            $("."+limitCount).text(limitNum - words.length);
        }
    }
</script>```