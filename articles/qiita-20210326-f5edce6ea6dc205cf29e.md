---
title: "pipでeditable mode以外のパッケージを更新"
emoji: "😀"
type: "tech"
topics: [Python,Bash,pip]
published: true
---
`pip install -e`でインストールしたパッケージ以外を全更新

```bash:Terminal
pip list | awk 'NR>2&&$3==""{print$1}' | xargs pip install -U
```

