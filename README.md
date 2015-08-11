# E.vents
Small library to organize &amp; manage DOM events

Requirements:
 - Jquery (Any version!)

Usage:

```javascript
   E(<parentSelector || null>).vents({
       '<event1> <selector1>': <function1 to trigger>,
       '<event2> <selector2>': <function2 to trigger>
   });
   
   // This is the same as:
   $(<parentSelector>).find(<selector1>).on(<event1>,<function1 to trigger>);
   $(<parentSelector>).find(<selector2>).on(<event2>,<function2 to trigger>);
   
   // If parentSelector is "null", the selector by default is "body":
   E.vents({                //Yes! E.vents === E().vents === E().events    !!!!!
       '<event1> <selector1>': <function1 to trigger>,
       '<event2> <selector2>': <function2 to trigger>
   })
   
   // Is the same as:
   $(<selector1>).on(<event1>,<function1 to trigger>);
   $(<selector2>).on(<event2>,<function2 to trigger>);

```


Simple example:

```HTML
<html>
<head>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/2.1.3/jquery.min.js"></script>
    <script src="e.vents.js"></script>
    <script type="text/javascript">
        $(document).ready(function start(){
           E.vents({
               'click #first': function() {
                   alert("You clicked the first button!");
               },
               'click #second': function() {
                   alert("You clicked the second button!");
               }
           });
        });
    </script>
</head>
<body>
    <button id="first">First button!</button>
    <br/>
    <button id="second">Second button!</button>
</body>
</html>
```
