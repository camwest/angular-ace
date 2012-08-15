# angular-ace

A directive for ace code editor

## Purpose & Rationale

* Use ace code editor as if it was a textarea
* Make sure forms still submit properly with the right data
* Only submit / bind to scope when the syntax is correct

## Installation

* require ace (https://github.com/ajaxorg/ace/)
* require angular (tested on 1.0.1)
* also requires jquery 1.7.2+ (for now)

## Usage

<!doctype html>
<html ng-app="myapp">
  <head>
    <script src="http://code.angularjs.org/1.0.1/angular-1.0.1.js"></script>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.7.2/jquery.min.js"></script>
    <script src="/ace.js"></script>
    <script src="/angular-ace.js"></script>  
    
    <script>
      angular.module('myapp', ['ace']);
    </script>

    <style type='text/css'>
      /* MUST HAVE WIDTH/HEIGHT */
      .ace-editor {
        width:500px;
        height:500px;
      }

      #contents {
        width:500px;
        height:500px;
        position:absolute;
        left:500px;
        top:0;
      }
    </style>
  </head>
  <body>

    <div ace="json" ng-model="bitchin">
      <textarea name="tutorial[contents]"></textarea>
    </div>

    <div id="contents">
      Value: {{ bitchin }}
    </div>

  </body>
</html>


## Copyright

Copyright (c) 2012 Cameron Westland. See LICENSE.txt for further details.
