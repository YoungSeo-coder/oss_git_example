## Week 1-1 강의 개요 (강의계획서)
> 강의내용  
> 1. 오픈소스소프트웨어  
> 2. git  
> 3. Haskell

## Week1-2 오픈소스소프트웨어 개요

1. 오픈소스란?
   - 정의 : 저작권자가 소스코드를 공개하여 누구나 사용, 복제, 수정, 배포할 권리를 부여한 SW
   - 효과 : 협업&자동화 도구 주심의 개발 문화 확산
   - OSS License : 오픈소스SW 권한의 범위를 지정
   - 철학 : 자유와 개방의 융합, 라이선스 준수는 필수이며 단순 무료는 아님.
2. OSS License 유형별 대표 특징
   - **MIT** : 상용 SW와의 연동이 자유롭고, 수정 코드 공개 의무가 없음
   - **GPL** : 수정,배포 시 소스코드 공개 필수 (강한 공유 규약)
   - **Apache** : 특허 보호 조항 포함, 기업 친화적

> **참고자료**  
> [만화로 나누는 자유/오픈소스소프트웨어 이야기](https://joone.net)

## Week2-1 버전 관리 개요

1. VCS  
   - 정의 : 파일 변경 이력을 추적하고, 이전 버전으로 복구할 수 있게 하는 시스템
   - 역할 : 코드 백업, 이력 관리, 협업 지원
   - 종류 : 중앙 집중식, 분산형(Git 등)

2. 기본 동작
   | 개념 | 설명 | Git 명령어 |  
   |------|------|-------------|  
   | **Check-in** | 수정 내용을 저장소에 기록 | `git commit` |  
   | **Check-out** | 저장소의 파일을 가져와 수정 | `git pull` |  
   | **Diff** | 변경 내용 비교 | `git diff` |  
   | **Branch** | 독립적인 작업 공간 생성 | `git branch` |  
   | **Merge** | 분기된 내용을 병합 | `git merge` |  
   | **Tag** | 중요 버전에 이름표 부여 | `git tag` |

3. 분산형 VCS(DVCS)의 추가 기능
- push : 로컬 변경사항을 원격 저장소로 전송
- pull : 원격 저장소의 변경사항을 로컬로 가져옴
  
> **참고자료**  
> [vcs](https://betterexplained.com/articles/a-visual-guide-to-version-control/)  

## Week2-2 Git

1. Git 개요
   - **특징**: 분산형 버전관리 시스템 (DVCS), 각 개발자가 로컬에 완전한 저장소 복사본을 가짐.
   - **4가지 관리 영역**
     - **Workspace (Working Directory)**: 현재 작업 중인 파일이 있는 directory  
     - **Index (Stage)**: 다음 커밋에 포함될 파일(스테이징 영역)  
     - **Local Repository**: 로컬에 있는 저장소, 버전 관리가 이루어짐  
     - **Remote Repository**: 원격 저장소(GitHub 등), 협업

2. Git 기본 Workflow
- 원격 저장소 복제 -> 파일 수정 -> 스테이징 -> 커밋 -> 푸시  
git clone <repo>     _# 원격 저장소 복제_  
git add <file>       _# 새로운 파일(또는 수정 파일) 스테이징_  
git commit -m "msg"  _# 로컬 저장소에 커밋_
git commit -a -m "수정사항" _#  수정 사항을 한번에 add+commit_
git push             _# 원격 저장소로 업로드_  
git pull             _# 원격 변경사항 병합_

3. 추가 명령어  
git fetch _# 원격 저장소 변경사항만 가져오기_  
git merge <branch> _# 브랜치 병합_  
git diff _# 작업공간과 index 비교_  
git diff HEAD _# 작업공간과 마지막 커밋 비교_

4. GitHub와 협업
   - GitHub : Git 기반 코드 공유 플랫폼, OSS 협업의 핵심 도구
   - 주요 기능
    - fork : 다른 사람의 repo를 내 repo로 복사
    - pull request : 수정 사항을 원본 프로젝트에 반영 요청
    - merge : 검토 후 병합하여 반영
      
> **참고자료** 
> [git](https://nvie.com/posts/a-successful-git-branching-model/)

## Week2-3 Github, fork, pull request

1. fork
   - 정의 : 다른사람의 GitHub repo에서 자신의 repo로 복사하는 과정
   - 특징 : 복사된 repo는 원본과 연결되어 있지만 독립적으로 관리 가능?
2. Pull Request
   - 정의 : 자신의 fork된 repo에서 변경된 내용을 원본 repo에 반영해달라고 요청하는 것
   - 특징 : 코드 검토 후 merge됨

## Week2-4 Git: Advanced topics



## Week3  Markdown

1. 인라인 스타일(글씨의 속성)
- 기울이기, 볼드체  
_이탤릭_  
**볼드**  
**_이탤릭&볼드_**

2. 헤더  
># 헤더1  
>## 헤더2  
>...  
>###### 헤더6  
>#### 헤더에 _이탤릭_섞기 가능  


3. 링크  
[문장](www.google.com) //google site link named 문장  
- 참조 링크, 렌더링 Markdown에 표시되지 않음  
Here's [a link to something else][another place].    
Here's [yet another link][another-link].  
And now back to [the first link][another place].  
  
[another place]: www.github.com  
[another-link]: www.google.com  

4. 이미지 (링크와비슷)  
![문장설명](링크.jpg)  
- 참조 링크, 이미지  
![Black cat][Black]  
![Orange cat][Orange]  
  
[Black]: https://upload.wikimedia.org/wikipedia/commons/a/a3/81_INF_DIV_SSI.jpg  
[Orange]: http://icons.iconarchive.com/icons/google/noto-emoji-animals-nature/256/22221-cat-icon.png
 
5. Blockquotes  
> 인용문  
>  
> 빈 줄에도 >(캐럿) 문자 삽입해야 함께 인용됨  

6. Lists  
* 리스트  
 * 리스트 들여쓰기  
  * 한번 더 들여쓰기

7. 숫자 있는 리스트   
 리스트 단락 안의 문장으로 만들기


8. Paragraphs  
문장뒤에 스페이스바 두번  
하면 같은 문단이어서 줄바꿈은 유지함.  
