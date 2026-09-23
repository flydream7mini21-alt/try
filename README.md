# chome

Django で作成したチャット・グループ管理アプリです。

## セットアップ

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
Copy-Item .env.example .env
cd chome_project
python manage.py migrate
python manage.py runserver
```

`DJANGO_SECRET_KEY`、`DJANGO_ALLOWED_HOSTS`、メール設定は環境変数で指定してください。`.env` は Git に追加しないでください。

## テスト

```powershell
cd chome_project
python manage.py test
```

## ディレクトリについて

- `chome_app/static/`: Git で管理する静的ファイル
- `chome_project/media/`: ユーザーがアップロードするファイル（Git 管理外）
- `chome_project/db.sqlite3`: ローカル開発用データベース（Git 管理外）
