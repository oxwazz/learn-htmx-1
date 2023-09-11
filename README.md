# learn-htmx-1

version htmx.org@1.9.5

## AJAX requests - [docs](https://htmx.org/docs/#ajax)
```
- hx-get
- hx-post
- hx-patch
- hx-put
- hx-delete
```
### ✅ hx-get
```html
<div hx-get="https://jsonplaceholder.typicode.com/todos/1">
  Get Todo (click me)
</div>
```
### ✅ hx-post
```html
<div hx-post="https://jsonplaceholder.typicode.com/todos">
  Create Todo (click me)
</div>
```
### ✅ hx-patch
```html
<div hx-patch="https://jsonplaceholder.typicode.com/todos/1">
  Edit Patch Todo (click me)
</div>
```
### ✅ hx-put
```html
<div hx-put="https://jsonplaceholder.typicode.com/todos/1">
  Edit Put Todo (click me)
</div>
```
### ✅ hx-delete
```html
<div hx-delete="https://jsonplaceholder.typicode.com/todos/1">
  Delete Todo (click me)
</div>
```

## Triggering Requests - [docs](https://htmx.org/docs/#triggers)
```
Standard Events =>
  - click (triggered on click)
  - change (triggered on blur)
  - etc

Standard Event Filters =>
  - <event>[<event filter>] (triggered when event filter is true, e.g. click[altKey])

Standard Event Modifiers =>
  - once (only trigger once)
  - changed (trigger only if value has changed)
  - delay:<timing declaration> (triggered after delay, e.g. delay:1s)
  - throttle:<timing declaration> (triggered at most once per timing declaration, e.g. throttle:1s)
```

### ✅ once
```html
<div
  hx-get="https://jsonplaceholder.typicode.com/todos/1"
  hx-trigger="click once"
>
  Trigger me (click, run only once)
</div>
```

### ✅ changed
```html
<input
  type="text"
  name="q"
  hx-get="https://jsonplaceholder.typicode.com/todos/1"
  hx-trigger="keyup changed delay:500ms"
  hx-target="#search-results"
/>
<div id="search-results">result</div>
<!-- we use changed modifier because we only trigger when value has change, not arrow-up, esc, shift, etc -->
```

### ✅ delay
```html
<input
  type="text"
  name="q"
  hx-get="https://jsonplaceholder.typicode.com/todos/1"
  hx-trigger="keyup changed delay:500ms"
  hx-target="#search-results"
/>
<div id="search-results">result</div>
```

### ✅ throttle
```html
<input
  type="text"
  name="q"
  hx-get="https://jsonplaceholder.typicode.com/todos/1"
  hx-trigger="keyup changed throttle:500ms"
  hx-target="#search-results"
/>
<div id="search-results">result</div>
<!-- throttle input every 500ms  -->
```






✅
☑️
❓
