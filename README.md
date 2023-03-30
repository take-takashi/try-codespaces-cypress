# try-codespaces-cypress
Codespaces+Cypressに挑戦

## 参考URL
- https://devopstar.com/2022/01/03/cypress-testing-in-devcontainers-and-github-codespaces/

## ポイント
- .devcontainerのDockerfileとdocker-composeが重要

## setup for test
```sh
mkdir test
cd test
npm init
npm i -D cypress
```

## setup for astro
```sh
mkdir app
cd app
npm create astro@latest . -- --template blog --install --no-git --typescript strict -y
```

### Try cypress
1. `http://127.0.0.1:8080`にブラウザでアクセス（ちなみにSafariでアクセスするとめっちゃ変な挙動する）
1. 表示画面でパスワードを入力してContinueを押下（パスワードは`.devcontainer/docker-compose.yml`内で定義）
1. ターミナルで`cypress open`すると、`http://127.0.0.1:8080`の画面がCypressの画面になる
1. `electron`を選択してスタート？
1. `test/cypress/e2e/1-getting-started/try.cy.js`のようなファイルを作成してテストができるようになる