# CatApps Doctor

Version: 0.1.0  
Build: 20260923-02

CatApps の独立障害診断・復旧ポータル。Google Apps Script 自体に到達できない障害でも開けるよう、GitHub Pages 上の静的サイトとして運用する。

## v0.1 PoC

- Google/GASに依存せずDoctor自身が起動することを確認する。
- CatMemos / CatAuth の通常URLと `authuser=0..4` の起動経路を提供する。
- `authuser` はGoogleアカウント固有値ではなくブラウザセッション上のaccount slotとして扱い、固定保存しない。
- Same-Origin Policyにより、外部Apps Scriptページが成功したかをDoctorから直接読み取る方式には依存しない。
- Googleログイン一覧の取得、Cookie読取、特定Googleアカウントの強制ログアウトは行わない。

## 目標

PoC実機結果を基に、自動化可能な診断だけをDoctorへ追加し、自動化不能な操作は一画面の復旧手順として提供する。

## 公開静的アセット

CatAppsDoctorは診断・復旧ポータルに限定する。CatApps共通のfavicon・公開画像・静的公開ファイルはpublic repository `LoveTheCat/CatAppsAssets` をSSOT / 配信元とし、Doctor repositoryには保持しない。
