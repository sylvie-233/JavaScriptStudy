# @elastic

## 基础介绍

javascript 操作 Elasticsearch库


## 核心内容
```yaml
@elastic/elasticsearch:
    Client:
        auth:
        node:
        ---
        indices: # 索引
            create():
                index:
                mappings:
                    properties:
                        fields:
                            keyword:
                        type:
                            integer:
                            text:
            exists():
        bulk():
        delete():
        get():
        index():
            document:
            index:
        search():
            aggs:
                max:
                    field:
                terms:
                    field:
            body:
                query:
            index:
            query:
                bool:
                    filter:
                    must:
                    must_not:
                    should:
                        match:
                match:
                match_all:
                term:
```
