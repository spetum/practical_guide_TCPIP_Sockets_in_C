2016.09.02(Friday) 06:07AM
LengthFramer.c 와 DelimFramer.c는 병행해서 쓸 수 있다.
LengthFramer.c는 길이를 기반으로 하는 프레임을 사용하는 반면
DelimFramer.c는 구분자를 기반으로 하는 프레임을 사용한다는 차이점이 있다.
Text방식과 Binary방식은 서로 같은 프레임 처리를 사용해야 한다.

예를 들어 Text방식의 "서버"는 DelimFramer.c를 사용하고 "클라이언트"는 
LengthFramer.c를 쓴다면 당장에 에러가 없는 내용이지만 알 수 없는 버그가 존재할 수 
있다.

