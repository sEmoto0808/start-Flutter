# start-Flutter
Flutterの環境構築をしてサンプルアプリをiOS/Androidでビルドする

## 環境構築
https://drive.google.com/drive/folders/1jmlcaxGaIfyL4o0Ghd1ctHKk3vaULy50

## Widgetについて
https://flutter.dev/docs/development/ui/widgets-intro
  
- 状態が変化するとframeworkによって差分が最小化されて、リビルドされる
- `runApp()` は渡されたwidgetをツリーのrootにする
- ツリーのroot widgetが画面全体を表示する
- 独自のwidgetを定義する時は `StatelessWidget` か `StatefulWidget` のサブクラスとして定義する
- `RenderObject` : widgetの形状を計算する

### Basic　Widget
- `Text` : スタイルを設定したテキストを表示する
- `Row, Column` : 縦横自由にレイアウトが組める。Webのflexboxをモデルに作られている
- `Stack` :
- `Container` : 矩形のオブジェクト。子要素に `Row` を持ったりできる。

マテリアルデザインのwidgetを使う場合は、 `MaterialApp` の子要素にする必要がある。
なので `runApp()` に渡すwidgetは `MaterialApp` にする。

```
Note: Material is one of the 2 bundled designs included with Flutter. 
To create an iOS-centric design, see the Cupertino components package, which has its own versions of CupertinoApp, and CupertinoNavigationBar.
```

### Handling gestures
- `GestureDetector` : ユーザーの操作を検出する。`Container` を子要素に設定することでタップされた時のコールバックを設定できる（ `onTap()` ）
- `GestureDetector` が検出できる操作: taps, drags, and scales
