

# Python으로 Telegram 챗봇

* Python을 선택한 이유

여러가지 새로운 라이브러리를 빠르게 쓸수 있다는 장점

python라이브러리가 가장 빠르게 발전

추후 분석툴로 python이 가장 쓰기 좋음



# 1. Telegram Bot을 생성한다.

 t.me/BotFather 로 들어간다.
 
/newbot 명령어로 새로운 봇을 만든다.


Alright, a new bot. How are we going to call it? Please choose a name for your bot.

username 입력

yonhee

봇의 이름을 만든다. 

yonheebot


Acceess Token을 return하여 주는데, 그것을 잘 기록해 두어야 한다. 

Done! Congratulations on your new bot. You will find it at t.me/yonheebot. You can now add a description, about section and profile picture for your bot, see /help for a list of commands. By the way, when you've finished creating your cool bot, ping our Bot Support if you want a better username for it. Just make sure the bot is fully operational before you do this.

Use this token to access the HTTP API:
584425783:AAHGuTBzmCad_vnjiSoeZvKdN94LM52Uru8

For a description of the Bot API, see this page: https://core.telegram.org/bots/api

# 2. chatbot 연결


챗봇 호스팅 서비스 BotHub.Studio 회원 가입 후 아래와 같이 CLI 도구를 설치합니다.



`pip install bothub-cli`

계정 연결을 위해 configure 을 실행합니다.

`bothub configure`

bothub에서 회원가입한, 

username과 비밀번호를 입력합니다. 

프로젝트 폴더를 생성합니다.

```
mkdir MyBot
cd MyBot
bothub init
```


기본 코드인 bot.py 에는 유저의 메시지를 그대로 따라하는 EchoBot 코드가 들어 있습니다.

그럼 실제 실행을 위해 위에서 생성한 텔레그램 Access Token을 연결합니다.

```
bothub channel add telegram --api-key=<Access Token>
```


API KEY에 Access Token을 입력하실땐 화살괄호 <>를 포함하지 않고 넣으셔야 합니다.

이제 서버로 프로젝트를 업로드 합니다.

`bothub deploy`

이제 텔레그램에서 챗봇이 잘 동작하는지 확인해 보면 됩니다.

자신의 챗봇은 @username 으로 검색하거나 t.me/<username> 을 통해서 접속할 수 있습니다.






References

http://aidev.co.kr/index.php?&mid=chatbotdev&search_keyword=python&search_target=title_content&document_srl=1268


http://static.wooridle.net/lectures/chatbot/



https://medium.com/bothub-studio-ko/python%EC%9C%BC%EB%A1%9C-telegram-%EC%B1%97%EB%B4%87-%EC%8B%9C%EC%9E%91%ED%95%98%EA%B8%B0-617f222dd393


