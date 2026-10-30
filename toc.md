# 目次 — PC-100 Series MS-DOS プログラマーズリファレンスマニュアル

<!-- 出典画像: images/IMG_6163.JPEG 〜 images/IMG_6168.JPEG(目次 p.[1]〜[10]) -->

凡例:
- 「頁」は本文のページ番号。
- 名称は原本の印字に従う(明らかな誤植は修正済み)。

---

## 本書の構成について ……… 1

---

## 第1章 システムコール

<!-- IMG_6163 -->

| 節 | 題名 | 頁 |
|---|---|---|
| 1.1 | イントロダクション | 3 |
| 1.2 | プログラムとシステムコール | 3 |
| 1.2.1 | マクロアセンブラからのコール | 3 |
| 1.2.2 | 高級言語からのコール | 3 |
| 1.2.3 | 制御をMS-DOSに戻す方法 | 4 |
| 1.2.4 | コンソールとプリンタに対する入出力コール | 4 |
| 1.2.5 | ディスクI/Oシステムコール | 4 |
| 1.3 | ファイルコントロールブロック(FCB) | 4 |
| 1.3.1 | FCBのフィールド | 5 |
| 1.3.2 | 拡張FCB | 7 |
| 1.3.3 | ディレクトリエントリ | 7 |
| 1.3.4 | FCBのフィールド群 | 7 |
| 1.4 | システムコール | 9 |
| 1.4.1 | プログラミング例 | 10 |
| 1.5 | XENIXとコンパチブルなコール | 10 |
| 1.6 | 割り込み | 12 |

### 1.6 割り込み(割り込みタイプ)

| タイプ | 名称 | 頁 |
|---|---|---|
| 20H | Program Terminate | 13 |
| 21H | Function Request | 15 |
| 22H | Terminate Address | 16 |
| 23H | CTRL-C Exit Address | 16 |
| 24H | Fatal Error Abort Address | 16 |
| 25H | Absolute Disk Read | 20 |
| 26H | Absolute Disk Write | 22 |
| 27H | Terminate But Stay Resident | 24 |

### 1.7 ファンクションリクエスト ……… 26

<!-- IMG_6164 -->

| 節 | 題名 | 頁 |
|---|---|---|
| 1.7.1 | CP/Mとコンパチブルなコール | 26 |
| 1.7.2 | レジスタの処理 | 26 |

ファンクション一覧(INT 21H のファンクション番号):

| ファンクション | 名称 | 頁 |
|---|---|---|
| 00H | Terminate Program | 31 |
| 01H | Read Keyboard and Echo | 33 |
| 02H | Display Character | 34 |
| 03H | Auxiliary Input | 35 |
| 04H | Auxiliary Output | 36 |
| 05H | Print Character | 38 |
| 06H | Direct Console I/O | 40 |
| 07H | Direct Console Input | 42 |
| 08H | Read Keyboard | 44 |
| 09H | Display String | 46 |
| 0AH | Buffered Keyboard Input | 47 |
| 0BH | Check Keyboard Status | 49 |
| 0CH | Flush Buffer, Read Keyboard | 51 |
| 0DH | Disk Reset | 52 |
| 0EH | Select Disk | 53 |
| 0FH | Open File | 54 |
| 10H | Close File | 56 |
| 11H | Search For First Entry | 58 |
| 12H | Search For Next Entry | 60 |
| 13H | Delete File | 62 |
| 14H | Sequential Read | 64 |
| 15H | Sequential Write | 66 |
| 16H | Create File | 68 |
| 17H | Rename File | 70 |
| 19H | Current Disk | 72 |
| 1AH | Set Disk Transfer Address | 73 |
| 21H | Random Read | 75 |
| 22H | Random Write | 77 |
| 23H | File Size | 80 |
| 24H | Set Relative Record | 82 |
| 25H | Set Vector | 84 |
| 27H | Random Block Read | 86 |
| 28H | Random Block Write | 89 |
| 29H | Parse File Name | 92 |
| 2AH | Get Date | 95 |
| 2BH | Set Date | 97 |
| 2CH | Get Time | 99 |
| 2DH | Set Time | 101 |
| 2EH | Set / Reset Verify Flag | 103 |
| 2FH | Get Disk Transfer Address | 105 |
| 30H | Get DOS Version Number | 106 |
| 31H | Keep Process | 107 |
| 33H | CTRL-C Check | 108 |
| 35H | Get Interrupt Vector | 109 |
| 36H | Get Disk Free Space | 110 |
| 38H | Return Country_Dependent Information | 111 |
| 39H | Create Sub_Directory | 114 |
| 3AH | Remove Directory Entry | 115 |
| 3BH | Change the Current Directory | 116 |
| 3CH | Create a File | 117 |
| 3DH | Open a File | 118 |
| 3EH | Close a File Handle | 120 |
| 3FH | Read From File / Device | 121 |
| 40H | Write to File / Device | 122 |
| 41H | Delete Directory Entry | 123 |
| 42H | Move a File Pointer | 124 |
| 43H | Change Attributes | 125 |
| 44H | I/O Control for Devices | 126 |
| 45H | Duplicate a File Handle | 130 |
| 46H | Force a Duplicate of a Handle | 131 |
| 47H | Return Text of Current Directory | 132 |
| 48H | Allocate Memory | 133 |
| 49H | Free Allocated Memory | 134 |
| 4AH | Modify Allocated Memory Blocks | 135 |
| 4BH | Load and Execute a Program | 136 |
| 4CH | Terminate a Process | 139 |
| 4DH | Retrieve the Return Code of a Child | 140 |
| 4EH | Find Match File | 141 |
| 4FH | Step Through a Directory Matching Files | 143 |
| 54H | Return Current Setting of Verify After Write Flag | 144 |
| 56H | Move a Directory Entry | 145 |
| 57H | Get / Set Date/Time of File | 146 |

### 1.8 PC-100拡張割込み ……… 148

<!-- IMG_6165 (p.[4], [5]) -->

#### 1.8.1 画面の制御 ……… 149

| ファンクション | 名称 | 頁 |
|---|---|---|
| 10H | Output Character to Console | 149 |
| 11H | Store Character Literally | 149 |
| 12H | Store Character(Dot image) | 150 |
| 13H | Store Character of Arbitrary Shape | 150 |
| 18H | Enter Double Width Mode | 151 |
| 19H | Exit From Double Width Mode | 151 |
| 1AH | Enter Double Height Mode | 151 |
| 1BH | Exit From Double Height Mode | 152 |
| 1CH | Enter Reversed Video Mode | 152 |
| 1DH | Exit From Reversed Video Mode | 152 |
| 1EH | Enter Underline Mode | 153 |
| 1FH | Exit From Underline Mode | 153 |
| 20H | Change Color | 153 |
| 21H | Block Reverse | 154 |
| 22H | Read Current Attributes | 154 |
| 28H | Set Up Screen Dimension | 155 |
| 29H | Set Up Color/Monochrome Mode | 156 |
| 2AH | Set Up Miscellaneous Screen Mode | 156 |
| 2BH | Allocate Kana-Kanji Translation Lines | 157 |
| 2CH | Deallocate Kana-Kanji Translation Lines | 158 |
| 2DH | Read Screen Parameters | 158 |
| 30H | Save Cursor Position | 160 |
| 31H | Restore Cursor Position | 160 |
| 32H | Move Cursor Up | 160 |
| 33H | Move Cursor Down | 161 |
| 34H | Move Cursor Forward | 161 |
| 35H | Move Cursor Backward | 161 |
| 36H | Locate Cursor | 162 |
| 37H | Read Cursor Position | 162 |
| 38H | Turn On Cursor | 162 |
| 39H | Turn Off Cursor | 163 |
| 3AH | Change Cursor Style | 163 |
| 3BH | Get Current Cursor Attributes | 164 |
| 40H | Set Palette | 164 |
| 41H | Read Palette | 165 |
| 42H | Reset Palette | 165 |
| 48H | Clear To End Of Line | 166 |
| 49H | Clear To End Of Page | 166 |
| 4AH | Clear Screen | 166 |
| 4BH | Reset VRAM | 167 |
| 4CH | Initialize VRAM | 169 |
| 50H | Read Character Font | 169 |
| 51H | Read Kanji Font(Shift-JIS) | 170 |
| 52H | Read Kanji Font | 170 |
| 53H | Kanji Code Conversion | 171 |
| 54H | Select Font | 171 |
| 55H | Set Up User-Defined Character Font Table | 171 |
| 56H | Delete Font | 173 |
| 58H | Change Viewport(Character-wise) | 173 |
| 59H | Change Viewport(Dot-wise) | 174 |
| 5AH | Change Viewport and Clear(Character-wise) | 175 |
| 5BH | Change Viewport and Clear(Dot-wise) | 175 |

#### 1.8.2 フロッピーディスクの制御 ……… 176

| ファンクション | 名称 | 頁 |
|---|---|---|
| 60H | Initialize Floppy Disk Hardware | 176 |
| 61H | Read Sectors | 176 |
| 62H | Write Sectors | 177 |
| 63H | Verify Sectors | 178 |

#### 1.8.3 RS-232Cポートの制御 ……… 179

| ファンクション | 名称 | 頁 |
|---|---|---|
| 68H | Initialize RS-232C Port | 179 |
| 69H | Send Character to RS-232C Port | 179 |
| 6AH | Read USART Status | 180 |
| 6BH | Receive Character from RS-232C Port | 180 |
| 6CH | Set Communication Buffer | 180 |
| 6DH | Send Break Signal | 181 |
| 6EH | Flow Control | 181 |
| 6FH | Return Pointer To Communication Buffer | 181 |
| 70H | Output Command Byte to USART | 182 |
| 71H | Receive Character from RS-232C Port Non-Destructively | 182 |
| 72H | Read Current RS-232C Port Settings | 183 |

#### 1.8.4 キーボードの制御 ……… 184

<!-- IMG_6166 (p.[6]) -->

| ファンクション | 名称 | 頁 |
|---|---|---|
| 78H | Scan Keyboard | 184 |
| 79H | Read Native Code Non-Destructively | 185 |
| 7AH | Read Native Code Destructively | 186 |
| 7BH | Read Shift-JIS Code Non-Destructively | 186 |
| 7CH | Read Shift-JIS Code Destructively | 187 |
| 7DH | Flush Keyboard Buffer | 187 |
| 7EH | Set Softkey String | 187 |
| 7FH | Set Mapping Table of Function Keys | 188 |
| 80H | Set Interesting Characters | 191 |
| 81H | Enable/Disable Key Click Sound | 192 |
| 82H | Interrogate Pointers to Mapping Tables | 192 |
| 83H | Get Keyboard ID | 192 |

#### 1.8.5 プリンタの制御 ……… 193

| ファンクション | 名称 | 頁 |
|---|---|---|
| 88H | Copy Screen to Printer | 193 |
| 89H | Print Character | 193 |
| 8AH | Sense Printer Status | 193 |
| 8BH | Install Printer Driver | 194 |
| 8CH | Print Character without Code Conversion | 194 |

#### 1.8.6 その他 ……… 195

| ファンクション | 名称 | 頁 |
|---|---|---|
| 90H | Sound | 195 |
| 92H | Sense Dip Switch | 195 |

#### 1.8.7 関連資料 ……… 196

### 1.9 マウス割込み(INT33H) ……… 199

| ファンクション | 名称 | 頁 |
|---|---|---|
| 0H | Initialize Mouse | 199 |
| 1H | Turn On Mouse Cursor | 200 |
| 2H | Turn Off Mouse Cursor | 200 |
| 3H | Get Mouse Cursor Position and Button Status | 200 |
| 4H | Set Mouse Cursor Position | 201 |
| 5H | Get Mouse Button Press Status | 201 |
| 6H | Get Mouse Button Release Status | 202 |
| 7H | Set Horizontal Range | 202 |
| 8H | Set Vertical Range | 203 |
| 9H | Set Mouse Cursor Style | 203 |
| 0BH | Read Mouse Motion Counter | 204 |
| 0CH | Set User-Defined Subroutine Call Mask | 204 |
| 0FH | Set Mouse/Pixel Ratio | 205 |

### その他の節

| 節 | 題名 | 頁 |
|---|---|---|
| 1.10 | MS-DOSシステムコールにおけるマクロ定義例 | 206 |
| 1.11 | MS-DOSシステムコールによるプログラム例 | 212 |

---

## 第2章 MS-DOS V2.0デバイスドライバ

<!-- IMG_6166 (p.[7]) -->

| 節 | 題名 | 頁 |
|---|---|---|
| 2.1 | デバイスドライバとは | 217 |
| 2.2 | デバイスヘッダ | 218 |
| 2.2.1 | 次のデバイスフィールドに対するポインタ | 218 |
| 2.2.2 | アトリビュート(属性)フィールド | 219 |
| 2.2.3 | ストラテジと割り込みルーチン | 219 |
| 2.2.4 | 名前フィールド | 219 |
| 2.3 | デバイスドライバの作成方法 | 220 |
| 2.4 | デバイスドライバの登録 | 220 |
| 2.5 | リクエストヘッダ | 220 |
| 2.5.1 | ユニットコード | 221 |
| 2.5.2 | コマンドコードフィールド | 221 |
| 2.5.3 | メディアチェックとBPBの作成 | 222 |
| 2.5.4 | ステータスワード | 223 |
| 2.6 | ファンクションコールパラメータ | 225 |
| 2.6.1 | INIT | 225 |
| 2.6.2 | MEDIA CHECK | 226 |
| 2.6.3 | BPBの作成(BIOSパラメータブロック) | 226 |
| 2.6.4 | メディアディスクリプタバイト | 227 |
| 2.6.5 | リードまたはライト | 228 |
| 2.6.6 | 連続非破壊読み込み | 228 |
| 2.6.7 | ステータス | 229 |
| 2.6.8 | FLUSH | 229 |
| 2.7 | クロックデバイス | 229 |
| 2.8 | デバイスドライバ例 | 230 |
| 2.8.1 | ブロックデバイスドライバ | 230 |
| 2.8.2 | キャラクタデバイスドライバ | 242 |

---

## 第3章 MS-DOS技術資料

<!-- IMG_6167 (p.[8]) -->

| 節 | 題名 | 頁 |
|---|---|---|
| 3.1 | MS-DOSの初期化 | 251 |
| 3.2 | コマンドプロセッサ | 251 |
| 3.3 | MS-DOSディスクアロケーション | 252 |
| 3.4 | MS-DOSディスクディレクトリ | 252 |
| 3.4.1 | PC-100ディスクフォーマット | 254 |
| 3.5 | MS-DOS V2.0ファイルアロケーションテーブル | 256 |
| 3.5.1 | ファイルアロケーションテーブルの使用方法 | 256 |
| 3.6 | MS-DOS標準ディスクフォーマット | 257 |

## 第4章 MS-DOSコントロールブロックとワークエリア

| 節 | 題名 | 頁 |
|---|---|---|
| 4.1 | MS-DOSメモリマップ | 259 |
| 4.2 | MS-DOSプログラムセグメント | 259 |

## 第5章 EXEファイルの構造とローディング

| 節 | 題名 | 頁 |
|---|---|---|
| 5.1 | EXEファイルの構造とローディング | 263 |

---

## 第6章 PC-100エスケープシーケンス

<!-- IMG_6167 (p.[9]) -->

| 節 | 題名 | 頁 |
|---|---|---|
| 6.1 | イントロダクション | 265 |
| 6.2 | カーソル位置制御 | 267 |
| CUP | カーソル位置の設定 | 267 |
| HVP | カーソル水平,垂直位置の設定 | 267 |
| CUU | カーソルを上に移動する | 268 |
| CUD | カーソルを下に移動する | 268 |
| CUF | カーソルを右に移動する | 268 |
| CUB | カーソルを左に移動する | 269 |
| DSR | デバイスステータスレポートを要求する | 269 |
| CPR | カーソル位置のレポート | 269 |
| SCP | カーソル位置のセーブ | 270 |
| RCP | カーソル位置の回復 | 270 |
| SU | スクロールアップ | 270 |
| SD | スクロールダウン | 271 |
| IND | インデックス | 271 |
| RI | 逆インデックス | 271 |
| 6.3 | 文字,行,画面の消去 | 272 |
| ED | 画面の消去 | 272 |
| EL | 行の消去 | 272 |
| DL | 行の削除 | 273 |
| DCH | 文字の削除 | 273 |
| 6.4 | 文字,行の挿入 | 274 |
| IL | 行の挿入 | 274 |
| ICH | 文字の挿入 | 274 |
| 6.5 | カラーパレットの設定 | 275 |
| SP | カラーパレットの設定 | 275 |
| RP | カラーパレットの初期化 | 276 |

<!-- IMG_6168 (p.[10]) -->

| 節 | 題名 | 頁 |
|---|---|---|
| 6.6 | 画面モード,文字フォントの設定 | 277 |
| SGR | 文字のアトリビュートの設定 | 277 |
| SM(1) | モードの設定(1) | 279 |
| SM(2) | モードの設定(2) | 280 |
| SM(3) | モードの設定(3) | 280 |
| RM(2) | モードの解除(2) | 281 |
| RM(3) | モードの解除(3) | 281 |
| SCS | 文字セットの選択 | 282 |
| 6.7 | キーボードの再割り当て | 283 |
| RAK | キーボードの再割り当て | 283 |

---

## 付録A システム立ち上げ時のソフトキーの設定

| 節 | 題名 | 頁 |
|---|---|---|
| A.1 | イントロダクション | 285 |
| A.2 | SOFTKEY.DATのフォーマット | 285 |

## 付録B ブートセクタ

| 節 | 題名 | 頁 |
|---|---|---|
| B.1 | イントロダクション | 286 |
| B.2 | ブートセクタの割り当て | 286 |
| B.3 | RAMディスクバイト | 286 |
| B.4 | 画面モードバイト | 287 |
| B.5 | 通信モードバイト | 288 |
| B.6 | メディアIDバイト | 288 |

## 索引 ……… 289
