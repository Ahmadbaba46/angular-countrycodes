# Angular Country Codes Module
Simple AngularJs module to provide telephone country code data

## Installation
### Install with Bower
```bash
# from the terminal at the root of your project
bower install angular-countrycodes --save
```
If you're not using wiredep you'll obviously also need to include the script in your html.

### Add to your module deps
```js
angular.module('xxxx', ['mcwebb.countrycodes'])
```

## Example Use
### Configure favoured countries
If you want, you can configure which countries will be returned at the top of the list. By default they'll just show A-Z.
For each country you want add it's ISO Alpha-2 code to an array in the preferredCountries config method.
```js
angular.module('xxxx')
.config(function (CountryCodesProvider) {
	CountryCodesProvider.preferredCountries(['gb', 'us']);
});
```
### Get List
```js
angular.module('xxxx')
.controller('SignupController', function SignupController($scope, CountryCodes) {
	$scope.countries = CountryCodes.getList();
});
```
