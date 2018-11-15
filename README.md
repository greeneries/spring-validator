# spring-validator


##### 고객에게 데이터를 입력받을 때 단계별로 나눠서 처리하는 방법
####### ModelAttribute 사용하는 방법
```
	@ModelAttribute("member") 
	public Member member() {
		return new Member("이름을 입력하세요", "주소를 입력하세요");
	}
```

##### 입력한 데이터 validation 체크하는 방법
```
	public void validate(
			Object target, // 사용자가 작성한 데이터를 보관하는 객체
			Errors errors) { // 데이터를 검증한 결과(에러정보)를 보관하는 객체
		ValidationUtils.rejectIfEmptyOrWhitespace(
				errors, "address", "required.address", "주소가 필요합니다.");
	}
```

<div>
	<img width="200" src="https://user-images.githubusercontent.com/42959261/48530771-a72d1980-e8dc-11e8-80bb-f0fc8bcfda02.JPG">
</div>
