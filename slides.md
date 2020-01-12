class: middle, center

<img src="./assets/deno_logo_3.svg" align="center" width="300" />

# `https://git.io/*.ts`

---
class: middle

ある日 CI で書いたコード

```
perl -p -e "s/\n/%0A/" |
sed -e "s/^/\#\#\[set-output name=description;\]/"
```

---
class: middle

あるコマンドの出力を GitHub Action の step のアウトプットに設定するシェル

```
perl -p -e "s/\n/%0A/" |
sed -e "s/^/\#\#\[set-output name=description;\]/"
```
---
class: middle, center, inverse

2020年に書くコードでは無い
---
class: middle

よく使う処理なので, シュッとしたい
```
perl -p -e "s/\n/%0A/" |
sed -e "s/^/\#\#\[set-output name=description;\]/"
```

---
class: middle

シュ!
```
deno https://git.io/set-output.ts
```

---
class: middle, center

[実際に使った例](https://gist.github.com/kt3k/8945d7205c5b739db616a3142ec33176)

---
class: middle, center

git.io について

---
# git.io

- github が運営している url shortner
- github 上のリソースに対してのみ使える
- curl コマンドで, 好きな URL を取れる
```
curl https://git.io/ -i \
  -F "url=https://github.com/YOUR_GITHUB_URL" \
  -F "code=YOUR_CUSTOM_NAME"
```

---
class: middle, center
`http://git.io/*.ts` を Deno script のエントリポイントにマップすると短い名前のスクリプトみたいになる.

---
class: middle, center
`http://git.io/*.ts` 全然とられていないので, 取り放題!

deno.land/x/ に出すのが気がひけるような物とか・・・ x-mas.ts とか・・・

---
class: middle, center

以上
