
# ItemRescue
bnscup2023で制作した3Dアクションゲームです。二人で作成しました。
[ゲームについて]
 アイテムを拾いながらNPC救うゲームです
 アイテムを拾う(掬う)と特殊行動ができるように
 移動している味方NPCに敵NPCが攻撃しにいくので、それらを排除していき、高スコア獲得を目指す


[プレイ方法]
　GithubからVisual Studioのソリューションをクローンして、ビルドしてください。
		https://github.com/Minogame321/ItemRescue
		　ビルドしてプレイする際にはBulletPhysicsを各自ダウンロードしてパスを通してください
  			参考：https://qiita.com/tas9n/items/522312d04013f3512f33

タイトルが出てきたら、START BUTTONをクリック。そしたら、一番左の石の上に乗るとゲームスタート。
味方キャラがお化けから逃げるので以下の行動でお化けに対抗しよう。
敵を倒す、敵がドロップするクリスタルを拾うとスコアが増える。
	ASDWキー：上下左右移動
	Enterキー：攻撃(当たるとお化けの体力が減る)
	Spaceキー：ジャンプ(2段ジャンプ可能)
	アイテムがある場合
		C：回復アイテム(味方のHP回復)
		X：ボムの使用(周囲のお化けを一網打尽)

[担当箇所]
	物理演算ライブラリPublletPhysicsの解析、及びSiv3Dの描画機能とのリンクを行い、物理エンジン機能の追加。(Siv3Dには3D空間での物理演算機能は存在しないため)
	物理演算ワールドクラス、物理物体クラスを作成し、簡単に物理物体、及び形状の登録と描画をできるようにした。
	3D空間にキャラクター画像を投影し、移動方向に応じた歩行モーションを描画する。
	攻撃についても同様に攻撃方向に斬撃エフェクトを描画する。