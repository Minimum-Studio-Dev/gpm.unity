# Release notes

🌏 [English](ReleaseNotes.en.md)

## v1.0.0

### Date

* 2022.08.25

### Added
* 캐싱 유효기간에 따른 백그라운드 자동 삭제 지원
* CacheControl 기능 지원
* CacheResult text, json 변환 기능 추가
* 만료, 설정된 재요청 시간이 안되었을 경우 Request 타입 추가
    * ALWAYS : 서버에 지속적으로 캐시 확인
    * FIRSTPLAY : 실행 중 1번만 서버에 캐시 확인 요청
    * ONCE : 1회 요청 후 로컬 데이터 사용
    * LOCAL : 로컬 데이터 사용

### Updated
* Common v2.2.2 업데이트
* 캐시 계산 최적화
* 임포트 데이터 최적화
* 재요청 시간 기준 변경(Tick -> 초)

## v0.2.1

### Date

* 2022.07.08

### Updated
* Common 2.1.0을 2.1.2로 업데이트

## v0.2.0

### Date

* 2022.06.28

### Added
* 최대 용량 설정 기능 추가
* 최대 개수 설정 기능 추가
* 웹 캐시 재요청 주기 설정 기능 추가
* 캐시 제거 우선순위 정렬 추가
    1. 만료된 것
    2. 접근한지 1달 지난 것
    3. 접근한지 1주 지난 것
    4. 생성된 파일 index
* 샘플 추가
* API 추가
    * SetMaxCount, GetMaxCount
    * SetMaxSize, GetMaxSize
    * SetReRequestTime, GetReRequestTime

## 0.1.0

### Date

* 2022.05.30

### Features

* Http Cache
* Local Cache
* CachedTexture