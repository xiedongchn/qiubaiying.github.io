**Regex**

Use `Regex` to `find/replace` string.

```regu
#regex below means replace "` *," with ";"
(` )(.*)(,) = (` .*,)
#old string
`id` varchar(64) default not null,
#result-1
`id;
#regex below means replace "`" with "private String "
(`)
#final result
private String id;
```

