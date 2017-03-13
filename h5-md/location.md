# H5地理位置

#### HTML5 - 使用地理定位
请使用 getCurrentPosition() 方法来获得用户的位置。
下例是一个简单的地理定位实例，可返回用户位置的经度和纬度。
实例

```
<script>
var x=document.getElementById("demo");
function getLocation()
  {
  if (navigator.geolocation)
    {
    navigator.geolocation.getCurrentPosition(showPosition);
    }
  else{x.innerHTML="Geolocation is not supported by this browser.";}
  }
function showPosition(position)
  {
  x.innerHTML="Latitude: " + position.coords.latitude +
  "<br />Longitude: " + position.coords.longitude;
  }
</script>
```

例子解释：
检测是否支持地理定位
如果支持，则运行 getCurrentPosition() 方法。如果不支持，则向用户显示一段消息。
如果getCurrentPosition()运行成功，则向参数showPosition中规定的函数返回一个coordinates对象
showPosition() 函数获得并显示经度和纬度
上面的例子是一个非常基础的地理定位脚本，不含错误处理。
处理错误和拒绝
getCurrentPosition() 方法的第二个参数用于处理错误。它规定当获取用户位置失败时运行的函数：
实例

```
function showError(error) {
  switch(error.code) {
    case error.PERMISSION_DENIED:
      x.innerHTML="User denied the request for Geolocation."
      break;
    case error.POSITION_UNAVAILABLE:
      x.innerHTML="Location information is unavailable."
      break;
    case error.TIMEOUT:
      x.innerHTML="The request to get user location timed out."
      break;
    case error.UNKNOWN_ERROR:
      x.innerHTML="An unknown error occurred."
      break;
    }
  }

 ```

错误代码：
-Permission denied - 用户不允许地理定位
-Position unavailable - 无法获取当前位置
-Timeout - 操作超时