# 키친포스

## 요구 사항
### 메뉴그룹
- 메뉴 그룹을 등록한다.
    - [ ] 메뉴 그룹의 이름이 null 또는 빈 값인 경우 등록할 수 없다.
    - [ ] 메뉴 그룹의 등록 할 때 동일한 이름으로 등록 할 수 있다.
- 전체 메뉴 그룹을 조회한다.
### 메뉴
- 메뉴를 등록한다.
    - [ ] 메뉴 등록의 필수 값은 금액, 메뉴 그룹 ID, 메뉴 상품 값은 필수 값이다.
    - [ ] 가격은 null이나 음수 값이면 안된다.
    - [ ] 등록된 메뉴 그룹만 사용할 수 있다.
    - [ ] 메뉴에 등록되는 상품은 이미 등록된 상품만 사용할 수 있다.
    - [ ] 메뉴의 가격은 구성 상품의 가격 * 수량을 넘을 수 없다.
    - [ ] 메뉴명은 null 또는 비속어는 등록 할 수 없다.
- 메뉴 가격을 변경한다.
    - [ ] 가격은 null이나 음수 값이면 안된다.
    - [ ] 메뉴의 가격은 구성 상품의 가격 * 수량을 넘을 수 없다.
- 메뉴를 노출한다.
    - [ ] 메뉴의 가격은 개별 구성 상품의 가격 * 수량 보다 커야한다.
    - [ ] 메뉴의 노출 상태를 노출 처리한다.
- 메뉴를 숨긴다.
    - [ ] 메뉴의 노출 상태를 숨김 처리한다.
- 전체 메뉴를 조회한다.
### 주문
- 주문을 등록한다.
    - [ ] 주문타입은 필수 값이다.
    - [ ] 하나 이상의 매뉴를 주문 해야한다.
    - [ ] 매장주문이 아닌 경우 메뉴당 하나 이상 주문 해야한다.
    - [ ] 등록된 메뉴만 주문이 가능하다.
    - [ ] 메뉴의 노출 상태가 노출중인 상품만 주문 가능하다
    - [ ] 메뉴의 가격과 주문 목록의 가격이 일치해야한다.
    - [ ] 주문의 최초 상태는 주문대기이다.
    - [ ] 배달주문인 경우 배달지 주소는 필수 값이다.
    - [ ] 매장주문인 경우 테이블 번호는 필수 이며 테이블에 먼저 온 손님 이 있는 경우 주문이 되지 않는다.
- 주문을 수락한다.
    - [ ] 등록된 주문상태가 주문대기인 경우에만 유효한 값이다.
    - [ ] 주문타입이 배달주문인 경우 배달 라이더에게 요청을 보내기 위해 주문 ID, 주문 총 가격, 배달 주소를 넘겨준다.
    - [ ] 주문상태를 주문수락으로 변경한다.
- 주문을 제공한다.
    - [ ] 등록된 주문상태가 주문수락인 경우에만 유효한 값이다.
    - [ ] 주문상태를 주문제공으로 변경한다.
- 주문 배달 시작한다.
    - [ ] 등록된 주문의 타입 배달주문이며 주문상태가 주문제공 경우에 주문 상태를 배달중으로 변경한다.
- 주문 배달 완료한다.
    - [ ] 등록된 주문의 타입 배달주문이며 주문상태가 배달인 경우에 주문 상태를 배달완료으로 변경한다.
- 주문 완료 처리한다.
    - [ ] 조회된 주문이 등록된 주문이어야 한다.
    - [ ] 주문 타입이 배달주문인 경우 주문상태가 배달완료여야 한다.
    - [ ] 주문 타입이 포장주문 또는 매장주문인 경우 주문 상태가 주문제공이어야 한다.
    - [ ] 주문상태를 주문완료로 변경한다.
    - [ ] 매장주문인 경우 매장 테이블을 비어준다.
- 전체 주문을 조회한다.
### 주문 테이블
- 테이블을 추가한다.
    - [ ] 테이블 이름은 한 글자 이살이어야 한다.
    - [ ] 테이블을 만들 때 손님은 0명 비어있는 상태로 만든다.
- 테이블에 앉는다.
    - [ ] 등록된 테이블만 데이터가 변경 가능하다.
    - [ ] 테이블에 비어있음의 여부를 사용중으로 변경한다.
- 테이블을 정리한다.
    - [ ] 등록된 테이블만 데이터가 변경 가능하다.
    - [ ] 정리할 태이블에서 손님이 식사를 마쳐야지만 테이블을 정리할 수 있다.
    - [ ] 테이블에 비어있음의 여부를 비어있음으로 변경하고 테이블에 앉아있는 손님의 수를 0명으로 수정한다.
- 테이블에 앉은 손님 수를 기록한다.
    - [ ] 손님의 수는 0보다 커야 한다.
    - [ ] 등록된 테이블만 데이터가 변경 가능하다.
    - [ ] 비어있는 테이블에는 손님이 앉을 수 없다.
    - [ ] 손님의 수를 기록한다.
- 전체 테이블을 조회한다.
### 상품
- 상품을 등록한다.
    - [ ] 상품의 가격은 0보다 커야한다.
    - [ ] 상품의 이름은 한 글자 이상이어야 한다.
- 상품의 가격을 수정한다.
    - [ ] 상품의 가경은 0보다 커야 한다.
    - [ ] 등록된 상품의 가격만 수정가능 하다.
    - [ ] 상품이 포함된 메뉴를 조회해서 상품이 속한 메뉴의 가격 * 수량의 총합이 메뉴가격 보다 크면, 메뉴를 숨김처리 한다.
- 전체 상품 조회한다.
## 용어 사전
| 한글명 | 영문명 | 설명 |
| --- | --- | --- |
| 배달주문 | DELIVERY | 상품을 배달라이더를 통해 전달하는 주문 형태 |
| 포장주문 | TAKEOUT | 손님이 준비된 메뉴를 수령하가는 주문 형태 |
| 매장주문 | EAT_IN | 손님이 매장 테이블에서 취식을 하는 주문 형태 |
| 주문대기 | WAITING | 손님이 주문을 완료한 상태 |
| 주문수락 | ACCEPTED | 주문한 메뉴를 매장에서 인지한 상태 |
| 주문제공 | SERVED | 메뉴가 준비되어서 전달 할 수 있는 상태 |
| 배달중 | DELIVERING | 준비된 메뉴가 손님에게 배달되는 상태 |
| 배달완료 | DELIVERED | 배달 라이더가 손님에게 음식을 전달한 상태 |
| 주문완료 | COMPLETED | 손님이 주문한 메뉴를 받은 상태 |
## 모델링
