# beth-rest

Declaratively describe REST services with HTML to automatically generate JavaScript clients for those APIs.

## Example Usage

```html
<beth-rest base-url="/api">
  <beth-resource name="post"></beth-resource>
</beth-rest>
```

By default Beth auto-binds itself to the window for easy access from JavaScript. The above service could be used this way:

```javascript
Beth.post.create({
  title: 'My blog entry',
  body: 'lorem...'
}).then(function(post, err) {
  if (err) {
    // There was a problem.
  } else {
    // Everything happened okay, new Post's body is in `post` variable.
  }
});
```
