# My Zenn Articles

## Migration from Qiita

```bash
go install github.com/ikawaha/zenn-importer@latest
gh repo create myzenn --public -y
cd myzenn
npm init --yes
npm install zenn-cli
npx zenn init
git add .gitignore
git add .
git commit -m 'init'
zenn-importer qiita -user eggplants -publish -verbose -dir articles
git add articles/* img/
git commit -m 'add: migrate from qiita'
git push --set-upstream origin master ||
git push --set-upstream origin main
```

## Preview

```bash
xdg-open http://localhost:8000
npx zenn preview
```

## Connect gh repo with Zenn

See: <https://zenn.dev/zenn/articles/connect-to-github<
