# 07/10 번역 리뷰

R팀 (Ryan) 최연호(drunkencoding)

## 1. Review 내용들

-   [Chapter 5:Filling in Layout -> `./filling-in-layout_drunkencoding.pdf`](filling-in-layout_drunkencoding.pdf)

## 2. Review 를 진행하며 책의 내용과 무관한 개인적인 소견으로..

1.  다시금 느끼지만.. command 실행 위치 및 pwd 가 드러나 있으면 좋겠네요. command 들이 상대경로로 동작하도록 되어있으니깐요.. 그리고 option 들 역시 full name 으로 적혀있으면 어떤 option 인지 유추하기 좋을 것 같습니다.

2. 책의 초기부분에서 여러 test app 들을 만드는데, 저같은 경우는 새로운 project 를 만들지 않고 그냥 계속 한 project 에서 진행했습니다. 책의 (정석?) 내용에서는 벗어나지만 저같이 진행한 경우에는 db:migrate 가 users 라는 table 이 기존재해서 실패하거든요,

   이런 경우에 해결법으로 sqllite 에 직접 들어가서 drop db 하는 방법이 있는데, 이에 대한 설명도 있으면 어떨까요?
   ```sh
   $ sqlite3 db/development.sqlite3
   sqllite> drop table users;
   sqllite>.quit
   $ bin/rake db:migrate
   ```

