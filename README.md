# Angular-2-webpack
Version of Angular 2 webpack I use to deploy Angular dist contents to a subfolder on a Windows server running .Net/IIS.  
  
This is based off of the code available in Angular's [webpack guide](https://angular.io/guide/webpack). It has been modified for the purpose of deploying content of dist folder to a subfolder on a Windows server.  
  
There are 3 locations in the code where your server folder needs to be updated. A webpack plugin was used to rewrite <base href> on prod build so that it matches your server folder location. One of the 3 locations is in src/Web.config, a file that should be included in the subfolder on server where you deploy to in order to override .Net routing and IIS 404 redirect so that Angular routing can work properly.  
  