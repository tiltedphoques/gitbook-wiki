---
description: In case compilation goes wrong.
---

# Troubleshooting

## xmake errors:

If you encounter the following error:

![](https://i.imgur.com/69IJuIY.png)

you most likely didn't point xmake to vcpkg. This can be fixed by installing it and then running&#x20;

```
xmake g --vcpkg="location"
```

