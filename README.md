# book-atelier-img

[book-atelier](https://github.com/polos0117/book-atelier) 의 그림 저장소다. 코드와 그림을 처음부터 나눠 둔다 —
Pages 사이트 하나는 1 GB 까지라, 차면 pkm-atelier 처럼 `book-atelier-img-2` 를 더한다(썸네일 워크플로가 900 MB 에서 알린다).

```
img/<파일>.webp          원본. 1024×1536 (2:3)
img/thumb/<같은 이름>     목록용. 긴 변 512 — 워크플로가 만든다
records/<책>/<자리>-ui.json   생성기의 "기록 내보내기" — 어느 화풍·판·설정으로 만들었나
pilot/                   화풍 참고 그림·시범 그림(등록하지 않는다)
```

파일 이름은 코드 저장소의 [IMAGE_RULES.md](https://github.com/polos0117/book-atelier/blob/main/IMAGE_RULES.md) 3절이 정본이다.

```
<책>_<폼>_<화풍>_f.webp          폼 초상 — 폼은 begin(발단) · middle(전개) · end(결말)
<책>_<폼>_open_<화풍>_f.webp     그 폼의 개방
<책>_<화풍>_f_casual3.webp       일상컷
```

올리면 `.github/workflows/thumbs.yml` 이 썸네일을 만들고, 비밀 `CODE_REPO_TOKEN`(book-atelier 하나에 Contents: Read and write 인
fine-grained 토큰)이 있으면 코드 저장소의 "그림 등록" 을 깨워 `data/img.json` 에 적게 한다. 토큰이 없으면 코드 저장소가 매시 시간표로 등록한다.
`.nojekyll` 은 Pages 가 파일을 있는 그대로 내보내게 한다.

## 공간 배경

`backgrounds/`는 서가 화면의 공간 배경이다. 인물 도감 등록 대상인 `img/`와 분리한다. `sunlit-library.webp`(1536×1024)는 데스크톱, `sunlit-library-small.webp`(800×533)는 모바일에서 쓴다. 생성 기록은 `records/backgrounds/`에 둔다.
