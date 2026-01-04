# 1
## Chap1
### 🍊mise他のインストール
* `mise`
  * 他ツールと違って環境変数 PATH 自体を動的に書き換えることでバージョン管理する。
  * 複数言語のバージョン管理が可能
* `shims` … ラッパー。これで動的切り替えを実現。`.mise.toml`の存在チェックをしている
```bash
# Install
mise use -g node

# shimsの設定
echo 'eval "$(mise activate bash)"' >> ~/.bashrc
source ~/.bashrc

# Check
node --version
> v25.2.1
```

### 📝Windowsの改行が混じっていて「npm install」に失敗
* `dot2unix`で解決
```bash
sudo apt install -y dos2unix
```

### 「vite」を使ってプロジェクトを作る
* Vue.jsと同じ作者 Evan You によるツール
* vueはviewのフランス語
* viteもフランス語、速い（quick）という意味
```bash
# プロジェクト作成コマンド
npm create vite@latest hello-world -- --template=react-ts
# ホームディレクトリで起動
npm run dev
```
* `package-lock.json` … インストールしたパッケージの依存情報を保存しておくためのロックファイル。

### プロジェクト初期値
* `document.getElementById('root')`が、`index.html`の中の