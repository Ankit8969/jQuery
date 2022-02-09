# jQuery


> All these property set the to the element hide or show
- $('div').hide();
- $('div').show();
- $('div').toogle();
- $(".green-box").fadeOut(2000);
-  $(".green-box").fadeIn(2000);
- $(".green-box").slideUp(2000);
- $(".green-box").slideDown(2000);

## Animation 
```
$(".green-box").animate(
    {
      "margin-left": "200px",
    },
    1000
  );
```
## You can add multiple styling like this
```
$(".blue-box").animate(
    {
      "margin-left": "150px",
      opacity: 0,
      height: "10px",
      "margin-top": "25px",
    },
    1000
  );
```
## You can add multiple effect
```
$(function () {
  $(".blue-box").animate(
    {
      "margin-left": "150px",
      opacity: 0,
      height: "10px",
      "margin-top": "25px",
    },
    1000
  );

  $("p").animate(
    {
      "letter-spacing": "3px",
    },
    2000
  );
});
```


## you can also write like this
```
$(function () {
  $(".blue-box").delay(1000).fadeTo(1000, 0.8).fadeOut(2000);
});

```
## you can also write like this
```
$(function () {
  $(".red-box").fadeOut(1000, function () {
    $(".green-box").fadeOut(1000);
  });
});

```

> You can also style the element using jQuery
```
$(function () {
  $("p").css("background-color", "red");
});
```

## Find in JQuery
```
$(function () {
  let list = $("#list").find("li");
  console.log(list);
});
```

## all these code work recursively 
```
$(function () {
  $("#list").find('li').css('background-color',"red");
  $("#list").children('li').css('background-color',"red");
  $("#list").parent("div").css("background-color", "red");
  $("#list").siblings("div").css("background-color", "red");
  
  // just prev
  $("#list").prev().css("background-color", "red");
  // just next
  $("#list").next().css("background-color", "red");
});
```


## automatically invoked the jquery function 
```
$(function(){


});
```

## Filter method in JQuery
```
$(function () {
  $("li")
    .filter((index) => {
      return index % 3 == 1;
    })
    .css("background-color", "red");
});

```

## Fast and Last Property
```
$(function () {
  $("li").first().css("color", "red");
  $("li").last().css("color", "blue");
});
```

# Method of getting the value

## .text() and .html()
```
$(function(){
  $("#btn1").click(function(){
    alert("Text: " + $("#test").text());
  });
  $("#btn2").click(function(){
    alert("HTML: " + $("#test").html());
  });
});
```

## geeting the value of any input box 
```
$(document).ready(function(){
  $("button").click(function(){
    alert("Value: " + $("#test").val());
  });
});
```

## geeting the value of attribute
```
$(document).ready(function(){
  $("button").click(function(){
    alert($("#w3s").attr("href"));
  });
});
```

# Method of setting the value

## text(), html() and val()
```
$(document).ready(function(){
  $("#btn1").click(function(){
    $("#test1").text("Hello world!");
  });
  $("#btn2").click(function(){
    $("#test2").html("<b>Hello world!</b>");
  });
  $("#btn3").click(function(){
    $("#test3").val("Dolly Duck");
  });
});
```

## Append method 
```
$(document).ready(function(){
  $("#btn1").click(function(){
    $("p").append(" <b>Appended text</b>.");
  });

  $("#btn2").click(function(){
    $("ol").append("<li>Appended item</li>");
  });
});
```

## prepand method
```
$(document).ready(function(){
  $("#btn1").click(function(){
    $("p").prepend("<b>Prepended text</b>. ");
  });
  $("#btn2").click(function(){
    $("ol").prepend("<li>Prepended item</li>");
  });
});
```

## another way to creating the item
```
function appendText() {
  var txt1 = "<p>Text.</p>";        // Create text with HTML
  var txt2 = $("<p></p>").text("Text.");  // Create text with jQuery
  var txt3 = document.createElement("p");
  txt3.innerHTML = "Text.";         // Create text with DOM
  $("body").append(txt1, txt2, txt3);   // Append new elements
}
```

## insertBefore and insertAfter
```
$("img").after("Some text after");

$("img").before("Some text before");
```


# Removing Property in jQuery

## removing and empty 
```
$("#div1").remove();
```
```
$("#div1").empty();
```

## addClass(), removeCLass(), toggleClass() and css()
```
$("button").click(function(){
  $("h1, h2, p").addClass("blue");
  $("div").addClass("important");
});
```
***IT add the two class***
```
$("#div1").addClass("important blue");
```
***Remove CLass***
```
$("h1, h2, p").removeClass("blue");
```

***Toggle FUnction***
```
 $("h1, h2, p").toggleClass("blue");
 ```
 
 ***Css() function ***
 ```
 $("p").css({"background-color": "yellow", "font-size": "200%"});
 ```
 
 ![img_jquerydim](https://user-images.githubusercontent.com/47697582/153184539-959bafe2-ad70-46c2-951b-7d72ffa63152.gif)

 # Traversing Up the DOM Tree
 
 > parent()
> parents()
> parentsUntil()
 
































































