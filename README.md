# API documatation

You can write a basic server script like:

```php
<?php
$json = json_decode($_GET['json'], true);
$res = array("status"=>200, "statusText"=>"OK", "data"=>$json);
echo "myFunc(" . json_encode($res) . ")";
?>
```
And name the file `demo_json_encode_decode.php` and use it in a HTML page:
```html
<script type="application/javascript">
  window.onload = function() {
    var jsonStr = {"name":"John", "age":32};
    var json = JSON.parse(jsonStr)
    var elem = document.createElement("script");
    elem.src = "demo_json_encode_decode.php?json=" + json;
    document.body.appendChild(elem)
  }
  myFunc(json) {
    document.write(json.status + " " + json.statusText)
  }
</script>
```
