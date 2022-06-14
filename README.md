# Zola

No feed file generated in multilingual sites reproduce exmaple.


```bash
zola build
```

You will see `public/categories/random/atom.xml`, but not for `public/zh/categories/random/atom.xml`.


[Issue track](https://github.com/getzola/zola/issues/1896)

Related config:

```toml
generate_feed = true
taxonomies = [
  # You can enable/disable RSS
  {name = "categories", feed = true},
  {name = "tags", feed = true},
]
theme = "after-dark"
[languages.zh]
taxonomies = [
  # You can enable/disable RSS
  {name = "categories", feed = true},
  {name = "tags", feed = true},
]
```