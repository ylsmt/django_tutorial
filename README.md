# django_tutorial
教程地址：https://www.djangoproject.com/start/

目录结构
```
├── django-polls
│   ├── dist
│   ├── django_polls.egg-info
│   ├── docs
│   ├── LICENSE
│   ├── MANIFEST.in
│   ├── polls
│   ├── README.rst
│   └── setup.py
├── manage.py
├── mysite
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
└── requirements.txt
```

polls:
```
├── admin.py
├── apps.py
├── __init__.py
├── migrations
│   ├── 0001_initial.py
│   └── __init__.py
├── models.py
├── static
│   └── polls
│       ├── images
│       └── style.css
├── templates
│   └── polls
│       ├── detail.html
│       ├── index.html
│       └── results.html
├── tests.py
├── urls.py
└── views.py
```
* [URL配置](#URL配置)
    * mysite/settings.py:
        * ```url(r'^polls/', include('polls.urls')),```
    * polls/urls.py:
        * ```url(r'^$', views.index, name='index'),```
        *  设置命名空间:
            ```app_name = 'polls'```
* [视图](#视图)
    * polls/views.py
    * 通用视图:
* [模型](#模型)
* [安装问题](#问题)
  - 找不到virtualenv 命令
     ``` 
     /usr/local/python3/bin/virtualenv django 
     ```
  * sqlite导入错误   安装sqlite3后重新编译
      ```
      yum install sqlite-devel -y
      cd Python-3.5.0
      ./configure --prefix=/usr/local/python3
      make && make install
      ```
