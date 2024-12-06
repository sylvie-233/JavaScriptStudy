# exceljs

## 基础介绍

excel操作库


## 核心内容
```yaml
exceljs:
    Cell:
        alignment:
        border:
        fill:
        value:
            formula: # 公式
            result:
    Row:
        eachCell():
    Workbook:
        xlsx:
            load():
            read():
            readFile():
            writeFile():
        addWorksheet(): # 添加sheet表
        getWorksheet():
    Worksheet:
        eachRow(): # 遍历行
        getCell():
        mergeCells():
```

