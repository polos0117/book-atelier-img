# book-atelier-img

[book-atelier](https://github.com/polos0117/book-atelier) 의 그림 저장소다. 코드와 그림을 처음부터 나눠 둔다 —
Pages 사이트 하나는 1 GB 까지라, 차면 pkm-atelier 처럼 `book-atelier-img-2` 를 더한다.

```
img/<파일>.webp        원본. 1024×1536 (2:3)
img/thumb/<같은 이름>   목록용. 긴 변 512 — 워크플로가 만든다(엔진을 옮길 때 붙인다)
```

파일 이름 규칙·썸네일·자동 등록은 엔진(pkm-atelier 에서 가져옴)과 함께 정한다. 그 전까지 시범 그림은 `pilot/` 에 둔다.
`.nojekyll` 은 Pages 가 파일을 있는 그대로 내보내게 한다.
