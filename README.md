# plain.angular
- Create new web application project
    - Empty
- Add index.html page on the root
    - Add something to the body
    - Run and test
- Add NuGet Package
    - Right click on references for web project
    - Manage NuGet Package...
    - Search for "angularjs"
        - Install
            - AngularJS Core
            - AngularJS Route
- Add index.html to the root of the project
- Add script tag to references js files
```
<script src="Scripts/angular.min.js"></script>
```
- Add app folder to the root of the project
    - Add sub folders
        - bootstrap
        - controllers
        - factories
        - views
- Add app.js in bootstrap folder
```
window.app = angular.module('plainjane', []);
```
- Add ng-app=‘leadintake’ to HTML tag in index.html
```
<html ng-app="plainjane">
```
- Add mainController.js in controllers folder
```
window.app.controller('appController', appController);

appController.$inject = [];

function appController() {

    var vm = this;
    vm.messageInput = 'Hello There';

}
```
- Add script references
```
<script src="app/*.js"></script>
```
- Add <div> tag in index.html
```
    <div ng-controller="appController as appCtrl">
        <input type="text" ng-model="appCtrl.messageInput" placeholder="Enter a Message"/>
        <label>Message: {{ appCtrl.messageInput }}</label>
    </div>
```
