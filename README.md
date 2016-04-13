# fbmessengerbot-test

## これはなに？

Facebook Messenger Bot をひとまず PHP on Heroku で動かしてみるキットです.
silex を使っています.

## 始め方

* Facebook App と Facebook Page を作成してください.
* Heroku アカウントを取得してください.
* 下の Deploy ボタンを押してデプロイします. 環境変数に適当な文字列を入れておきます(後で編集したり使ったりします).

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](http://bit.ly/fbmessengerbot-test-deploy)

* https://developers.facebook.com/docs/messenger-platform/quickstart を参考に、以下の手順を進めてください.
    * Facebook App に Messenger を利用する設定を追加し、Facebook Page の Access Token を取得 -> Heroku にデプロイしたアプリケーションの環境変数 FACEBOOK_PAGE_ACCESS_TOKEN に設定します.
    * Webhooks URL として、 <Heroku にデプロイしたURL>/callback を指定し、Verify Token にはデプロイ時に指定した FACEBOOK_PAGE_VERIFY_TOKEN を指定します. events として messages にチェックを入れ、Verify します.
    * Facebook 側の所定の URL に対して POST リクエストを送信し、Facebook Page に App を登録(Subscribe)します.
* Facebook メッセンジャーから Facebook Page に話しかけてみましょう.
* web/index.php を編集して Hack してみましょう. Enjoy!
