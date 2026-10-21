book-atelier 도트 걷기 다시 뽑기 — alice·손자(sunzi)·춘향(chunhyang) 걷기 시트만 인물마다 한 장씩, 모두 세 장.

왜 다시 뽑나: 지난 걷기 시트는 여섯 칸 중 1·3·4·6 칸이 모두 "가까운 다리가 앞" 이라, 다리가 번갈아 나가지 않았다
(4번 칸에 가까운 다리가 뒤로 뻗고 먼 다리가 앞으로 내딛는 자세가 없다). 그래서 이번에는 다리 자세 안내 그림을 같이 붙인다.

먼저 읽을 것: book-atelier 의 docs/ATELIER_PIXEL_ART_PLAN.md 10절 체크포인트(걷기 고침), IMAGE_RULES.md 7절.

인물마다 첨부 세 장 (순서대로):
1. 그 인물의 정지 도트 6배 — alice_begin_still_x6.png · sunzi_begin_still_x6.png · chunhyang_begin_still_x6.png (claude가 준 파일)
2. 다리 자세 안내 — walk_leg_guide.png (claude가 준 파일, 1024×1536, 3×2 칸). 진한 남색 = 가까운 다리, 회색 = 먼 다리. 모양·색은 따르지 말고 칸마다 다리 위치만 따른다
3. 그 인물의 정본 — https://polos0117.github.io/book-atelier-img/img/<인물>_<정본 폼>_literary_fantasy_f.webp
   (alice 는 alice_end_…, 손자·춘향은 <인물>_begin_…)

지킬 것:
- 인물마다 한 번, 걷기 시트 한 장. 세 인물을 따로 생성한다.
- 결과가 마음에 안 들어도 다시 뽑거나 고치지 말고 그대로 보여줘. 크롭·축소·보정 금지.
- 저장소에 올리지 마. 원본 PNG 세 장만 나한테 넘겨줘. 이름은 <인물>_begin_walk_gen2.png
- 기존 이미지 삭제, 강제 push, 이력 재작성 금지.

공통 프롬프트 (세 장 모두, [인물 묘사] 자리에 아래 그 인물의 한 줄):

Pixel art WALK CYCLE sprite sheet of the EXACT same character as attached image 1 — a finished pixel-art sprite.
Copy it pixel for pixel in style: same very large chunky pixels, same 16-colour palette, same dark outline,
same proportions (about 4 heads tall), same face. [인물 묘사]
Keep decoration as simple as image 1 — do not add new details. Image 3 is only a colour and face reference.

Sheet layout: portrait canvas 1024 x 1536, 6 frames in a 3 x 2 grid (cell 341 x 768), read left to right, top to bottom.
In every cell the character is the same size (about 125 pixels tall on the sprite's own pixel grid, each sprite pixel
drawn as a crisp 6 x 6 square), centred horizontally, feet on the same baseline near the bottom of the cell.
Side three-quarter view walking toward the viewer's right, walking in place (she does not travel across the cell).
Hard edges only: no anti-aliasing, no blur, no gradients, no dithering noise. Transparent background.
No grid lines, no cell borders, no numbers, no labels, no text, no ground, no shadow, no motion lines, no extra characters.

LEGS — follow attached image 2 exactly, cell by cell (dark navy = her NEAR leg, the one closer to the viewer;
grey = her FAR leg). Do not copy image 2's shapes or colours, only where each leg and foot is:
frame 1 = contact: NEAR leg reaches forward, heel down; FAR leg stretched back, only its toe touching.
frame 2 = down: weight on the NEAR leg, knee slightly bent, body 1 pixel lower; FAR foot lifting off behind.
frame 3 = passing: NEAR leg straight under the body; FAR leg swings forward past it with the knee lifted; body 1 pixel higher.
frame 4 = contact, the MIRROR of frame 1: FAR leg reaches forward, heel down; NEAR leg stretched BACK, only its toe touching.
frame 5 = down: weight on the FAR leg; NEAR foot lifting off behind; body 1 pixel lower.
frame 6 = passing: FAR leg straight under the body; NEAR leg swings forward past it with the knee lifted; body 1 pixel higher.
Frames 1 and 4 must look clearly different: in frame 1 the near leg is in front, in frame 4 the near leg is behind.
Arms swing opposite to the legs (near arm back when the near leg is forward). Head height changes by at most 1 sprite pixel
except the rise and fall above. The loop 6 -> 1 must be seamless.

인물 묘사 — alice:

Short dark-brown bob with the bow on the image-left side of the head, cream dress with navy trim and white apron, red and navy card-suit marks, pocket watch at the image-right hip, white stockings with suit marks (the near leg's stocking shows the suit marks most clearly), navy shoes.

인물 묘사 — 손자:

Black hair in a neat high top bun with a gold-and-jade pin and a jade tassel on the image-left side, ink-black layered robe with jade-green and pale gold trim, bamboo-slip shoulder guards and bracers, a dark sash with a jade disc at the image-right hip, a short paneled armour skirt, knee-high black boots.

인물 묘사 — 춘향 (공통의 LEGS 대신 이 줄을 쓴다 — 치마가 다리를 가린다):

Long dark-brown hair with a red flower pin, one long braid falling over the image-right shoulder, long red ribbons, a rose-pink jeogori with a big red bow tie and a jade pendant, a full layered rose and white chima skirt reaching the ankles, small red shoes.
LEGS: her legs are hidden by the long skirt — follow attached image 2 only for where the two small red shoes are and how the skirt front moves:
frame 1 = NEAR shoe forward peeking out in front of the hem, FAR shoe behind (only its toe showing at the back of the hem); the skirt front pushes forward;
frame 2 = shoes close, skirt settles, body 1 pixel lower; frame 3 = FAR shoe swinging forward under the hem, body 1 pixel higher;
frame 4 = the MIRROR of frame 1: FAR shoe forward in front of the hem, NEAR shoe behind; frame 5 = shoes close, body 1 pixel lower;
frame 6 = NEAR shoe swinging forward under the hem, body 1 pixel higher. Frames 1 and 4 must clearly show a different shoe in front.
The hem and braid sway opposite to the forward shoe. The loop 6 -> 1 must be seamless.

끝나면 알려줄 것 (시트마다):
- 원본 파일 (PNG, 받은 그대로) — <인물>_begin_walk_gen2.png
- 실제로 쓴 프롬프트 (바꾼 게 있으면 무엇을 왜, 이어 요청을 했으면 그 문구 그대로)
- 첨부한 그림 세 장이 맞는지
- 생성 시각, 작업 ID가 있으면 그대로
- 배경이 투명인지
