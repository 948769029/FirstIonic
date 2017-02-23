# FirstIonic
##ionic自定义插件的使用
1在Staging/www/template/tab-dash.html中添加
```
<div ng-controller="CustomMethodController">
        <button ng-click="handleClick()">点击</button>
    </div>
```
2在Staging/www/js/controllers.js中添加
```
.controller('CustomMethodController', function($scope){
$scope.handleClick = function() {
successCallBack = function(num) {
alert(num);
}
errorCallBack = function(data) {
alert(data);
}
cordova.plugins.ZJPlugman.coolMethod("调用成功了~",successCallBack,errorCallBack);
}
})
```

