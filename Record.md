# Record

```javascript
##  二叉树的最大深度

function TreeNode(val, left, right) {
  this.val = (val === undefined ? 0 : val)
  this.left = (left === undefined ? null : left)
  this.right = (right === undefined ? null : right)
}

var maxDepth = function(root) {
  if (!root) return null;
  let ret = 1;
  function dfs(root, depth) {
    if (!root.left && !root.right) ret = Math.max(ret, depth);
    if (root.left) dfs(root.left, depth + 1)
    if (root.right) dfs(root.right, depth + 1)
  }
  dfs(root, 1)
  return ret;
}
```

