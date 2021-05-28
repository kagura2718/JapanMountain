# JapanMountain Data

このデータは以下の URL 内の table では国内の多くの山を網羅しているようなので、これを json としてデータ起こししました。何かの役に立つかもしれないので、このまま公開しておきます。

[日本の主な山岳一覧(国土地理院ウェブサイト)](https://www.gsi.go.jp/kihonjohochousa/kihonjohochousa41140.html)

以下のデータファイルが含まれています。

- JapanMountain.json
- JapanMountain.csv

## データメンテナンス方針

- 地勢変更など(地震、噴火など)で情報に変化があった場合は追従する。
- **明白な誤字、間違いも修正しない。**
- Unicode (utf-8) を使う。
- 消し忘れと思われる記号文字は消去する。
- 文字化け対策と見られる画像文字は該当する unicode 文字に変更する。
- json の項目の意味を変更することはしない。意味を変更する場合は新規に列を追加する。
- csv は option なので列の追加はありえる。
- *unicode に該当する文字がない場合の対応は未定。*

## Json

name: 主な名称
kana: 主な名称の読み仮名
lat: 緯度
lng: 経度
nameMap: 主な名称とその他の名称の配列
altitude: 標高
area: 山地、島名など大まかな地域
prefectures: 都道府県の配列
triangulationStationName: 三角点名
gisMapUrl: 国土地理院地図への URL

cordillera?: 山系が提供されている場合は設定される
shortname?: 主な名称の他に短い名前が提供されている場合は設定される

## CSV

Json ファイルから一部の平坦にできるデータのみを出力したものです。

- 名前
- かな
- 緯度
- 経度
- 標高


## License

[CC Licenses](https://creativecommons.org/licenses/by/4.0/legalcode.ja)
[CC Licenses (日本語)](https://creativecommons.org/publicdomain/zero/1.0/deed.ja)

参考: [国土地理院コンテンツ利用規約](https://www.gsi.go.jp/kikakuchousei/kikakuchousei40182.html)


