# Schedify 課表選課系統（Django）

## 專案結構
```
config/        專案設定（settings、urls、wsgi、asgi）
pages/         主要應用程式（models、views、urls、templates、static、fixtures）
manage.py
pyproject.toml / uv.lock / .python-version
db.sqlite3     執行 migrate 後產生
```

## 執行方式（需要先安裝 uv）
```
uv sync
uv run python manage.py makemigrations pages
uv run python manage.py migrate
uv run python manage.py loaddata courses
uv run python manage.py runserver
```
打開 http://127.0.0.1:8000/ 。第一次用某個學號登入會自動建立帳號，並請你填寫姓名。

管理後台：`uv run python manage.py createsuperuser`，之後到 /admin/。
