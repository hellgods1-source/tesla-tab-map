# 사고수리센터 안내

FOH 고객응대용 단독 HTML입니다.  
**공유는 링크만 보내면 됩니다.** Chrome/Edge에서 바로 열립니다.

https://hellgods1-source.github.io/tesla-tab-map/?v=20260831

로컬에서 볼 때는 `사고수리센터_안내.html` 또는 `index.html`을 브라우저로 엽니다.

## FOH 사용

1. 위 링크를 Chrome/Edge로 엽니다. (OneDrive·Teams 미리보기는 쓰지 않습니다)
2. **고객 위치 주소·지명**을 입력하고 찾기 → 후보를 고르거나, **내 위치**를 켭니다.
3. **가까운 센터 5곳**(100km 이내) → `근처 복사` → 상담 문자에 붙여 넣습니다.
4. 전국이 필요하면 **전국 복사**를 씁니다.

주소 검색만 네트워크가 필요합니다. GPS는 HTTPS(또는 localhost)에서만 동작합니다.

## 공유할 때

링크만 보냅니다.

https://hellgods1-source.github.io/tesla-tab-map/?v=20260831

하지 말 것: OneDrive HTML 미리보기, Teams/메일 내장 뷰어. 스크립트가 막혀 지도가 안 뜹니다.

## 문자에 포함되는 안내

근거리 `근처 복사` 하단에 보험 참고와 공통 푸터가 붙습니다.

```
보험 견인 참고: 기본 10km · EV 특약 100km
※ 특약·상품·횟수에 따라 다릅니다. 가입 약관·보험사에 확인해 주세요.
예약은 해당 센터에 직접 문의해 주세요.
고객지원: 080-617-1399
공식 안내: https://www.tesla.com/ko_kr/support/body-shop-support
```

전국 복사에는 보험 참고를 넣지 않습니다.

## 화면

- PC: 왼쪽 Leaflet 지도(전국 핀), 오른쪽 센터 정보
- 위치 있음: 100km 이내 가까운 5곳. 100km 초과는 근거리 정리에서 제외
- 위치 없음: 시도별 그룹 (복사 버튼 없음)
- 복사 버튼: `근처 복사`, `전국 복사`만
- 전국 복사: 서울, 경기, 인천, 원주, 대전, 대구, 부산, 광주, 김해, 제주 순
- 뱃지: 직영 / 추천 / 공인 (현재 목록은 직영 2 · 공인 19. 추천은 공식 확인 후 넣음)
- 헤더: 버전(제작·배포일) · 목록: 데이터 날짜 · 푸터: 최근 변경 한 줄

## 데이터

- 버전(`APP_VERSION`): **2026.08.31** — 이 HTML 제작·배포일 (헤더)
- 데이터(`DATA_AS_OF`): **2026.08.22** — 센터 목록·좌표 갱신일 (목록)
- 변경 기록(`CHANGELOG`): 푸터에 최근 한 줄
- 출처: 고객지원 안내 문자 병합 21곳. Tesla 공식 로케이터 실시간 연동은 하지 않습니다.
- 지도 핀은 도로 중심선이 아니라 건물(또는 확인된 필지) 기준입니다.

공식 안내: [Tesla 공인 바디샵](https://www.tesla.com/ko_kr/support/body-shop-support)

## 데이터 갱신 체크리스트

1. [tesla.com/ko_KR/support/body-shop-support](https://www.tesla.com/ko_KR/support/body-shop-support) 지도와 대조
2. 신규·폐점·전화·주소·좌표 반영
3. 직영 / 추천(Preferred) / 공인 구분 확인
4. `index.html`(또는 `사고수리센터_안내.html`)의 `SHOPS`와 `shops.csv`를 같이 수정한 뒤 GitHub Pages에 올립니다
5. 센터가 추가되거나 위치가 바뀌면 `DATA_AS_OF`를 그날로 바꾸고 `CHANGELOG` 맨 위에 `{ date, note }`를 넣는다
6. 화면·기능만 바뀌면 `APP_VERSION`을 그날로 바꾼다
7. 헤더 버전과 목록 데이터 날짜가 다르면 업데이트가 반영된 것이다

## GitHub Pages

이 폴더만 공개 저장소로 올립니다. 상위 `매니저 업무` 폴더는 올리지 마세요.  
`index.html`이 앱 본문입니다.
