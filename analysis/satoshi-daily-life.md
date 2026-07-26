# サトシ・ナカモトの日常・生態に関する記述の抽出

本文書は `doc/` に収録されたサトシ・ナカモト本人の文章（フォーラム投稿・メール・メーリングリスト投稿）から、
ビットコインの技術内容そのものではなく、**書き手の生活・環境・習慣・人となり**が読み取れる記述を抽出したものである。

対象は `doc/` 配下の全 987 ファイルのうち、差出人が Satoshi Nakamoto と判別できる **757 件**。
引用中の `>` で始まる被引用部（相手の発言）は除外し、サトシ自身が書いた本文のみを対象とした。

---

## 1. 仕事を持っていた（直接の証言）

もっとも明確なのが、Martti Malmi（sirius / sirius-m）宛のメールにある一文である。

> "I'm not going to be much help right now either, pretty busy with work, and need a break from it after 18 months development."
> （私も今はあまり力になれない。仕事がかなり忙しいし、18か月の開発のあと休みが必要だ）
> — [doc/martti-malmi/24.md](../doc/martti-malmi/24.md) 2009-07-21 04:14 +0100

ここでの "work" はビットコイン開発とは区別されている。同じ文で "after 18 months development"（＝ビットコイン開発）
と並置されているため、**ビットコイン以外に別の仕事を抱えていた**ことがわかる。
また "18 months development" は 2009年7月から逆算して 2008年初頭を開発開始とし、
後述の「設計・コーディングは2007年から」という自己申告と整合する。

同種の記述は繰り返し現れる。

| 日付 | 出典 | 記述 |
|---|---|---|
| 2009-06-14 | [martti-malmi/21](../doc/martti-malmi/21.md) | "Thanks, I've been really busy lately."（最近本当に忙しい） |
| 2010-03-06 | [martti-malmi/189](../doc/martti-malmi/189.md) | "There's a blog writer who wants to write a story about Bitcoin, but I don't have time right now to answer his questions."（取材依頼に答える時間がないので Martti に振る） |
| 2010-05-16 | [martti-malmi/192](../doc/martti-malmi/192.md) | "I've also been busy with other things for the last month and a half. **I just now downloaded my e-mail since the beginning of April.** I mostly have things sorted and should be back to Bitcoin shortly." |
| 2010-07-18 | [martti-malmi/210](../doc/martti-malmi/210.md) | "I'm losing my mind there are so many things that need to be done."（やることが多すぎて気が狂いそうだ） |
| 2010-07-29 | [bitcoin-forum/0532-06306](../doc/bitcoin-forum/0532-06306.md) | "If you don't believe me or don't get it, I don't have time to try to convince you, sorry." |
| 2010-08-27 | [bitcoin-forum/0921-11399](../doc/bitcoin-forum/0921-11399.md) | "Sorry, I've been so busy lately I've been skimming messages and I still can't keep up." |
| 2011-04-26 | [gavin-andresen/1](../doc/gavin-andresen/1.md) | "I've moved on to other things and will probably be unavailable."（他のことに移った。おそらく連絡がつかなくなる） |

とくに 2010-05-16 の「4月初め以降のメールを**今さっきまとめてダウンロードした**」は、
常時オンラインではなく、**まとまった空き時間ができたときに一括で処理する**という生活パターンを示している。

### 実際に生じた長期の沈黙

メッセージの時刻を並べると、この「忙しさ」は記録上の空白として現れる。

| 空白 | 期間 |
|---|---|
| 77日 | 2009-02-13 → 2009-05-02 |
| 53日 | 2010-03-24 → 2010-05-16（本人が「1か月半、他のことで忙しかった」と説明した期間） |
| 52日 | 2008-11-17 → 2009-01-08（v0.1 リリース直前の作り込み期間） |
| 36日 | 2009-06-14 → 2009-07-21（直後に「仕事が忙しい」と説明） |
| 34日 | 2009-07-21 → 2009-08-24 |
| 32日 | 2009-08-29 → 2009-09-30 |

---

## 2. 活動時間帯 — 起きていた時間と寝ていた時間

タイムスタンプの残る 716 件（フォーラム 539 件、メール 177 件）を UTC に換算して時刻分布を取った。

```
時刻(UTC)  投稿数
00 ######################  38
01 ##################      32
02 #############           23
03 #########               16
04 ########                15
05 #########               17
06 #####                   10
07 #                        2
08                          0     ←
09 #                        1     ← 完全な空白帯
10                          0     ←
11                          0     ←
12 #                        3
13 ##                       5
14 #########               16
15 ################        29
16 #################################   58
17 ###############################################  81
18 ##################################################  86  ←ピーク
19 ##################################  59
20 #################################   57
21 ####################################  63
22 #################################   58
23 ###########################         47
```

- **07:00–13:00 UTC の 7 時間に、2年半で 11 件（全体の 1.5%）しかない。**
  とくに 07:00–12:00 UTC に至っては **3 件（0.4%）**。
- ピークは **16:00–24:00 UTC**。この 8 時間だけで全体の **71%** を占める。
- この空白帯は年をまたいでも安定している（2009年: 119件中2件、2010年: 579件中9件）。

7時間連続でほぼ完全に沈黙する帯が数年間一貫して存在することは、**そこが睡眠時間帯だった**ことを強く示唆する。

### フォーラムのタイムスタンプは UTC である

`doc/bitcoin-forum/` の投稿時刻にはタイムゾーン表記がないが、次の理由から UTC と判断できる。

- タイムゾーンが明示されたメール群（177件）を UTC 換算した分布の**円周平均は 20.9 時**。
- タイムゾーン不明のフォーラム投稿（539件）をそのまま扱った分布の**円周平均は 20.3 時**。
- 両者の空白帯（07–13時）も一致する。

独立した2系統のデータが 0.6 時間以内で重なるため、フォーラムアーカイブの時刻は実質 UTC とみなせる。

### 曜日 — 週末も平日も働いていた

```
月 95   火 70   水 106   木 133   金 121   土 70   日 121
```

土日の合計が全体の **27%**（均等なら 29%）。**週末にほとんど活動が落ちない**。
仕事を持ちながら、ビットコインには曜日を問わず時間を割いていたことになる。

### 月別の活動量 — 熱量の推移

```
2008-10   1        2009-11  53        2010-07 160  ←Slashdot 掲載の月
2008-11  14        2009-12  24        2010-08 135
2009-01  13        2010-01  11        2010-09  38
2009-02   5        2010-02  68        2010-10  31
2009-05   6        2010-03  18        2010-11  22
2009-06   2        2010-05  17        2010-12  30
2009-07   1        2010-06  49        2011-01   2
2009-08   3                           2011-02   1
2009-09   1
2009-10  11
```

2010年7月（Slashdot 記事による流入）の 160 件が突出し、以後急速に減っていく。
2010-07-18 の "the slashdot flood of work we've got now. I'm losing my mind" はまさにこの山の最中の発言である。

---

## 3. タイムゾーン設定 — メールヘッダは一貫して英国時間

サトシのメールの時差表記を集計すると、次の3系統に分かれる。

| 時差 | 件数 | 使用アカウント／時期 |
|---|---|---|
| `+0800` | 28 | vistomail（2008-11 〜 2009-01。cryptography ML、Dustin Trammell 宛） |
| `+0000` | 103 | gmx.com（冬期） |
| `+0100` | 46 | gmx.com（夏期） |
| `(UTC+01:00)` / `(UTC)` | 3 | anonymousspeech / vistomail（Adam Back 宛） |

`gmx.com` アカウント（2009-02 以降）の `+0000` / `+0100` の切り替わりは、**英国の夏時間の切替日と一致する**。

| 英国 DST 切替 | 直前のメール | 直後のメール |
|---|---|---|
| 2009-10-25 | 2009-10-24 `+0100`（[martti-malmi/41](../doc/martti-malmi/41.md)） | 2009-10-26 `+0000`（[martti-malmi/42](../doc/martti-malmi/42.md)） |
| 2010-03-28 | 2010-03-06 `+0000` | 2010-05-16 `+0100`（[martti-malmi/192](../doc/martti-malmi/192.md)） |
| 2010-10-31 | 2010-10-04 `+0100`（[martti-malmi/237](../doc/martti-malmi/237.md)） | 2010-12-01 `+0000`（[martti-malmi/238](../doc/martti-malmi/238.md)） |

2009-10-25 の切替は**前後2日以内で正確に挟み込めている**。2010年の2回は前後にメールの空白期間があるため
挟み込みは粗いが、夏期＝`+0100`／冬期＝`+0000` という対応自体は3回とも崩れていない。

つまりメールクライアント（またはメールサーバ）の設定は **Europe/London** に固定されていた。

ただし前節の活動時間帯と突き合わせると矛盾が生じる。空白帯 07:00–13:00 UTC は、
ロンドン時間ではちょうど **朝7時〜昼1時**にあたり、そこで毎日寝ていたことになってしまう。
一方、たとえば北米東部時間（UTC−5）なら **深夜2時〜朝8時**で自然な睡眠帯になる。
**メールヘッダの時差表記と、実際の生活リズムは食い違っている。**

なお `+0800`（2008年11月〜2009年1月）は vistomail というウェブメールサービス経由の投稿であり、
サーバ側のタイムゾーンを反映している可能性が高い。本人の所在地の証拠としては弱い。

---

## 4. 使っていた機材とソフトウェア環境

| 種別 | 記述 | 出典 |
|---|---|---|
| 主環境 | Windows。「Linux移植をやるとテストとビルドの手間が倍になる」と渋る | [martti-malmi/44](../doc/martti-malmi/44.md) 2009-10-27 |
| コンパイラ | "That's with mingw. That's the better compiler, **I only used VC for debugging**." | [martti-malmi/29](../doc/martti-malmi/29.md) 2009-08-24 |
| Linux機 | "I've been working on getting **my linux machine** set up and building the dependencies." | [martti-malmi/46](../doc/martti-malmi/46.md) 2009-10-29 |
| Linux配布 | Ubuntu 9.10 Karmic 64bit → のちに 10.04。"I disabled gdm on my Ubuntu system so it boots into command line." | [bitcoin-forum/0018-00174](../doc/bitcoin-forum/0018-00174.md), [0060-00434](../doc/bitcoin-forum/0060-00434.md) |
| CPU | "I have dual-proc, so I ran two memory hogs." | [bitcoin-forum/0383-03295](../doc/bitcoin-forum/0383-03295.md) 2010-07-15 |
| 持っていない機材 | "I hope someone can test an i5 or AMD to check that I built it right. **I don't have either to test with.**" | [bitcoin-forum/0820-09478](../doc/bitcoin-forum/0820-09478.md) 2010-08-15 |
| 旧ドライブ | "I tested it on a slow **7 year old drive**" | [bitcoin-forum/1931-24662](../doc/bitcoin-forum/1931-24662.md) 2010-11-26 |
| ブラウザ | 「新規登録ページでダウンロードバーが入力欄を隠す（with Firefox）」 | [martti-malmi/21](../doc/martti-malmi/21.md) 2009-06-14 |
| デスクトップ | "Every other systray icon **on my computer** is in the startup folder" / "I see OpenOffice.org and a number of other things on my computer do it that way" | [martti-malmi/38](../doc/martti-malmi/38.md), [martti-malmi/31](../doc/martti-malmi/31.md) |
| 常時稼働ノード | "Right now (04:50 GMT) **my node** is connecting to yours and getting zombie connections each time." | [martti-malmi/76](../doc/martti-malmi/76.md) 2009-11-12 |
| ネット環境 | SourceForge のログインページに何日もアクセスできない状態が続く | [martti-malmi/24](../doc/martti-malmi/24.md) 2009-07-21 |

要するに **メイン機は Windows + mingw、別に Linux のテスト機を持ち、自宅ノードを常時稼働させ、
i5 や AMD は所有していない**という、それほど豪華ではない開発環境である。

なお 2009-11-12 のメールで自分の作業時刻を **"04:50 GMT"** と書いており、
この時点で GMT を自分の基準時計として使っていたことがわかる（前節の設定と整合）。

---

## 5. 言語習慣 — 英国式綴りとアメリカ式の混在

サトシ本人の文章全体で綴りを機械的に数えると、**英国式が明確に優勢だが完全に一貫してはいない**。

| 英国式 | 件数 | 米国式 | 件数 |
|---|---|---|---|
| favour / favours | 4 | favor | 0 |
| neighbour(s) | 5 | neighbor | 0 |
| defence | 2 | defense | 0 |
| grey | 3 | gray | 0 |
| labelled / cancelled | 5 | labeled / canceled | 0 |
| maths | 2 | math | 0 |
| cheque | 2 | — | — |
| analyse / sceptical | 2 | analyze / skeptical | 0 |
| optimis- | 14 | optimiz- | 8 |
| colour | 4 | color | 4 |
| realis- | 1 | realiz- | 6 |
| licence | 0 | license | 9 |

英国・英連邦系の語彙も使う。

> "Writing a description for this thing for general audiences is **bloody hard**."
> — [bitcoin-forum/0234-01976](../doc/bitcoin-forum/0234-01976.md) 2010-07-05

> "Searching for themes is futile, there are thousands of **rubbish** themes."
> — [martti-malmi/80](../doc/martti-malmi/80.md) 2009-11-14

> "Do you have electronic transfer or paper **cheque** in your country?"
> — [martti-malmi/142](../doc/martti-malmi/142.md) 2010-02-04

> "boring **grey** in **colour**"（金に代わる仮想の金属を説明する有名なくだり）
> — [bitcoin-forum/0583-11405](../doc/bitcoin-forum/0583-11405.md) 2010-08-27

一方で `license` `realize` `organize` は米国式で書いており、`colour` と `color` は 4 対 4 で拮抗する。
**英国式に寄せる意識はあるが、徹底しきれていない**という状態である。

---

## 6. 仕事のやり方・性格

**自己認識：コードは得意、文章は苦手**

> "It's very attractive to the libertarian viewpoint if we can explain it properly. **I'm better with code than with words** though."
> — [cryptography-list/23](../doc/cryptography-list/23.md) 2008-11-15

> "What we need most right now is website writing. **My writing is not that great, I'm a much better coder.**"
> — [martti-malmi/1](../doc/martti-malmi/1.md) 2009-05-02

**細部への執着**

> "I have a program I use to find all the spacing inconsistencies at the beginning and ending of strings in your .po file and **manually fix them up** before I upload them to SVN."
> — [bitcoin-forum/0151-03238](../doc/bitcoin-forum/0151-03238.md) 2010-07-15

> "Make sure you use the .po file I uploaded to SVN or in a release, because **I always fix up at least a few things.**"
> — [bitcoin-forum/0151-15360](../doc/bitcoin-forum/0151-15360.md) 2010-10-04

翻訳ファイルの前後の空白のズレを検出する専用プログラムまで自作して、毎回手で直してからコミットしていた。

**コーディングの好み**

> "you can probably tell from the code that **I'm not a fan of** [大きなコメントヘッダ] for interior functions. Big obligatory comment headers for each function space out the code and make you hesitate about creating [新しい関数]."
> — [bitcoin-forum/0393-03510](../doc/bitcoin-forum/0393-03510.md) 2010-07-16

> "**I hate reinventing the wheel** and only resorted to writing my own serialization routines reluctantly."
> — [bitcoin-forum/0632-07090](../doc/bitcoin-forum/0632-07090.md) 2010-08-02

> "**I usually shy away from iostreams.** Seems like I too often hit limitations. They kind of botched the C++ streams standard in the 90's"
> — [bitcoin-forum/0921-11399](../doc/bitcoin-forum/0921-11399.md) 2010-08-27

90年代のC++標準化事情を実感として語っており、その時期に既に実務でC++を書いていた人物であることを示唆する。

**優先順位のつけ方はきわめて現実的**

> "Auto-run might give us 300% more nodes while Linux might give us 3% more. Linux would help server farms, but actually we'd like to favour individual users."
> — [martti-malmi/31](../doc/martti-malmi/31.md) 2009-08-29

**リスク回避的**

> "Please promise me you won't make a switch now. The last thing we need is switchover hassle on top of the slashdot flood of work we've got now."
> — [martti-malmi/210](../doc/martti-malmi/210.md) 2010-07-18

> "Bottom line is **I'd rather call an existing file copy function than make and test my own.**"
> — [bitcoin-forum/0921-11399](../doc/bitcoin-forum/0921-11399.md) 2010-08-27

---

## 7. 感情の出た瞬間

普段は淡々としているが、地の感情が出ている箇所がある。

| 記述 | 出典 |
|---|---|
| "**Oh crap**, I got your sourceforge usernames mixed up, sorry about that. I clicked on the wrong e-mail when I was looking for your username." | [martti-malmi/5](../doc/martti-malmi/5.md) 2009-05-04 |
| "Sourceforge is just so **darn** slow. I don't know what else to do though." | [martti-malmi/44](../doc/martti-malmi/44.md) 2009-10-27 |
| "So **dang**, there goes all the nice wxWidgets portability support functions." | [martti-malmi/60](../doc/martti-malmi/60.md) 2009-11-06 |
| "**My head hurts** just thinking about that." | [bitcoin-forum/0012-00055](../doc/bitcoin-forum/0012-00055.md) 2009-12-12 |
| "**Sorry to be a wet blanket.**"（水を差してすまない）— 2度使用 | [bitcoin-forum/0234-01976](../doc/bitcoin-forum/0234-01976.md), [0393-03510](../doc/bitcoin-forum/0393-03510.md) |
| "**I'm losing my mind** there are so many things that need to be done." | [martti-malmi/210](../doc/martti-malmi/210.md) 2010-07-18 |
| "**Sigh...** why delete a wallet instead of moving it aside and keeping the old copy just in case?" | [bitcoin-forum/1327-15136](../doc/bitcoin-forum/1327-15136.md) 2010-10-03 |
| "**I love the idea** of virtual, non-geographic communities experimenting with new economic paradigms." | [p2p-research/6](../doc/p2p-research/6.md) 2009-02-13 |
| "**Hey Zooko!** I wanted to thank you for posting about Bitcoin on your blog a year or two ago" | [bitcoin-forum/0890-10723](../doc/bitcoin-forum/0890-10723.md) 2010-08-22 |
| "WikiLeaks has **kicked the hornet's nest**, and the swarm is headed towards us."（最後から2番目のフォーラム投稿） | [bitcoin-forum/2216-29280](../doc/bitcoin-forum/2216-29280.md) 2010-12-11 |

謝罪と自己卑下がやや多い。"Sorry" で始まる文が繰り返し現れ、
自分が水を差す側に回るときは必ず前置きを入れる、という礼儀のパターンがある。

---

## 8. 匿名性の実践

- メールアドレスの変遷：`satoshi@anonymousspeech.com`（2008-08、Adam Back 宛）
  → `satoshi@vistomail.com`（2008-11 〜 2009-01）→ `satoshin@gmx.com`（2009-02 以降）。
  いずれも匿名志向のサービスで、実名につながる商用プロバイダを使っていない。
- 自分自身の運用でもパスワード・権限を最小化する。
  > "Since there's no SSL login, I want to mainly use that account with sub-admin powers and **use the admin account as little as possible.**"
  > — [martti-malmi/21](../doc/martti-malmi/21.md) 2009-06-14
- 自分のサイトで言えることと言えないことを区別している。
  > "There are a lot of things you can say on the sourceforge site that **I can't say on my own site**."
  > — [martti-malmi/19](../doc/martti-malmi/19.md) 2009-06-11
- 匿名の資金提供者を抱えていたが、匿名ゆえに使いにくいとこぼす。
  > "There are donors I can tap if we come up with something that needs funding, but **they want to be anonymous, which makes it hard to actually do anything with it.**"
  > — [martti-malmi/24](../doc/martti-malmi/24.md) 2009-07-21
- 取材は Martti に振る（[martti-malmi/189](../doc/martti-malmi/189.md) 2010-03-06）。
- 最後に Gavin へ：
  > "**I wish you wouldn't keep talking about me as a mysterious shadowy figure**, the press just turns that into a pirate currency angle. Maybe instead make it about the open source project and give more credit to your dev contributors; it helps motivate them."
  > — [gavin-andresen/1](../doc/gavin-andresen/1.md) 2011-04-26

---

## 9. 経歴についての自己申告

| 記述 | 出典 |
|---|---|
| "The design and coding started in **2007**." | [bitcoin-forum/0013-00046](../doc/bitcoin-forum/0013-00046.md) 2009-12-10 |
| "I wish there was something like that when I originally researched this **three years ago**, there was scant to nothing back then."（2010年3月時点＝2007年） | [jon-matonis/1](../doc/jon-matonis/1.md) 2010-03-04 |
| "The design supports a tremendous variety of possible transaction types that I designed **years ago**." | [bitcoin-forum/0195-01611](../doc/bitcoin-forum/0195-01611.md) 2010-06-17 |
| "When I wrote it **more than 2 years ago**, there were screaming hot SHA1 implementations but minimal attention to SHA256."（2010年7月時点＝2008年前半にはSHA256実装を書いていた） | [bitcoin-forum/0453-04068](../doc/bitcoin-forum/0453-04068.md) 2010-07-18 |
| "pretty busy with work, and need a break from it after **18 months development**"（2009年7月時点＝2008年初頭から本格開発） | [martti-malmi/24](../doc/martti-malmi/24.md) 2009-07-21 |
| "I started implementing a **marketplace feature** earlier ... it's only half done though. A bit like e-bay but without auctions" | [mike-hearn/8](../doc/mike-hearn/8.md) 2009-04-14 |
| "I wasn't aware of the b-money page, but my ideas start from exactly that point."（Wei Dai の b-money を Adam Back に教えられて初めて知った） | [adam-back/3](../doc/adam-back/3.md) 2008-08-21 |

「2007年に設計とコーディングを開始 → 2008年初頭から本格開発 → 2008年8月に論文の引用確認 → 2008年10月に論文公開」
という時系列を、本人が複数の相手に一貫して語っている。

---

## 10. 生活・世界観がにじむ記述

- **金融についての実感**：金（gold）の性質、信用バブル、身分詐称による口座からの引き出しなど、
  一般ユーザ視点の不満として語る。
  > "Banks let anyone who has your name and account number drain your account, and you're not going to get it back"
  > — [martti-malmi/5](../doc/martti-malmi/5.md) 2009-05-04
- **HTTPS への態度**：一ユーザとしての苛立ちを述べている。
  > "**As a user** I'm a little annoyed when it takes time to verify the identity of some no-name site I casually came across."
  > — [martti-malmi/105](../doc/martti-malmi/105.md) 2009-11-21
- **Wikipedia の使用者**：
  > "I often come across annoying red links of things that Wiki ought to at least have heard of."
  > — [bitcoin-forum/0652-14729](../doc/bitcoin-forum/0652-14729.md) 2010-09-30
- **情報源**：Slashdot、Wikipedia、Zooko のブログ、InfoWorld、`themonetaryfuture.blogspot.com` などを
  日常的に追っている様子がうかがえる。
- **「cryptocurrency」という語との出会い**：この語を自分で作ったのではなく、他人の造語として知り、
  採用するかどうかを Martti に相談している。
  > "Someone came up with the word 'cryptocurrency'... maybe it's a word we should use when describing Bitcoin, **do you like it?**"
  > — [martti-malmi/19](../doc/martti-malmi/19.md) 2009-06-11
- **公開・非公開の線引きに神経質**：Martti が FAQ に書いた自分の発言を削除させている。
  > "could you delete the last sentence on the FAQ ... **that's not really something I meant to say publicly.**"
  > — [martti-malmi/19](../doc/martti-malmi/19.md) 2009-06-11
- **投資として売り込むことへの慎重さ**：
  > "I'm uncomfortable with explicitly saying 'consider it an investment'. That's a dangerous thing to say and you should delete that bullet point."
  > — [martti-malmi/19](../doc/martti-malmi/19.md) 2009-06-11

---

## 11. まとめ — 記録から復元できる「生態」

1. **ビットコイン以外の仕事を持っていた。** 本人が "pretty busy with work" と明言し、
   数週間〜2か月半の音信不通が繰り返し発生し、その後まとめてメールを処理する。
2. **活動は 16:00–24:00 UTC に集中し、07:00–13:00 UTC はほぼ完全に沈黙する。**
   この 7 時間の空白が 2 年半一貫しており、睡眠時間帯と考えられる。
3. **週末も平日も関係なく作業していた。** 土日の投稿比率は 27%（均等なら 29%）。
4. **メールクライアントの設定は Europe/London で固定**（英国夏時間の切替日と正確に一致）。
   ただしこれは活動時間帯とは整合しない。
5. **綴りは英国式が優勢だが不完全**（`favour`/`neighbour`/`grey`/`cheque`/`maths` の一方で `license`/`realize`）。
   "bloody hard"、"rubbish" といった英連邦系の口語も使う。
6. **開発環境は Windows + mingw が主、別に Ubuntu のテスト機**。i5 や AMD の実機は持っていなかった。
   ブラウザは Firefox、7年前の HDD でテストするなど、機材は潤沢ではない。
7. **極端に細かい**。翻訳ファイルの空白のズレを検出する自作ツールを持ち、毎回手で直す。
8. **文章は苦手だと繰り返し自認**し、広報・執筆は Martti に委ねた。
9. **匿名性の運用は徹底**。匿名メールサービスのみを使い、admin 権限すら日常使いを避け、
   取材は他人に振り、最後には Gavin に「自分を謎めいた人物として語らないでほしい」と頼んだ。
10. **2010年7月の Slashdot 流入が転機**。投稿数は同月 160 件で最大となり、
    "I'm losing my mind" と漏らしたあと、活動量は単調に減少して 2011年4月に姿を消す。

---

## 注意事項

- 引用は `doc/` 配下の本文に基づく。`doc/` 自体は `src/` の一次資料から機械変換されたものであり、
  元資料の変換誤差（HTML エンティティ、改行、`&nbsp;` の混入など）を含みうる。
- タイムスタンプはメールヘッダやフォーラムの記録値であり、送信者が偽装・設定変更していた可能性は排除できない。
  とくに `+0800`（vistomail 期）は経由したウェブメールサーバの時刻である可能性が高い。
- `doc/mike-hearn/`、`doc/bitcoin-list/`、`doc/p2p-foundation/` の一部はタイムゾーン表記を欠くため、
  時刻分布の集計（716 件）から除外している（Satoshi 名義の全 757 件のうち 41 件）。
- 綴りの集計は正規表現による機械的な計数であり、引用・コード断片が完全には排除できていない可能性がある。
- 本文書は所在地・国籍・個人の特定を目的としたものではない。記録から直接読み取れる事実と、
  そこから言える範囲の推論のみを記載している。
