---
title: HTML5 Detect
tags: [HTML5]
---
以下是对 **HTML5** 新技术的一些检测方法
{% highlight javascript %}
function supports_canvas(){
    return !!document.createElement('canvas').getContect;
}

function supports_canvas_text(){
    if(!support_canvas())   {return false;}
    var dummy_canvas = document.createElement('canvas');
    car context = dummy_canvas.getContext('2d');
    return typeof context.fillTex t == 'function';
}

function supports_video(){
    return !!document.createElement('video').canPlayType;
}

function supports_local_storage(){
    try{
        return 'localStorage' in window && window['localStorage'] !== null;
    }   catch(e){
        return false;
    }
}

function supports_web_workers(){
    return !!window.Workwer;
}

fuction supports_offline(){
    return !!window.applicationCache;
}

function supports_geolocation(){
    return 'geolocation' in navigator;
}

function supports_input_types(){
    var i = document.createElement("input");
    // the default type is "text"
    i.setAttribute("type", "search");
    // search number range color tel url email date month week time datetime datetime-local
    return i.type !== "text";
    // if the browser doesn't support the type you set, it will still be "text" as default
}

function supports_input_placeholder(){
    var i = document.createElement('input');
    return 'placeholder' in i;
}

function supports_input_autofocus(){
    var i = document.createElement('input');
    return 'autofocus' in i;
}

function supports_microdate_api(){
    return !!document.getItems;
}

function supports_history_api(){
    return !!(window.history && history.pushState);
}

{% endhighlight %}
