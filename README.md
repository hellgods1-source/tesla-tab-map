# Tesla 공인 바디샵 찾기

고객 문자로 보낼 수 있는 모바일 지도 페이지입니다.  
휴대폰에서 열면 직영 사고수리센터·공인 바디샵 21곳이 지도에 표시되고, **내 위치**를 켜면 가까운 순으로 정렬됩니다.

공개 페이지: https://hellgods1-source.github.io/tesla-tab-map/

## 문자 문구 예시

```
안녕하세요, Tesla 고객지원팀입니다.

사고 수리 시 가까운 Tesla 직영 사고수리센터 및 공인 바디샵을 지도에서 확인하실 수 있습니다.

[Tesla 공인 바디샵 찾기]
https://hellgods1-source.github.io/tesla-tab-map/

기타 문의: 080-617-1399
감사합니다.
Tesla Korea
```

## GitHub Pages 배포

이 폴더만 공개 저장소로 올립니다. (상위 `매니저 업무` 폴더는 올리지 마세요.)

```bash
cd tesla-tab-map
git init -b main
git add index.html README.md
git commit -m "Add Tesla authorized body shop locator"
gh repo create tesla-tab-map --public --source=. --remote=origin --push
gh api -X POST repos/hellgods1-source/tesla-tab-map/pages -f "build_type=legacy" -f "source[branch]=main" -f "source[path]=/"
```

또는 GitHub 웹: Settings → Pages → Branch `main` / folder `/ (root)` → Save.

수 분 후 https://hellgods1-source.github.io/tesla-tab-map/ 가 열립니다. 위치 권한은 HTTPS에서만 동작합니다.

## 데이터

센터 목록은 고객지원 안내 문자 2통을 병합·중복 제거한 21곳입니다.  
좌표는 도로명 주소를 OpenStreetMap Nominatim 기준으로 넣었습니다.

공식 안내: [Tesla 공인 바디샵](https://www.tesla.com/ko_kr/support/body-shop-support)
