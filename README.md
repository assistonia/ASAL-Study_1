# Github Study Project (Use Git Bash)
깃허브를 익히고 실습을 통해 공부해보기<br>
# 용어 정리
 * Git : 버전 관리 시스템
 * GitHub : Git으로 관리하는 프로젝트를 올려둘 수 있는 사이트
 * Git Bash : CLI 방식으로 Git을 사용할 수 있는 환경
 * 커밋 : 버전 관리를 통해 생성된 파일, 혹은 그 행위
 * log : 지금까지 만든 커밋의 기록
 * checkout : 원하는 지점으로 이동
 * 로컬저장소 : Git으로 버전 관리하는 내 컴퓨터 안 폴더
 * 원격저장소(레포지토리) : GitHub에서 협업하는 공간(폴더)
 * push : 로컬저장소의 커밋을 원격저장소에 올리는 행위
 * pull : 원격저장소의 커밋을 로컬저장소에 내려받는 행위
# ※ 사전 작업
  * git 다운로드
  * 마우스 우클릭 후 원하는 폴더에 git bash here 클릭<br>
  ![image](https://user-images.githubusercontent.com/88313282/148160155-3c9e93fd-61a7-4b7c-b300-2011e87a84c9.png)
# 1. 계정 설정하기
본인의 닉네임과 이메일을 다음 명령어를 통해 등록하여 준다. (버전 관리를 누가 했는지 알아야 하기 때문)
```swift
git config --global user.name "your name"
git config --global user.email "your Email"

```
![image](https://user-images.githubusercontent.com/88313282/148159261-09a7c172-5d71-419e-bdaf-082da465956d.png)

# 2. git clone
내 컴퓨터 로컬저장소에 파일을 내려받기 위해 다음 명령어를 통해 파일을 받아준다.
```swift
https://github.com/AISL-Study/Git_Study_1.git

```
<br>
원격저장소의 주소는 레포지토리 우측 상단에 code를 클릭하면 파일을 받을 수 있는 주소가 나타나게 된다.<br>

![image](https://user-images.githubusercontent.com/88313282/148161025-9d286fb3-9616-4aa8-be19-8e89a1ea6532.png)<br>

![image](https://user-images.githubusercontent.com/88313282/148161599-6a82b9ba-ee50-4b41-a246-454659368d8f.png)

![image](https://user-images.githubusercontent.com/88313282/148161817-3424239f-af8f-4052-990d-9cc971ebfbc1.png)

# 3. 원격저장소 주소 확인
원격 저장소 설정이 됐는지 확인하는 명령어.<br>
origin는 원격 저장소의 주소를 말하며
즉, 현재 clone을 통해 가져온 레포지토리가 내 로컬 레포지토리에 복사가 되었고 그 원격 저장소의 주소를 확인할 수 있다. 
```swift
git remote -v

```
![image](https://user-images.githubusercontent.com/88313282/148161979-790f1f04-871c-4b67-a033-7c07c60c056f.png)

# 4. Branch 생성
자신의 로컬 환경에서 코드를 추가하는 작업을 하기 위해 브랜치를 만들어준다.

```swift
git checkout -b 브랜치 이름
```
※ 브랜치 이름은 본인 영문 이름으로 할 것. (누가 코드를 추가했는지를 확인하기 위해서)

# 5. 코드 수정하기
index.html 파일을 수정해준다.<br>
본인의 이름과 학번을 적어서 수정 후 저장할 것.<br>
<img src="https://user-images.githubusercontent.com/88313282/148162543-b294b94d-6f11-42c9-a07a-1d0905254354.png"  width="400" height="200">

※ html 파일을 수정하는 방법은 구글링을 통해 직접 해보시면 됩니다.

# 6. 깃허브 작업하기
파일을 수정했다면, github의 원격저장소에 작업하는 과정이 필요합니다.<br>
다음 세개의 명령어를 통해 깃허브 작업을 할 수 있습니다.
1. git add
```swift
git add .
```
   > 현재 로컬 레포지토리에 수정한 모든 내용을 추가해준다.

2. git commit
```swift
git commit -m "메시지 내용"
```
   > 커밋은 수정한 내용을 알림 

3. git push
```swift
git push origin 브랜치 이름
```
   > 원격 저장소에 내 브랜치로 수정한 내용을 push

# 7. 브랜치 삭제
```swift
git pull origin master
```
> 원본 저장소에 merge가 완료되면 원본 저장소와 로컬 저장소의 코드를 동기화
```swift
git branch -d 브랜치 이름
```
> 작업하던 로컬의 브랜치를 삭제


