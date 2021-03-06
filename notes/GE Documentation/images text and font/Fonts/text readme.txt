E	North American English Release
J	Japanese
P	PAL (European) English Release

LwaxE & LwaxJ are copies of the LsevE & LsevJ files, respectively.
-------
To read in text, use the unsigned long offsets at the beginning of the file.  Second value in text code (ie. 04XX) is the offset in binary header to access text.

Some files (ie. LdepoX) are missing offsets.  To accurately grab all the text from the values, read the first offset in the file, then read all the long offsets until that address.
ie. LdepoE
0x0	00000090
read in 36 unsigned long values.  The following are valid:
00	01	02	03	04
05	06	07	08	09
0A	0B	0C	0D	0E
0F	10	11	12	13
18	19	1A	1B	1D
1E	1F	20	21	22

-------
Japanese language chart:	D180
J	118660-1257E0
E	117940-124AC0
P	1048B0-111A30
(all standard ascii accepted)

8*** characters are 0x60 bytes each (10x6); 1E8 entries total (B700)
J	118660-123D60
E	117940-123040
P	1048B0-10FFB0
8080	 	118660
8081	、
8082	$	1186C0
8083	(
8084	)	118720
8085	･
8086	%	118780
8087	「
8088	」	1187E0
8089	'
808A	"	118840
808B	<
808C	>	1188A0
808D	￥
808E	～	118900
808F	 

fixed width 0-9
8090	0	118960
8091	1
8092	2	1189C0
8093	3
8094	4	118A20
8095	5
8096	6	118A80
8097	7
8098	8	118AE0
8099	9

fixed width A-Z
809A	A	118B40
809B	B
809C	C	118BA0
809D	D
809E	E	118C00
809F	F
80A0	G	118C60
80A1	H
80A2	I	118CC0
80A3	J
80A4	K	118D20
80A5	L
80A6	M	118D80
80A7	N
80A8	O	118DE0
80A9	P
80AA	Q	118E40
80AB	R
80AC	S	118EA0
80AD	T
80AE	U	118F00
80AF	V
80B0	W	118F60
80B1	X
80B2	Y	118FC0
80B3	Z

80B4	!	119020
80B5	"
80B6	#	119080
80B7	'
80B8	*	1190E0
80B9	+
80BA	,	119140
80BB	ー
80BC	.	1191A0
80BD	/
80BE	:	119200
80BF	=
80C0	?	119260
80C1	@
80C2	｡	1192C0
80C3	ﾞ
80C4	ﾟ	119320

Katakana small characters
80C5	ァ	a (small)
80C6	ィ	i (small)	119380
80C7	ゥ	u (small)
80C8	ェ	e (small)	1193E0
80C9	ォ	o (small)
80CA	ッ	tu (small)	119440
80CB	ャ	ya (small)
80CC	ュ	yu (small)	1194A0
80CD	ョ	yo (small)
80CE	ヲ	wo	119500
80CF	ン	n

katakana
80D0	ア	a	119560
80D1	イ	i
80D2	ウ	u	1195C0
80D3	エ	e	
80D4	オ	o	119620
80D5	カ	ka
80D6	キ	ki	119680
80D7	ク	ku
80D8	ケ	ke	1196E0
80D9	コ	ko
80DA	サ	sa	119740
80DB	シ	si
80DC	ス	su	1197A0
80DD	セ	se
80DE	ソ	so	119800
80DF	タ	ta
80E0	チ	chi	119860
80E1	ツ	tu
80E2	テ	te	1198C0
80E3	ト	to
80E4	ナ	na	119920
80E5	ニ	ni
80E6	ヌ	nu	119980
80E7	ネ	ne
80E8	ノ	no	1199E0
80E9	ハ	ha
80EA	ヒ	hi	119A40
80EB	フ	hu
80EC	ヘ	he	119AA0
80ED	ホ	ho
80EE	マ	ma	119B00
80EF	ミ	mi
80F0	ム	mu	119B60
80F1	メ	me
80F2	モ	mo	119BC0
80F3	ヤ	ya
80F4	ユ	yu	119C20
80F5	ヨ	yo
80F6	ラ	ra	119C80
80F7	リ	ri
80F8	ル	ru	119CE0
80F9	レ	re
80FA	ロ	ro	119D40
80FB	ワ	wa

katakana voiced
80FC	ガ	ga	119DA0
80FD	ギ	gi
80FE	グ	gu	119E00
80FF	ゲ	ge
8180	ゴ	go	119E60
8181	ザ	za
8182	ジ	zi	119EC0
8183	ズ	zu
8184	ゼ	ze	119F20
8185	ゾ	zo
8186	ダ	da	119F80
8187	ヂ	di
8188	ヅ	du	119FE0
8189	デ	de
818A	ド	do	11A040
818B	バ	ba
818C	ビ	bi	11A0A0
818D	ブ	bu
818E	ベ	be	11A100
818F	ボ	bo

katakana semi-voiced
8190	パ	pa	11A160
8191	ピ	pi
8192	プ	pu	11A1C0
8193	ペ	pe
8194	ポ	po	11A220

fixed-width a-z
8195	a
8196	b	11A280
8197	c
8198	d	11A2E0
8199	e
819A	f	11A340
819B	g
819C	h	11A3A0
819D	i
819E	j	11A400
819F	k
81A0	l	11A460
81A1	m
81A2	n	11A4C0
81A3	o
81A4	p	11A520
81A5	q
81A6	r	11A580
81A7	s
81A8	t	11A5E0
81A9	u
81AA	v	11A640
81AB	w
81AC	x	11A6A0
81AD	y
81AE	z	11A700

Hiragana small characters
81AF	ぁ	a (small)
81B0	ぃ	i (small)	11A760
81B1	ぅ	u (small)
81B2	ぇ	e (small)	11A7C0
81B3	ぉ	o (small)
81B4	っ	su (small)	11A820
81B5	ゃ	ya (small)
81B6	ゅ	yu (small)	11A880
81B7	ょ	yo (small)
81B8	を	wo	11A8E0
81B9	ん	n

Hiragana
81BA	あ	a	11A940
81BB	い	i
81BC	う	u	11A9A0
81BD	え	e
81BE	お	o	11AA00
81BF	か	ka
81C0	き	ki	11AA60
81C1	く	ku
81C2	け	ke	11AAC0
81C3	こ	ko
81C4	さ	sa	11AB20
81C5	し	shi
81C6	す	tsu	11AB80
81C7	せ	se
81C8	そ	so	11ABE0
81C9	た	ta
81CA	ち	ti	11AC40
81CB	つ	tu
81CC	て	te	11ACA0
81CD	と	to
81CE	な	na	11AD00
81CF	に	ni
81D0	ぬ	nu	11AD60
81D1	ね	ne
81D2	の	no	11ADC0
81D3	は	ha
81D4	ひ	hi	11AE20
81D5	ふ	hu
81D6	へ	he	11AE80
81D7	ほ	ho
81D8	ま	ma	11AEE0
81D9	み	mi
81DA	む	mu	11AF40
81DB	め	me
81DC	も	mo	11AFA0
81DD	や	ya
81DE	ゆ	yu	11B000
81DF	よ	yo
81E0	ら	ra	11B060
81E1	り	ri
81E2	る	ru	11B0C0
81E3	れ	re
81E4	ろ	ro	11C120
81E5	わ	wa

Hiragana voiced
81E6	が	ga	11C180
81E7	ぎ	gi
81E8	ぐ	gu	11C1E0
81E9	げ	ge
81EA	ご	go	11C240
81EB	ざ	za
81EC	じ	zi	11C2A0
81ED	ず	zu
81EE	ぜ	ze	11C300
81EF	ぞ	zo
81F0	だ	da	11C360
81F1	ぢ	di
81F2	づ	du	11C3C0
81F3	で	de
81F4	ど	do	11C420
81F5	ば	ba
81F6	び	bi	11C480
81F7	ぶ	bu
81F8	べ	be	11C4E0
81F9	ぼ	bo

Hiragana semi-voiced
81FA	ぱ	pa	11C440
81FB	ぴ	pi
81FC	ぷ	pu	11C4A0
81FD	ぺ	pe
81FE	ぽ	po	11C500

Katakana
81FF	ヴ	vu	

kanji beginning with 8280 - 87D0


C*** kanji are 0x80 bytes each (10x8); 69 entries total (1A80)
J	123D60-1257E0
E	123040-124AC0
P	10FFB0-111A30
C080	￥	123D60
C081	キ
C082	ャ	123DE0
C083	ス
C084	ト	123E60
C085	メ
C086	イ	123EE0
C087	ン
C088	そ	123F60
C089	の

C0E8	市	125760
C0E9	民

A full index would be difficult/impractical without knowing exactly what format Rare used to index them all.
However, for whatever reason, GE's text samples include a ridiculous amount of possible kanji, most unused.

actual conversion:
(upper char & 0x7F)<<7 | (lower char & 0x7F)
