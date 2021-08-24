# FlowerShopProject
[サイトURL](https://syu-kuri.github.io/dotinstall_FlowerShopProject/)

## 概要
### 八重乃花(やえのはな)が作った資料
彼からももらった資料の内容は以下のとおりです。
- お花屋さんの名称
  - 「osumou flowers」
- お店の特徴
  1. 商品は価格帯ごとに3つだけ
  1. ただし、日替わりで内容が変わる
  1. このご時世なので完全キャッシュレス
- 商品のラインナップ
  - 「小結」：¥980
    - いちばんお求めやすい。日常に彩りを添えてくれるよう願いを込めた商品。
  - 「大関」：¥3,980
    - ちょっとした贈りものに。高すぎず安すぎず、ちょうどよい価格帯の商品。
  - 「横綱」：¥9,800
    - 特別な日に。
- ロゴ画像
  - [osumou-flowers.zip](https://github.com/256times/FlowerShopProject-202108/files/6999044/osumou-flowers.zip)をご利用ください。
- URL
  - osumou-flowers.dotinstall.com （架空のURLです。サイト内でURLを表記する場合にお使いください）
- 電話番号
  - 03-xxxx-xxxx
- 住所
  - 東京都目黒区東山x-x-x
- 営業時間/定休日
  - 11:00-20:00 （月曜休）
 
### 追加情報
- 元横綱の年齢: 42歳
- ファン層: まんべんなくですが、高齢の方も（日本の人口比がそうですからね・・・）多い
- 商品価格は税込
- 八重乃花の好きな花: 「日本的な花」としての蓮、梅、桜等あたりの多弁花
- 注文方法: 店頭での販売・注文のみ（電話では営業時間その他のお問い合わせ対応のみ）
  - 電話注文、配送、返品はやっていない
- 開店日: 8月1日にプレオープンしている

### 制作に関する要件
今回の要件については以下のとおりです。
- HTML/CSS（余裕があればJavaScript）を使った「osumou flowers」のウェブサイト。
- スマホからのアクセスが多いことが想定されるのでレスポンシブに対応させてください。
- 1ページ以上作ってください（1ページだけでも構いません）。
- GitHub Pagesにて公開してください。
- 上記のロゴ画像を使ってください。
- 画像が必要な場合、ダミー画像、もしくはライセンスフリーの素材を使用してください。ご自身で作成して頂いても構いません。
- サイトに掲載する文章は決まっていません。適当なダミーテキスト使って頂いても構いませんし、ご自身で考えてしまっても良いです。
- その他、良い案があれば自由に盛り込んでいただいてOKです。


## レイアウトの決め方
dotinstallのコミュニティFlowerShopProjectの参加者が使っているもの
- [Pinterest](https://www.pinterest.jp/)
- [3色だけでセンスのいい色という本](https://book.impress.co.jp/books/1119101155)
- [縦長のwebデザインギャラリー・サイトリンク集｜MUUUUU.ORG](https://muuuuu.org/)
- [Webデザイン制作の参考になる国内のステキなサイト集](https://sankoudesign.com/)
- [動くWebデザイン　アイディア帳](https://coco-factory.jp/ugokuweb/)
- [LPアーカイブ](https://rdlp.jp/lp-archive)

## filter: drop-shadowが重なり順に影響する理由
`filter`で`none`以外を指定すると、スタッキングコンテクストが生成されるため、画像が上にきてしまう。
スタッキングコンテクストはやや難しいが、[MDN](https://developer.mozilla.org/ja/docs/Web/CSS/CSS_Positioning/Understanding_z_index/The_stacking_context)で仕様を確認できる。
したがって、さらにそのうえに`overlay`を重ねるには、[`z-index`](https://ics.media/entry/200609/)を追加して、さらにスタッキングコンテクストを作らないといけない、という仕組み。
というわけで、`filter`を使うとこうなる、という仕様だと理解しておくと良さそう！
