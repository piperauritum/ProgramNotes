# 池田拓実（コンピュータ）ソロ

#### 演奏
2022年9月10日、Ftarri 水道橋店、池田拓実・Iannis Zannos

## 概要

コンピュータ・ソロとは言うものの、コンピュータは楽器ではない。語の本来の意味では計算機、その実態は事務用品である。そもそも音楽のために作られたものではない。コンピュータを演奏に用いることは、石を演奏に用いるのと同じく誤用である（尚、業界用語で半導体は"石"とも呼ばれる）。以前、石で音楽を演奏するという、ある意味で不可能に近い演目[^1]に取り組むことで、そもそも何が音楽なのかという問いが生じた。大多数の楽器との相違点として、コンピュータそれ自体は音を発するために物として振動しない。振動するのは専らヘッドフォンであったり、Bluetooth接続されたスピーカーであって、コンピュータ本体は振動する必要がどこにもない。その代わり、近年は計算能力の向上によって複雑な構造体の振動をシミュレートできるようになり、物理モデル化されたピアノや弦楽器、金管楽器、木管楽器の音源が製品として販売されている。コンピュータが扱っているのは物理的な振動ではなく、飽くまで情報としての振動である。

楽器ではなく、本質的に計算機であるところのコンピュータを"演奏"することとは、つまるところ情報を操作することである。コンピュータ演奏の勘所となる概念が、アルゴリズムとの対話である[^2]。ユーザーが与えた入力に対して何らかのアルゴリズム、手続きによって、コンピュータは何かしらの反応をする。プログラムを作り込み、手続きが膨大になると、それは特定の音楽を演奏するための楽譜に接近する。楽譜にも様々な位相があり、綿密に書き込まれた"建築図面"から、簡単な"指示書"も存在する。図面から指示書に戻る、つまりアルゴリズムを単純化し、あるいは処理を小分けして、小分けにした処理を視覚的に操作するためのインターフェースを作成する。一旦コンピュータに委譲した手続きを分解し、ユーザー側に再委譲するという考えである。ユーザー、即ち演奏者は音というよりは情報を操作し、操作に応じたインターフェースの振る舞いが音楽として知覚される、という手順となる。

これまで専らアルゴリズムに注視した、本質的にモノフォニックな演奏とは異なり、ポリフォニックな"具体音楽"を生演奏しようと思ったのが、本企画の端緒である。ポリフォニックであるため単独企画が可能だろうと考えた次第である。

[^1]: Christian Wolff, "Stones" http://www.frogpeak.org/unbound/wolff/wolff_prose_collection.pdf
[^2]: 久保田晃弘、「遙かなる他者のためのデザイン」 http://www.bnn.co.jp/books/8517/

## Opening Acts

Iannis Zannos氏はSuperColliderのエキスパートであり、The SuperCollider Book (MIT Press) [^3]には「Programming in SuperCollider」の章を執筆している。池田はこれまで、ギリシャ-日本間の遠隔ライブコーディング（センサー装着ダンサーとのセッション）や、クセナキス「Duel」の再解釈でコラボレーションを行っている。当日はダンサーであるTasos Pappas Petridis氏がセンサーを装着、ギリシャよりリモートで演奏に参加する。

Zannos氏はセンターを用いたダンサーの動作の検出と音楽への利用を試みている。ライブコーディング版「Duel」では後半、ダンサーもリモート参加する。全ての参加者はOSCgroups[^4]によってSuperColliderに対する命令を共有しており、音声信号ではなく音響合成プログラムが全ての参加者の端末で実行される。日本から送信されたプログラムはギリシャで実行され、当地のダンサーのコントロールによって音響が生成される。

本年2022年は、クセナキスの生誕100年に際して数々の行事が行なわれており、池田とZannosによるDuelの再解釈もその一環である。池田の解釈では、Duelは人間化されたアルゴリズム作曲であり、言わば「逆シミュレーション音楽」[^5]の祖先でもある。利得行列によって曲を構成するというクセナキスの当初の構想を確実にするため、池田は原曲のゲーム行列を簡易的遺伝的アルゴリズム(GA)によって改良し、原曲のオーケストラをライブコーディングに置き換えたバージョンをZannos氏の助力により作成した。

以下はDuelのゲーム行列である。6種の戦術をXとYが交互に実行し、ゲーム行列における戦術の組み合わせ（交点）が得点となる。正数はX、負数はYの得点となる。例えばYによる戦術IVの後で、Xが戦術IIIを実行するとXは5点を得られる。この行列のうち5点を稼げるのはこの組み合わせだけなので、結局Yの相対的損失を考慮すればYが戦術IVを選ぶことはかなり稀と思われる。またシミュレーションの結果からも、この行列はXに圧倒的に有利であると考えられ、池田は簡易GAによるゲーム行列の改良を思い至った。改良の結果、シミュレーションによるXとYの勝率は概ね互角となった。本当に互角であるのかはライブ演奏によって検証される。

<table>
	<colgroup></colgroup>
	<colgroup></colgroup>
	<colgroup></colgroup>
	<colgroup></colgroup>
	<tr>
		<td colspan=2 rowspan=2></td>
		<td colspan=6 align="center">Y</td>
		</tr>
	<tr>
		<td>I</td>
		<td>II</td>
		<td>III</td>
		<td>IV</td>
		<td>V</td>
		<td>VI</td>
	</tr>
	<tr>
		<td rowspan=6>X</td>
		<td>I</td>
		<td>-1</td>
		<td>1</td>
		<td>3</td>
		<td>-1</td>
		<td>1</td>
		<td>-1</td>
	</tr>
	<tr>
		<td>II</td>
		<td>1</td>
		<td>-1</td>
		<td>-1</td>
		<td>-1</td>
		<td>1</td>
		<td>-1</td>
	</tr>
	<tr>
		<td>III</td>
		<td>3</td>
		<td>-1</td>
		<td>-3</td>
		<td>5</td>
		<td>1</td>
		<td>-3</td>
	</tr>
	<tr>
		<td>IV</td>
		<td>-1</td>
		<td>3</td>
		<td>3</td>
		<td>-1</td>
		<td>-1</td>
		<td>-1</td>
	</tr>
	<tr>
		<td>V</td>
		<td>1</td>
		<td>-1</td>
		<td>1</td>
		<td>1</td>
		<td>-1</td>
		<td>-1</td>
	</tr>
	<tr>
		<td>VI</td>
		<td>-1</td>
		<td>-1</td>
		<td>-3</td>
		<td>-1</td>
		<td>-1</td>
		<td>3</td>
	</tr>
</table>


[^3]: https://lbahp.mitpress.mit.edu/books/supercollider-book
[^4]: http://www.rossbencina.com/code/oscgroups
[^5]: https://www.iamas.ac.jp/~mmiwa/rsm.html

#### Reference

Iannis Zannos, Takumi Ikeda, “35. Phoenix-Albatross: An Approach to Iannis Xenakis’s Work on Game Theory through Live Coding and Networked Dance”, 2024 [https://doi.org/10.11647/OBP.0390.37](https://doi.org/10.11647/OBP.0390.37)

---
*Copyright © 2025 Takumi Ikeda All Rights Reserved. 禁無断転載*
