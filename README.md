# ZeOmega_AngularJS


    Setup Instructions
        1. Microsoft Visual Code - https://code.visualstudio.com/
        2. NodeJS - https://nodejs.org/en/
            - node -v
            - npm -v
        3. Install static server - sudo npm install -g http-server

    JQuery vs AngularJS
        1. DOM manipulation is taken care of by AngularJS Framework.
        2. Less JS in Angular, less complexity
        3. AngularJS is a framework - comprehensive solution for UI stuff

    AnguarJS Basics
        1. AngularJS Module : angular.module
        2. MVC pattern in AngularJS - Separation of concerns  angular.controller($scope)
        3. MVW - Module View Whatever
        4. Model ($scope)
        5. With each controller, you get a unique $scope object
        6. Each controller scope is extention of $rootScope (super-parent)
        7. $rootScope, associated with Module (module-level) - can contain common methods and fields but it is bad practice to put to much content.
        8. Controller scopes which are direct/indirect extensions of scope.
        9. Factories - factory for common objects that can be shared by different controllers.

    Exercises post session.
        1. Enter any text into a text box and capitalize it. 
            Eg. "todAY is a SUNNy day!!" --> "Today is a sunny day"
        2. Enter any color into text box and that should become background color of a para.
            Eg. "red" in text box, para will become red in color

    Using Filters 
        1. Data manipulation is controller's responsibility but when you want to present in a view it becomes responsibility of Filters
            - Formatters and Filters
        Existing filters
            uppercase, lowercase, date, limitTo, orderBy, filter
        Custom filters
            capitalize
            Create a custom filter to reverse a string.
        Generate raw json data : https://www.mockaroo.com/

    Directives: Custom tag as a component (self-sufficient)
        Built in Directives 
            Already avaible in the library
            ng-app, ng-controller, ng-repeat, ng-if
        Custom Tags <notepad/>
            1. template: HTML content of the tag
            2. restrict: to restrict it to element(E) or attribute(A) or class(C) or combination (ACE) of all three.
            3. link (scope, element, attrs)
                scope -> The scope in which your directive is placed
                element -> JQLite (subset of Jquery) wrapped element, in which you call 90% of jquery methods (addClass, removeClass, bind ....)
                attrs -> Get the attribute values
            4. Transclude ; transclude: true, ng-transclude
            5. Isolation in scope { @}
        Dynamic custom tag
    
    Exercise:
     
        1. Create card directives and provide a search feature on the title using filters.
        https://getbootstrap.com/docs/4.0/components/card/


    Server side communication

        REST Api's
        - Hard coded .json url
        - Server side code to consume and produce json info 
        - Server side (Java, .NET, PHP, NodeJS)
        - $http service
        - $http is configurable (set headers, status code, status text)
        - $resource


        NodeJS
            - Create a configuration file using npm init -> package.json
            - npm install express

            Steps
            1. Configuration file - npm init - package.json
            2. npm install <dependency> - express, body-parser
            3. .js and write express code


    Callbacks vs Promises

    1. CAllback 
    function doSomething(callback){
        setTimeout(() => {
            console.log('Do Something')
            callback("success")
        }, 5000)
            
        }
    doSomething(function(result) {console.log(result)})

    2. Promises are substitue to callbacks in JS. Promises are better boz u don't expose your functionality.

    function doSomething(){
    return new Promise((resolve, reject) => {
    setTimeout(() => {
        console.log('Do Something')
        resolve("success")
    }, 5000)
    })	
    }

    doSomething().then( function(data){
	    console.log(data)
        })



    New JS features
    http://es6-features.org/   
        promises 

    Single Page Application
        Airline booking application
        Search, Selection, Flyer details, Payment
        Angular router is a separate module
            angular.module('yourApp', ['ngRoute', 'anotherApp'])
        Facilities of routing libraries
            - Navigation : Programmatic and Link based navigation to routes
            - Routes with Parameters
            - Nested Routes
            - Routes Guarded
    Providers
        Difference b/w Factories, Services and Providers
            - Providers can be configured once, data can be changed once --> module.config
            - Providers unlike (factories and services) can be configured or their values can be changed once and only with the config funtion
        Dependency Injection

    UI Router (third party routing API)

    Forms validations  
        ng-valid
        ng-invalid
        ng-dirty
        ng-pristine

        Never do DOM manipulation



