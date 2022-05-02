# Web-Skills(7)
![Shikamaru](https://github.com/whitebird1016/Web-Skills-with-Shikmamaru/blob/main/1_HTGSqvOc52yfMwyLhCMjVA.jpeg)
<h2>DOM Skills</h2>
<h3>1: Show all DOM borders</h3>

```
[].forEach.call($$("*"), dom => {
    dom.style.outline = "1px solid #" + (~~(Math.random() * (1 << 24))).toString(16);
});
```
<h3>2: Responsive pages</h3>

```
function AutoResponse(width = 750) {
    const target = document.documentElement;
    target.clientWidth >= 600
        ? (target.style.fontSize = "80px")
        : (target.style.fontSize = target.clientWidth / width * 100 + "px");
}
```
<h3>3: Filter XSS</h3>

```
function FilterXss(content) {
    let elem = document.createElement("div");
    elem.innerText = content;
    const result = elem.innerHTML;
    elem = null;
    return result;
}
```
<h3>4: Access (LocalStorage)</h3>

```
const love = JSON.parse(localStorage.getItem("love"));
localStorage.setItem("love", JSON.stringify("I Love You"));
```
