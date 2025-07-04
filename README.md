# 光照射エネルギー計算ツール

## 概要

このツールは、光照射に関する各種パラメータを簡単に計算できるWebアプリケーションです。レーザー治療、光線療法、研究実験などで必要となる照射時間、エネルギー密度、光強度などを素早く算出できます。

## 主な機能

### 1. 照射時間計算
目標とするエネルギー量を得るために必要な照射時間を計算します。
- 計算式：照射時間（秒）= 目標エネルギー（J）÷ 光出力（W）

### 2. 基本エネルギー計算
光出力と照射時間から総エネルギー量を算出します。
- 計算式：エネルギー（J）= 光出力（W）× 照射時間（秒）

### 3. 光強度 (Irradiance) 計算
照射面積あたりの光出力を計算します。
- 計算式：光強度（W/cm²）= 光出力（W）÷ 照射面積（cm²）

### 4. エネルギー密度 (Fluence) 計算
単位面積あたりのエネルギー量を計算します。
- 計算式：エネルギー密度（J/cm²）= 総エネルギー（J）÷ 照射面積（cm²）

### 5. 距離による光強度減衰計算
逆二乗の法則に基づいて、距離変化による光強度の変化を算出します。
- 計算式：新しい強度 = 元の強度 ×（元の距離 ÷ 新しい距離）²

### 6. パルスレーザー計算（V2.0新機能）
パルスレーザーのパラメータを計算します。
- パルスエネルギー、平均出力、ピーク出力などの相互変換

### 7. 光子エネルギー計算（V2.0新機能）
波長から光子1個あたりのエネルギーを計算します。
- 計算式：E = hc / λ
- h: プランク定数、c: 光速、λ: 波長

## 新機能（V2.0）

- **ダークモード対応**: 目に優しい暗い配色への切り替えが可能
- **パルスレーザー計算**: 研究や医療で使用されるパルスレーザーのパラメータ計算
- **光子エネルギー計算**: 波長から光子エネルギーを算出
- **改善されたUI**: より直感的で使いやすいインターフェース

## 使用方法

1. ブラウザでHTMLファイルを開きます
2. 各計算セクションで必要な数値を入力します
3. 自動的に計算結果が表示されます
4. 右上のトグルボタンでダークモードに切り替え可能

## 注意事項

- **光出力について**: 消費電力ではなく、実際の光出力（放射束）を入力してください
- **照射径**: 光が実際に照射される部分の直径を正確に測定してください
- **安全性**: 医療用レーザーや高出力光源を使用する場合は、必ず安全基準を確認し、適切な保護具を着用してください
- **距離の影響**: 光源からの距離が2倍になると、照射面積は4倍、光強度は1/4になることに注意してください

## 想定される用途

- 歯科用レーザー治療のパラメータ設定
- 光線力学療法（PDT）の照射条件計算
- 研究実験での光照射条件の決定
- 光硬化型材料の硬化時間算出
- UV殺菌装置の照射時間計算
- パルスレーザーを用いた精密加工の条件設定

## 技術仕様

- 純粋なHTML/CSS/JavaScriptで実装
- 外部ライブラリ不要
- レスポンシブデザイン対応
- リアルタイム計算機能
- ダークモード対応

## ライセンス

MIT License

Copyright (c) 2025 Fumihiko Yoshino

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

## 作成者

吉野文彦（Fumihiko Yoshino）

## 更新履歴

- **V2.0** (2025年7月4日): ダークモード追加、パルスレーザー計算機能、光子エネルギー計算機能を実装
- **V1.0** (2025年7月4日): 初版リリース

## バージョン別アクセス

- [最新版 (V2.0)](https://vermilionheart.github.io/light-energy-calculator/light_calculator_V2.0.html)
- [V1.0](https://vermilionheart.github.io/light-energy-calculator/light_calculator_V1.0.html)
