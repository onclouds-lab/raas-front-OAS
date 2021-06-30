# coordinate-system

![図](../assets/images/IMG_20210628_143358.jpg)

## 座標系一覧
name | unit | 主な用途
---------|----------|---------
 Facility | m | 全体の俯瞰
 Image | pixel | クライアント上の描画
 Floor | m | ロボットの自己位置推定

## 単位系変換
\ | Facility  | Image |Floor
---------|----------|---------|-----
 Facility | \ | **要確認**|無変換
 Image |**要確認** |\ | `/resolution`|
 Floor|無変換|`*resolution`|\
  
 ## 原点変換
 \ | Facility  | Image |Floor
---------|----------|---------|-----
 Facility | \ | - `image origin offse`|-`origin (in YAML)`-`image origin offset`
 Image |+`image origin offset` |\ | -`origin (in YAML)`|
 Floor|+`origin (in YAML)`+ `image origin offset`|+`origin (in YAML)`|\