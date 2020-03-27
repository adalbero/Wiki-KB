---
title: MongoDB Tools
description: Tricks & Tips
published: true
date: 2020-03-27T13:48:09.018Z
tags: 
---

# Import CSV, TSV or JSON

```shell
mongoimport --type csv -d test -c products --headerline --drop products.csv
```

- `-type` - import format. Can be: `csv`, `json`, `tsv`
- `-d` - database
- `-c` - collection
- `-headerline` - first row represent field names


