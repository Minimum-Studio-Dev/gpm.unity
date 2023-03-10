# Release notes

🌏 [English](ReleaseNotes.en.md)

## 1.1.0

### Date

* 2023.03.10

### Added
* CacheStorage 뷰어 툴 추가
* RequestTexture RequestType 넣을 수 있도록 함수 추가
* RequestTexture preload 추가

### Updated
* NotModified 코드 발생 시에도 유효기간 정보 갱신하도록 개선
* maxCount 기본값 10000 설정
* maxSize 기본값 256MB 설정
* 캐시 다시 받을 때도 내부적으로 같은 데이터이면 데이터 유지하도록 개선

### Fixed
* LastModified 값이 0일때 읽지 못하던 버그 수정
* ReRequest 시간 설정 시 계산 잘못하던 문제 수정
* 캐시 새로 받을 때 용량 계산 잘못하던 문제 수정
* ios에서 폴더 변경으로 인한 접근 권한 문제 수정
* 동시에 Request 할 때 callback 받을 수 있도록 수정
* StringToValue null 값 들어가도 정상 동작하도록 수정
* Size 제한으로 삭제 시 자동 삭제 중인 캐시도 계산하도록 수정

## 1.0.1

### Date

* 2022.10.13

### Fixed
* 샘플에서 로컬 파일 읽기 버튼 연결 잘못된 버그 수정
* http 통신 시 마지막 수성 날짜 포맷 안 맞는 버그 수정

## 1.0.0

### Date

* 2022.08.26

### Added
* 캐싱 유효기간에 따른 백그라운드 자동 삭제 지원
* CacheControl 기능 지원
* CacheResult text, json 변환 기능 추가
* 만료, 설정된 재요청 시간이 안되었을 경우 Request 타입 추가
    * ALWAYS : 요청할 때마다 서버에 데이터가 바뀌었는지 검증
    * FIRSTPLAY :  앱 실행 후 처음 요청할 때마다 서버에 검증
    * ONCE : 최초 요청 이후 서버에 검증하지 않고 캐시 된 데이터를 사용
    * LOCAL : 캐시 된 데이터를 사용합니다.

### Updated
* Unity Guidelines의 1.3.a Versions of Unity 내용에 따라 최소 버전을 2019.4로 상향합니다.
    * 참조 : [Unity Guidelines](https://assetstore.unity.com/publishing/submission-guidelines)

* Common v2.2.2 업데이트
* 캐시 계산 최적화
* 임포트 데이터 최적화
* 재요청 시간 기준 변경(Tick -> 초)

## 0.2.1

### Date

* 2022.07.08

### Updated
* Common 2.1.0을 2.1.2로 업데이트

## 0.2.0

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