# pdf-lib



## 基础介绍

JavaScript PDF 操作库，支持 创建、修改、合并、加水印、表单填写 等功能，适用于 Node.js 和浏览器端



## 核心内容
```yaml
pdf-lib:
    PDFDocument: # pdf文档
        addPage():
        copyPages():
        create():
        embedFont():
        embedPng():
        getForm():
        getPages():
        load(): # 加载文档
        save(): # 获取文档字节数据
    PDFEmbeddedPage:
    PDFFont:
    PDFForm: # pdf表单
        getTextField():
    PDFImage:
    PDFPage: # pdf页面
        drawImage():
        drawText():
        setRotation():
    StandardFonts:
    rgb():
```