# JapanMountain Data

[日本の主な山岳一覧(国土地理院ウェブサイト)](https://www.gsi.go.jp/kihonjohochousa/kihonjohochousa41140.html)

このデータは以下の URL 内の table では日本国内の多くの山を網羅しているようなので、これを json としてデータ起こししました。何かの役に立つかもしれないので、このまま公開しておきます。

このリポジトリには以下のデータファイルが含まれています。

- JapanMountain.json
- JapanMountain.csv

## License

[CC Licenses](https://creativecommons.org/licenses/by/4.0/legalcode.ja)
[CC Licenses (日本語)](https://creativecommons.org/publicdomain/zero/1.0/deed.ja)

参考: [国土地理院コンテンツ利用規約](https://www.gsi.go.jp/kikakuchousei/kikakuchousei40182.html)


## Json

### header

version: json データのバージョン

後述のメンテナンス方針を参照

### data 配列

- name: 主な名称
- kana: 主な名称の読み仮名
- lat: 緯度
- lng: 経度
- nameMap: 主な名称とその他の名称の配列
- altitude: 標高
- area: 山地、島名など大まかな地域
- prefectures: 都道府県の配列
- triangulationStationName: 三角点名
- gisMapUrl: 国土地理院地図への URL
- cordillera?: 山系が提供されている場合は設定される
- shortname?: 主な名称の他に短い名前が提供されている場合は設定される

## CSV

Json ファイルから一部の平坦にできるデータのみを出力したものです。

- 名前
- かな
- 緯度
- 経度
- 標高

## メンテナンス方針


### データ

- 地勢変更など(地震、噴火など)で情報に変化があった場合は追従する。
- Unicode (utf-8) を使う。
- **明白な誤字、間違いも修正しない。**
- 消し忘れと思われる記号文字は消去する。
- 文字化け対策と見られる画像文字は該当する unicode 文字に変更する。
- json のフィールドの意味を変更することはしない。意味を変更する場合は新規に列を追加する。
- csv は option なので列の追加はありえる。
- *unicode に該当する文字がない場合の対応は未定。*

### Version

一通りデータやデータ構造の検証が終わった後で 1.0.0 として公開します。

- 軽微なデータの修正をした場合は Revision 番号を up します。
- Upstream の軽微な修正も反映した後で Revision を up します。
- データ形式に小さな変更(フィールド追加など)があった場合に Minor 番号を up します。
- データ形式に大きな変更(データ構造の変更、フィールド削除)があった場合は Major 番号を up します。
- Upstream のデータ構造に変更があった場合もフィールド互換性はできるだけ維持する。