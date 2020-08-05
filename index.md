##유저
1. 유저 생성
POST: /users

2. 유저 확인
GET: /users/{user_id}

3. 유저 수정
PUT: /users/{user_id}

4. 유저 탈퇴

###user
1. id: String?
2. fcm_token: String
3. uuid: String
4. device_id: String
5. platform_type: String
6. createdDate: LocalDateTime



##캠핑장
1. 캠핑장 목록
GET: /campsites (검색 파라미터 추가 할 것)

###campsite
1. id: Int
2. name: String?
3. address: String?
4. reservationUrl: String?
5. createdDate: LocalDateTime

##구독
1. 구독 목록
GET: /users/{user_id}/subscribed?date=yyyyMMdd

2. 구독 생성
POST: /users/{user_id}/subscribed

3. 구독 정보
GET: /users/{user_id}/subscribed/{id}

4. 구독 삭제
DELETE: /users/{user_id}/subscribed/{id}

###subscribed
1. id: string
2. userId: string
3. campsites: Int
4. date: Date
5. createdDate: LocalDateTime
6. -- 대기 인원 -- => 날짜 선택 시
