## validation 분리
* 기존 validation 로직을 따로 분리
* Spring에서 제공하는 Validator 사용
* support, validate 메소드 지원
* support는 해당 클래스를 지원하는지 확인
* validate는 검증로직 작성
* @Validated 을 컨트롤러 파라미터 앞에 붙여 간편히 사용가능
* 애플리케이션 클래스에 getValidator() 메소드를 통해 모든 컨트롤러에서도 사용가능

## Bean Validation 시작
* Item클래스의 변수들에 에노테이션을 붙여 검증을 수행
* 더욱 간소화하여 검증수행
* javax validator, 하이버네이트 validator를 사용

## Bean Validation 스프링 적용
* 스프링 validation 패키지를 implmentaion하면 저절로  
* @Valid 등을 붙인 부분에 대해서 Global Validation이 동작

## Bean Validation 에러 코드
* properties에 등록하여 에러 메시지 사용 가능

## Bean Validation 오브젝트 오류
* ScriptAssert를 통해 체크 가능
* 그보다는 기존 ItemValidator의 자바 코드를 고치는 것이 좋음

## Bean Validation groups
* 상황에 따른 Bean Validation적용을 달리 할 수 있음
* @Validation(groups = SaveCheck.class) 와 같이 적용

## Form 전송 객체 분리 소개
* 요청 -> Item -> controller -> Item -> 응답 (지금까지 한 경우)
* 요청 -> Form -> controller -> Item 새로 생성 -> 응답 (Form 으로 받을 경우)
* Form을 통해 데이터를 받을 경우 검증시, groups를 사용하지 않아도 된다.