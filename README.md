# Discord에 깃허브 웹 훅(Web Hook) 연결하기
멋쟁이사자 FE 중간 프로젝트 대비 깃허브 사용법 특강 테스트 레파지토리입니다.
깃훅과 디스코드를 연결 시키는 과정을 설명합니다.

## 디스코드에서 할 일
1. 원하는 디스코드 채팅 채널의 "설정 ➡️ 연동"에 들어가 웹후크 만들기를 선택합니다.
2. 웹 후크를 만들고 원하는 웹후크 이름, 사진(선택 사항)을 셋팅 한 뒤 웹후크 URL 복사 버튼을 클릭합니다.


## 깃허브에서 할 일
1. 연결시킬(알람을 받을 프로젝트 폴더의 'settings'를 누른 후, webhooks에 들어갑니다.
2. webhooks의 'Add webHook' 버튼을 클릭 후, 복사해두었던 디스코드의 웹후크 URL를 'Payload URL'항목에 붙여넣기 합니다.
3. (중요!) 복사한 URL뒤에 '/gitbub'를 꼭 추가해서 넣어줍니다. 예) 복사한URL/github
4. 하위 설정은 아래를 추천합니다.
   <br /> **Content type** ➡️ application/json,
   <br /> **Secret** ➡️ 공란으로 두세요.
   <br /> **Which events would you like to trigger this webhook?**
   <br />➡️ **Send me everything**: push 이벤트 이외의 PR 리뷰 등을 포함한 모든 깃 허브 알림 ( 💛 처음이시면 이걸 추천드려요)
   <br />➡️ **Let me select individual events**: 알림받고 싶은 것을 체크
   <br /> **SSL verification와 Active 항목**은 원래 기본 셋팅대로 두세요.
5. Add Web Hook를 누르면 끝! 이제 테스트 이슈를 작성해보시고 해당 채널에 알림이 잘 뜨는지 확인해봅시다.

