## validation 분리
* 기존 validation 로직을 따로 분리
* Spring에서 제공하는 Validator 사용
* support, validate 메소드 지원
* support는 해당 클래스를 지원하는지 확인
* validate는 검증로직 작성
* @Validated 을 컨트롤러 파라미터 앞에 붙여 간편히 사용가능
* 애플리케이션 클래스에 getValidator() 메소드를 통해 모든 컨트롤러에서도 사용가능

## Bean Validation
* Item클래스의 변수들에 에노테이션을 붙여 검증을 수행
* 더욱 간소화하여 검증수행
* javax validator, 하이버네이트 validator를 사용
