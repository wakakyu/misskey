# CHANGELOG about VRTL

VRTLのブランチで行われた変更点をまとめています

<!-- VV Please add changelog here VV -->

--- 2025.5.0-vrtl.1 released at this time ---

- fix(frontend): LTLが無効な場合、公式クライアント上でVSTLが利用出来なくなる問題を修正 #228

--- 2025.4.1-vrtl.1 released at this time ---

- fix(backend): 自分のフォロワー限定投稿に対するリプライがぶいみみソーシャルタイムラインで見えないことが有る問題を修正 - 2025/04/30 #224
- feat(backend): VRTLのサーバーリストを Redis にキャッシュし、取得に失敗した場合はキャッシュを使用するようにしました - 2025/04/30 #223

--- 2025.4.0-vrtl.1 released at this time ---

--- 2025.3.1-vrtl.1 released at this time ---

--- 2025.2.1-vrtl.1 released at this time ---

--- 2025.2.0-vrtl.1 released at this time ---

--- 2025.1.0-vrtl.2 released at this time ---

- fix(backend): Unexpectedly removed VRTL endpoints in 2025.1.0-vrtl.1
- fix(frontend): Unable to see VRTL when logged in

--- 2025.1.0-vrtl.1 released at this time ---

--- 2024.11.0-vrtl.1 released at this time ---

--- 2024.10.1-vrtl.1 released at this time ---

--- 2024.9.0-vrtl.1 released at this time ---

--- 2024.8.0-vrtl.1 released at this time ---

- fix(frontend): VRTL VSTLの名前が表示されないところがある問題 (anatawa12#97) - 2024/08/07
- fic(frontend): VRTL VSTLでリプライのトグルが表示されない問題 (anatawa12#92) - 2024/08/04

--- 2024.7.0-vrtl.1 released at this time ---

--- 2024.5.0-vrtl.2 released at this time ---

- chore(backend): VRTL参加サーバーの取得に失敗したときのリトライの間隔を短く
- feat: VRTL/VSTLに連合なし投稿を含めるかを選択可能に
  - もともとのVRTL/VSTLでは連合なし投稿が常に含まれていましたが、正しくVRTL/VSTLのノートを表現するために含めないようにできるようになりました
  - VSTLの場合、連合なし投稿を含めないようにしてもフォローしている人の連合なし投稿は表示されます
- fix(frontend): ウィジェットでVRTL/VSTLが使用できない問題を修正
- fix(backend): 自分自身に対するリプライがwithReplies = falseなVRTL/VSTLにて含まれていない問題を修正
- feat(backend): `vmimiRelayTimelineImplemented` と `disableVmimiRelayTimeline` nodeinfo に追加しました
	- これによりサードパーティクライアントがVRTLの有無を認知できるようになりました。
