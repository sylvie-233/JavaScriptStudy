# exceljs

## 基础介绍

excel操作库（支持Node.js、浏览器）


## 核心内容
```yaml
exceljs:
    Cell:
        alignment:
        border:
        fill:
        style: # 样式
        text: # 字符串值
        type:
        value:
            formula: # 公式
            result:
    Column:
        header:
        hidden:
        values:
        eachCell():
    Row:
        values:
        eachCell():
    Workbook:
        calcProperties:
        created: # 创建时间
        creator: # 作者
        lastModifiedBy:
        lastPrinted:
        modified: # 修改时间
        properties:
        views: # 工作簿视图
        xlsx:
            load(): # 加载工作簿
            read():
            readFile():
            writeFile(): # 写出文件
        addWorksheet(): # 添加sheet表（创建）
            headerFooter:
            pageSetup:
                fitToPage:
                paperSize:
            properties:
                tabColor:
            views:
                showGridLines:
                state:
                    frozen:
                xSplit:
        eachSheet(): # 遍历所有工作表
        getWorksheet():
        removeWorksheet(): # 删除工作表（根据id）
    Worksheet:
        autoFilter: # 自动筛选器
        columns: # 列定义
        id: # id主键
        pageSetup: # 页面设置
            printArea:
        state: # 工作表状态
            hidden:
            visible:
        addRow(): # 添加行
        addRows():
        eachRow(): # 遍历行
        getCell():
            text:
        getColumn(): # 获取列
        getRow():
            values:
        insertRow():
        insertRows():
        mergeCells(): # 合并单元格
```

### 工作簿




### 工作表






### 单元格





### 样式



