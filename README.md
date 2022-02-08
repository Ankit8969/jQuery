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

# Manipulating the DOM in jQuery


















