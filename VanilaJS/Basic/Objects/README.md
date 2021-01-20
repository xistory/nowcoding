## Objects

1. users는 객체들로 이루어진 배열입니다. 각각의 객체는 유저의 계정 하나를 뜻합니다.   
signUp 함수를 만들어보세요. 입력값으로는 _id, username, email, password(문자열)를 받습니다.   
signUp이 실행되면 users에 해당 객체가 추가됩니다. email을 기준으로 검사해서 이미 존재하는 email이면 가입을 거절하는 메세지를 띄워주세요.      

2. signIn 함수를 만들어보세요. 입력값으로 _id, password를 받습니다.   
users 안에 해당 계정이 있는지 확인해서 있으면 그 계정의 isLoggedIn 프로퍼티를 true로 고쳐줍니다.   
계정이 없으면 로그인을 거절하는 메세지를 띄워주세요.   

3. products에는 3개의 제품에 대한 정보가 담겨있습니다. users와 마찬가지로 객체들로 이루어진 배열입니다.   
rateProduct 함수를 만들어보세요. 입력값으로 _id, rate, userId을 받습니다.   
rateProduct가 실행되면 해당 제품의 ratings에 입력받은 rating을 추가합니다.   

4. averageRating 함수를 만들어보세요. 입력값으로 name(제품이름)을 받습니다.   
averageRating이 실행되면 ratings 프로퍼티에 있는 모든 rating들의 평균을 내서 출력해줍니다.   