# 光研究関連計算ツール

## 概要

このツールは、光照射実験や研究で必要となる各種パラメータを簡単に計算できるWebアプリケーションです。特に、センサーで測定した総光出力（パワー）から、実際の光強度（Irradiance）や目標とするエネルギー密度（Fluence）を達成するための照射時間を、2つの簡単なステップで算出できるように設計されています。

## 主な機能

### 主要な計算ワークフロー

#### ステップ①：光強度 (Irradiance) の計算
センサーで測定した**総光出力（パワー）**と、光線ガイドの**直径**から、ガイド先端での光強度（単位面積あたりのパワー）を計算します。
- **計算式**: `光強度 (W/cm²) = 光出力 (W) / 照射面積 (cm²)`

#### ステップ②：必要照射時間の計算
ステップ①で求めた**光強度**と、目標とする**エネルギー密度（J/cm²）**から、必要な照射時間を計算します。
- **計算式**: `照射時間 (秒) = 目標エネルギー密度 (J/cm²) / 光強度 (W/cm²)`

---

### その他の計算ツール

#### 総エネルギー（ジュール）計算
光出力と照射時間から、照射される総エネルギー量を算出します。
- **計算式**: `エネルギー (J) = 光出力 (W) × 照射時間 (秒)`

#### 総エネルギーから照射時間を計算
目標とする総エネルギー量（J）と光出力（W）から、必要な照射時間を計算します。
- **計算式**: `照射時間 (秒) = 目標総エネルギー (J) / 光出力 (W)`

#### パルスレーザー計算
パルスレーザーの各種パラメータ（ピーク出力、平均出力、フルエンスなど）を計算します。

#### 光子エネルギー計算
光の波長から、光子1個が持つエネルギーを計算します。
- **計算式**: `E = hc / λ` (h: プランク定数, c: 光速, λ: 波長)

## 特徴

- **直感的なワークフロー**: 実際の測定手順に沿った2ステップ方式で、必要な値を簡単に算出できます。
- **ダークモード対応**: 目に優しい暗い配色に切り替え可能です。
- **単位変換機能**: W, mW, nWなどの単位を柔軟に選択できます。
- **レスポンシブデザイン**: PC、タブレット、スマートフォンなど、様々なデバイスで快適に利用できます。
- **外部ライブラリ不要**: 純粋なHTML/CSS/JavaScriptのみで動作し、高速かつ軽量です。

## 使用方法

1.  ブラウザでHTMLファイルを開きます。
2.  **推奨ワークフロー**:
    1.  センサー（プローブ）で測定した**総光出力（パワー）**と**光線ガイドの直径**を「ステップ①」に入力し、光強度を計算します。
    2.  計算結果を「ステップ②」に転記し、**目標エネルギー密度**を入力して必要な照射時間を算出します。
3.  必要に応じて「その他の計算ツール」もご利用ください。

## 注意事項

- **光出力について**: 消費電力ではなく、実際の光出力（放射束）を入力してください。
- **照射径**: 光が実際に照射される部分の直径を正確に測定してください。
- **安全性**: 医療用レーザーや高出力光源を使用する場合は、必ず安全基準を確認し、適切な保護具を着用してください。

## 想定される用途

- 歯科用レーザー治療のパラメータ設定
- 光線力学療法（PDT）の照射条件計算
- 研究実験での光照射条件の決定
- 光硬化型材料の硬化時間算出
- UV殺菌装置の照射時間計算
- パルスレーザーを用いた精密加工の条件設定

## 技術仕様

- HTML5
- CSS3 (カスタムプロパティ使用)
- JavaScript (ES6)

## ライセンス

MIT License

Copyright (c) 2025 Fumihiko Yoshino

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

## 作成者

吉野文彦（Fumihiko Yoshino）

## 更新履歴

- **V2.0** (2025年7月5日): ワークフローを2ステップ方式に再設計、UI/UXの大幅改善、ダークモードの安定化、基本計算機能の再追加
- **V1.0** (2025年7月4日): 初版リリース
