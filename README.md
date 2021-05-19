# Git 주차별 학습 정리

스파르타 Git - 주차별로 학습한 내용을 관리하는 프로젝트이다. 

Table of Contents
-----------------

<!-- vim-markdown-toc GFM -->

* [1주차 학습 정리](#1주차-학습-정리)
  * [앞으로 git 프로젝트로 만들고 싶은 것](#앞으로-git-프로젝트로-만들고-싶은-것)
  * [1주차 주요 개념 키워드 적어보기](#1주차-주요-개념-키워드-적어보기)
  * [windows 에서 Git 관리 폴더 설정하기](#windows-에서-Git-관리-폴더-설정하기)
  * [Windows 에서 삭제하기](#Windows-에서-삭제하기)
  * [원격 repo 사용하기](#원격-repo-사용하기)
  * [Tracking 하기](#Tracking-하기)
  
* [2주차 학습 정리](#2주차-학습-정리)
  * [Issue 할당](#Issue-할당)
  * [Branch 개념](#Branch-개념)
  * [Merge 개념](#Merge-개념)
  * [Merge conflict 개념](#Merge-conflict-개념)
  * [원격 repo 개념](#원격-repo-개념)
  
* [3주차 학습 정리](#3주차-학습-정리)
  * [Using Homebrew](#using-homebrew)
  * [Using git](#using-git)
  * [Using Linux package managers](#using-linux-package-managers)
  * [Windows](#windows)
  * [As Vim plugin](#as-vim-plugin)

1주차 학습 정리
------------
### 앞으로 git 프로젝트로 만들고 싶은 것
- 개발된 소스를 git 으로 버젼관리를 하고 싶다. <br>
- 작성된 문서를 git 으로 관리하고 싶다.<br> 
  ( 현재는 네이버의 포스터로 작성하고 있는데 git 이 더 이점이 있을 것 같다.  )

### 1주차 주요 개념 키워드 적어보기
`
   Q1. Github 은 무엇인가요?<br>
    => 더 이상 이런 파일은 그만! 하나의 파일로도 버전관리를 할 수 있게 도와줘요.<br>
    
   Q2. Git 으로 모든 파일의 내용이 자동 비교가 되나요?
   => 기본 설정으로는 코드(Python, HTML, JavaScript, Java,...) text 파일, markdown파일(text 파일의 일종), CSV 파일 등 이 가능합니다!
   => 이미지 파일, Word 파일, PDF 파일, 엑셀 파일은 여러가지 설정을 해주어야 가능하답니다. 기본 설정으로 이런 파일들은 파일의 크기가 변했구나! 만 알 수 있어요~<br>
 
   Q3. Github 으로 무엇을 할 수 있을까요?
   => Git 과 Github 은 다릅니다!  Github 은 Git 원격 저장소 + Git 으로 할 수 있는 커뮤니티 기능 서비스입니다.<br> 
   => 즉, Github 은 Git 으로 된 프로젝트 저장 공간을 제공하고, Git 편하게 사용하기 위한 여러가지 부가기능을 가지고 있어요.<br> 
      Git 이 협업할 때 필수! 라고 했었죠? Github 에는 협업하기 위한 기능들을 가지고 있어요. 마치 개발자들의 SNS 같답니다.<br> 
   => Github 외에도 Git 프로젝트 저장소 +  프로젝트 관리하는 기능을 제공하는 곳으로는 대표적으로 Gitlab,<br> 
      bitbucket 등의 서비스가 있어요.<br>
   => 프로젝트 함께 만드는데 참여하는 것 즉 '프로젝트에 기여하기(contribution)' 하기 위한 여러 기능도 제공합니다.<br> 
      이 부분 버그(프로그램 오류,오작동)가 있어요!<br> 
      알리고 프로젝트를 개선시키려면 어떤게 필요할까? 토의할 수도 있어요.<br> 
      
   Q4. Git은 버전관리 도구라고 했습니다. commit(커밋) 은 무엇일까?<br>
   => Git 은 commit(커밋) 을 통해 '현재 프로젝트의 상태'을 저장하고 조회합니다.<br>
   => 여러분들이 '파일 저장' 버튼을 누르면 현재 상태의 파일이 저장되는 것처럼 현재 프로젝트의 상태를 저장할 수 있어요. <br>
      정확히는 snapshot(스냅샷) 즉, 찰칵 사진을 찍는 것, 현재 프로젝트의 전체 상태를 포착하는 거에요.<br> 
   => commit 은 현재 프로젝트의 상태를 저장하는 것이라는 것을 기억하세요! 파일의 어떤 부분이 변경되었는지를 저장하는 것이 아니랍니다<br>
`
   
### windows 에서 Git 관리 폴더 설정하기
   1. sourcetree 를 켜고 Create 
   2. 탐색을 누르고 뜨는 화면에서 바탕화면에 만든  kimchi-recipe 클릭하고 '폴더 선택' 버튼을 눌러주세요
   3. 아래처럼 내용이 잘 채워졌다면 '생성을' 눌러주세요
   4. 아래처럼 팝업이 뜨면 예 를 눌러주세요. 놀라지 마세요! 이미 있는 폴더를 git 폴더로 만들 건지 다시 한번 확인하는 것 뿐이에요
   5. 아래처럼 보이면 잘 된 거에요! 
   
### Windows 에서 삭제하기
   1. + 를 눌러서 New Tab 을 열어주세요.<br> 
   2. 삭제하려는 저장소를 선택한 후 우클릭 - 삭제를 누르면 팝업이 뜹니다.<br>
   3. sourcetree 에서만 안 보이게 하려면 북마크를 제거하세요 를<br>
      컴퓨터에서까지 삭제하려면 디스크에 있는 저장소를 삭제하세요 를 눌러주세요.<br>
   4. 디스크에 있는 저장소를 삭제하세요 를 누르면 내 컴퓨터에서도 삭제가 됩니다!<br>  
      git 설정이 꼬여서 git 설정만 처음부터 해보고 싶은 거라면 다음 단계를 참고!<br>   
   5. git 설정이 잘 되지 않아서 프로젝트 파일은 현재 상태 그대로 두고, git 설정만 처음부터 되돌리고 싶은 거라면!
      내 컴퓨터 프로젝트 폴더 내 .git 폴더를 지워주면 됩니다. 
      이 경우, git 프로젝트가 아닌 그냥 일반 프로젝트가 되었다고 생각하면 됩니다. 
      다시 git 프로젝트로 만드는 git 초기화(initialize)부터 해주면 되겠죠?   
   
   Q1.  원격 repo와 로컬 repo 가 뭐예요<br>
   => Git 도 클라우드 서비스로 두 군데의 내용을 동기화한 것처럼 원격 repo와 로컬 repo 를 연결시켜서 내용을 반영시킬 수 있어요.<br> 
      로컬 repo 가 원격 repo 를 연결하는 것을 추적(Tracking, 트랙킹 / branch tracking) 이라고 해요.<br>

   => 로컬 repo 만이 내가 어떤 원격 repo 와 연결되어있는지를 알고 있어요.<br> 
      원격 repo 는 내가 어떤 로컬 repo 와 연결되어있는지 정보를 가지고 있지 않아요.<br> 
      언제나 로컬 repo 를 기준으로 동작을 이해해주세요!<br> 
   => 로컬 repo 를 기준으로 생각하면 되겠죠? 나(로컬 repo)의 내용을 보내주는 거니까 push! 나(로컬 repo)로 내용을 땡겨오는 거니까 pull!<br>  
   => 원격 repo 를 내 컴퓨터에서도 사용할 수 있도록 가져올 수도 있어요. 일종의 초기 다운로드라고 생각하면 됩니다.<br> 
      이걸 clone(클론, 복제) 라고 해요.<br> 
      
### 원격 repo 사용하기
   1. tracking- 로컬 repo 와 원격 repo 연결하기<br>
      원격 repo 가 없으므로 Github 에 원격 repo 를 만들고, 내 컴퓨터에 있는 로컬 repo 와 연결시켜볼게요!<br> 
   2. 원격 repo 만들기<br>  
      github 로그인 후 뜨는 페이지에서 초록색 new 버튼을 눌러서 repo를 만들어보겠습니다<br>
      프로젝트 설명 페이지, 라이센스 등 여러 설정을 할 수 있지만 일단은 가장 간단한 형태로 만들어볼게요!<br> 
      
### Tracking 하기
   [부제] Github 에 있는 repository 와 내 컴퓨터에 만들어놓은 repository 연결하기
   1. Windows 에서 설정하기<br>  
      sourcetree 에 들어가서 kimchi-recipe 창에서 설정 버튼을 눌러주세요<br>
      설정창이 뜨면 원격 -  추가를 누르세요.<br>
      원격 이름 : origin 을 적어주세요. origin 은 원격에 연결하는 저장소를 말할 때 일컫는 이름이에요.<br> 
      아하 보통 이렇게 쓰는구나 하고 넘어가시면 됩니다!<br>
      url/ 경로 : 아까 만들어주었던 github 의 주소를 넣어주세요.<br>
      앞에 설정이 잘 되었다면 아래처럼 보일 꺼에요. 여러분들은 siyoungoh 대신 여러분들 github 이름이 보이겠죠?<br> 
      여기에서 확인 버튼을 누르면 됩니다<br>
   2. 원격 repo Github 에서 없애는 방법<br>
      Github 에 로그인 한 후 repo 페이지로 가서 Setting 을 누릅니다.<br> 
      options 를 선택한 후 맨 마지막으로 스크롤을 내립니다.<br> 
      Danger Zone 에 있는 Delete this repository (이 repository 지우기) 클릭!<br>
      정말로 지울 것인지 확인하는 창이 뜹니다. 절대 복원할 수 없으니 꼭 주의하세요!<br> 
      하단 빈 칸에 user이름/repository명 형식으로 그대로 적어주세요.<br> 
      그런 다음 I understand the consequences, ~ 버튼을 누르면 repo 가 삭제됩니다.<br> 

2주차 학습 정리
------------
### Issue 할당
   -. issue 만들어보기<br> 
      > 로그인한 후 내 repo 페이지에 접속해서  issue 탭을 눌러주세요.<br> 
   -. issue 만들기<br> 
      > 초록색 버튼 New issue 를 누르면 생성이 됩니다.<br> 
      > 제목과 상세 내용은 협업하는 사람도 잘 알아볼 수있도록 적어주는게 좋겠죠!<br> 
      > Assigness(담당자) : 이 이슈를 작업하거나 연관된 사람을 적어줍니다. 내가 요리법 업데이트 할 꺼니까 나를 선택해주세요.<br> 
      > Labels: 이 issue 가 어떤 건지 분류해주는 겁니다. Github이 만들어준 기본 라벨을 사용할 수도 있고,<br>  
         내가 직접 만들어줄 수도 있어요. 여기서는 enhancement (추가 기능 개선) , good first issue<br>  
         (처음 프로젝트에 참여하는 사람이 작업하기 쉬운 이슈) 를 골라주었어요. 마음에 드는 걸 골라주셔도 됩니다!<br>     
      > 제목 옆에 있는 #숫자 가 보이나요? 이게 바로 이슈의 번호 입니다.<br>  
      > 밑에 Leave a comment 라고 적힌 창이 생겼죠? 이슈에 대한 댓글이에요.<br>  
   -. issue 를 완료하기<br> 
      > issue  페이지 하단에  Close issue  를  누르면 이슈가 종료됩니다.<br>      

### Branch 개념
   -.  브랜치(Branch)를 사용하게 되면 나뭇가지가 뻗어나오듯 기능에 맞게 나누어 작업할 수 있습니다.<br>
   -.  issue와 브랜치 만들기<br>
       > 만약 커밋되지 않은 작업 내역이 있다면 commit 을 해주세요!<br> 
       > 왼쪽 히스토리 탭을 선택하고 - 마지막 commit 에서 우클릭 한 후 브랜치 를 선택해주세요.<br>   
       > 새 브랜치 : 브랜치 이름을 적어주세요. 내가 잘 관리할 수 있게 적어주세요.<br> 
                        여기서는 feature/이슈번호_관리쉬운이름 형식으로 만들어줍시다.<br>   
       > 정보를 입력한 후 '브랜치 생성' 버튼을 누릅니다.<br>
       > sourcetree 에서는 브랜치명 안에  / 를 적어주면 마치 폴더처럼 보여줍니다.<br> 
       > 앞으로 하는 commit 은 방금 만든 브랜치인 feature/2_jjigae 에만 반영됩니다.<br> 
          현재 작업하는 브랜치를 선택하는 것을 체크아웃(checkout) 이라고 합니다. 
   -. 브랜치 삭제하기
      > 브랜치를 삭제한다는 것은 그동안 브랜치에 했던 작업 내역 즉, commit 이 모두가 사라진다는 의미입니다. 
      >  작업 브랜치가 변경되면 파일의 상태도 당연히 해당 브랜치의 마지막 commit 으로 상태로 변경됩니다. 

### Merge 개념
   -. Merge(병합) 는 브랜치를 다른 브랜치에 합치는 것입니다.<br> 
   -. 실제 프로젝트에서는 작업 내역을 모두 합칠 기준이 되는 브랜치(main)를 정해두고 작업합니다.<br>
   -. 브랜치명은 규칙을 가지고 잘 이름 지으면 프로젝트 관리가 쉬워집니다.<br> 
      작업이 완료되면 작업한 브랜치는 보통 삭제해줍니다. 나중에 브랜치 설정이 꼬이는 것을 방지할 수 있습니다.<br> 

### Merge conflict 개념
   -. Merge 하는 과정에서 같은 파일이 동일한 부분이 수정된 게 발견되면 Merge conflict(병합 충돌) 이 발생합니다.<br>
   -. Git 이 똑똑하게 충돌을 파악할 수 있도록 파일 내용을 고쳐서 충돌 내역을 보여줍니다.<br> 
   -. conflict 를 수정하려면 최종적으로 반영할 내역으로 고친 후에 merge commit 하면 됩니다.<br> 
   -. 브랜치 두개를 만들고 각각 브랜치에서 같은 파일을 수정하고 commit 해보세요.<br> 
      main 브랜치에  merge 하려고 하면 conflict 가 발생합니다! 파일을 직접 수정해서 conflict 를 수정하고 commit 해보세요.<br>

### 원격 repo 개념
   -. tracking 한다는 것은 로컬 repo와 원격 repo의 특정 브랜치를 연결해주는 것입니다.<br>
   -. push와 pull 은 기본적으로 tracking(추적)되고 있는 브랜치를 기준으로 commit 내역을 반영합니다. 

3주차 학습 정리
------------

