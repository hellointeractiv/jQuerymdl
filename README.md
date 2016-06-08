# mdl
Flexible modal, confirm &amp; prompt jquery plugin.
Demo : http://hello-interactiv.com/utils/mdl/index.html

## Install 
```html
<link rel="stylesheet" href="dist/mdl.css" >
<script src="demo/libs/jquery.min.js"></script>
<script src="dist/mdl-min.js"></script>
```

## Config by js
```html
<a class="mdl-btn" id="bt1" data-target="#modal1" >
modal by js
</a>
```

```javascript
$('#bt1').mdl({
	type: 'modal',
	fullscreen:false,
	overlayClick:true
});
```

##Config by datas
```html
<a class="mdl-btn btns-modal" data-type="modal" data-target="#modal2" data-fullscreen="true" data-overlayClick="true" >
modal by datas
</a>
```

```javascript
$('.btns-modal').mdl(this);
```



## Confirm
```html
<a class="mdl-btn btns-confirm" data-type="confirm" data-fullscreen="false" data-overlayClick="true" >
confirm
</a>
```

```javascript
$('.btns-confirm').mdl({
	type:'confirm',
	fullscreen:false,
	overlayClick:false,
	content:"Êtes vous sûr de vouloir supprimer toutes vos données?"
}, function(result){
	alert("result:" + result);
});
```


## Prompt
```html
			
<a class="mdl-btn btns-prompt" data-type="prompt" data-fullscreen="false" data-overlayClick="true" >
Prompt
</a>
```

```javascript
$('.btns-prompt').mdl({
	type:'prompt',
	overlayClick:false,
	content:"what is the color of the white horse?"
}, function(result){
	alert("result:" + result);
});

```



##Open &  close manually
```javascript
mdl_open('#modal1');
			
setTimeout(function(){ 
	mdl_close('#modal1');
}, 2400);		
```
