编辑/data/seafile/seafile-data/seafile/conf/seahub_settings.py添加如下:
```
ENABLE_ONLYOFFICE = True
VERIFY_ONLYOFFICE_CERTIFICATE = False
# 调用onlyoffice接口地址
ONLYOFFICE_APIJS_URL = 'http://10.106.52.43/web-apps/apps/api/documents/api.js'
ONLYOFFICE_FILE_EXTENSION = ('doc', 'docx', 'ppt', 'pptx', 'xls', 'xlsx', 'odt', 'fodt', 'odp', 'fodp', 'ods', 'fods')
ONLYOFFICE_EDIT_FILE_EXTENSION = ('docx', 'pptx', 'xlsx','doc','xls','ppt')
```

页面设置:
![pdnsettings](https://github.com/charnet1019/docker-compose/blob/master/seafile/img/settings.png)


# 在线文档编辑依赖于onlyoffice，需要单独安装
