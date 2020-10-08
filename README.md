# 깃허브에 대한 정보 정리

분명히 강좌 들을 때 열심히 썼는데도... 몇 달 안 썼더니 다 까먹어서 허탈하다...

다음에는 까먹지 않기 위해 정리하려고 한다.



# 깃허브 시작하기

0. [깃허브](https://github.com)에 가입한다.

1. Repository를 만든다.

2. 로컬 저장소를 만들기 위해 내 컴퓨터에 깃허브 관련 폴더를 만든다.

3. 그 안에 Repository를 담을 폴더를 만든다 (폴더 안에 바로 모든 파일들이 쌓이므로 꼭! Repository별로 폴더를 만든다). 이 폴더가 Working directory가 된다.

4. 해당 폴더 안에 들어가서 Git Bash를 실행한다.

5. 깃허브 계정을 연동하기 위한 준비단계로, 닉네임과 이메일을 등록한다. 전에는 닉네임과 이메일을 무조건 깃허브 계정과 동일하게 해야하는 줄 알았는데, 테스트해보니 다른 닉네임/이메일이어도 괜찮았다. 그래서 나는 기기별로 다른 닉네임을 설정해두었다. 근데 사용자 이메일은 github에 등록된 이메일로 설정하는 것을 추천한다고 전에 강사 선생님께서 말씀하셨다.

   ```bash
   git config --global user.name "닉네임"
   git config --global user.email "이메일"
   ```

6. 이제 해당 폴더 (=working directory) 를 깃 저장소로 만든다.

   ```bash
   git init
   ```

7. 원격 저장소와 연결해준다.

   ```bash
   git remote add origin https://github.com/jiuney/GitHowTos.git
   ```

   이 명령어는 처음에만 쓰면 되고 나중엔 안해도 된다고 한다.

8. 주의! 만약 기존에 있던, 안에 뭐라도 들어있는 repository를 연결했으면 일단 무조건 `pull`부터 한다. 무조건. 그래야 이미 뭔가 있는 내 repository를 로컬에 저장할때든 아니면 다른 사람 깃을 clone할때든 헷갈려서 말아먹지 않는다. 만약 진짜 아무것도, README고 뭐고 아무것도 없는 텅 빈 repository를 새로 만든거라면 이 과정을 생략한다 (명령어 써봤자 오류가 난다: "fatal: couldn't find remote ref master")

   ```bash
   git pull origin master
   ```

9. 이제 로컬 working directory에서 작업을 한다. 나는 일단 이 README.md를 작성했다.

10. 작성한 파일을 업로드하려고 한다. 우선 `git add`를 통해 작업한 내역들 (=변경사항들) 을 `staging area`로 보낸다.

11. `git commit -m "message"`를 통해 `staging area`에 있던 작업내역들을 `local repository`로 보낸다. 즉 이 명령어는 commit도 하고, 해당 commit에 대한 설명도 덧붙이는 것이다.

    ```bash
    git commit -m "201008 Getting started with Git"
    ```

12. 

