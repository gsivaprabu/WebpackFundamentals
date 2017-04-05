# Introduction - The Need for a Build

#### Why Do We Need a Build?

- Combining Files
- Minifying Files
- Maintaining File Order
- Transpilation
- Linting
- Web Application large and larger
- Security
- Multiple web Request
- css,images,fonts loaded every time.
- 100 to 2000  js file means u need 100 to 2000 requests
- Reduce the request

#### Code Size

Normal Code
```javascript
function rockOut(guitar) {
if(guitar.canShred) {
guitar.shred();
} else {
guitar.play();
}
}
```

After Minified
```javascript
function rockOut(guitar){if(guitar.canShred){guitar.shred();}else{guitar.play();}}
```

Really Minified
```javascript
function rockOut(c){c.canShred?c.shred():c.play()}
```

### File Order Dependencies

```html
<head>
<script src=“members.js”></script>
<script src=“bands.js”></script>
</head>
```
- Using any frameworks.
- Angular re-order files correctly.
- Module System

### Transpilation

- New featured languages converted to old supported languages
- Below cod use default parameter (**It supports only ECMASCRIPT-6**)
- Use transpiler convert to old
```javascript
function playSolo(drums, duration = 5) {
drums.startSolo();
setTimeout(function() {
drums.endSolo();
}, duration * 60000);
}
```

### Linting

**Debugging syntax errors()**

- Missing semicolon
- Keyboard parameter missing

```javascript
function tune(lead, bass, keyboard) {
lead.tune()
bass.tune()
}
```