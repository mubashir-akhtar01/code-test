1) authenticatedUser can be access from Auth::user()
2) all the users should be differentiate on behalf of roles and every roles have their permissions
3) no need to assign user_type into env file(it can be implement by RBAC) and we also cannot access env variables directly into controllers it can access throug config/app.php commonly. I have used it as enums which will be a php class and every constants and enums define there.
4) it will be good practice to use JSONResource response for APIs.
5) in Store functions, validations should be defined in StoreRequest file, no need to check every variables in controllers or repository class.
6) default values should be defined in DB if no variables found in request then DB automatically assign the default values.
7) for whereIn queries we can check the param and it should be an array and lenght of the array will be greater then 0 
8) attribute casting should be written in model class by using(setVariablenameAttriute) rather than to use it in controllers or repositories
9) to check form request contains only particular value then use $request->safe()->only(['val1', 'val2']) in  store/update form request ;
10) dont understand why the code didn't use proper implementation of Laravel Queue Jobs


upto so far i realised that some of the code logic is very messy not follows the good practices, and I am unable to read and understand all the code line by line to identify all of the issues just for my code test. some of the issue i have highlighted are mentioned-above.