# Chanwoo Lee's Blog


## 개요
chanwoow.github.io는 블로그를 구현하기 위해 만든 사이트로, 2021학년 2학기 강의인 유레카프로젝트에서 진행되었던 깃 블로그 강의를 기반으로 웹사이트를 설계하고자 노력하였다. 향후에 개인적으로 개발 블로그 및 프로젝트 보관용으로 사용할 수 있는 웹사이트를 만들기 위해 강의를 순차적으로 따랐고, 구체적으로 아래의 과정을 거쳤다.

## 환경 설정
- 우선 본 계정인 chanwoow에 웹페이지로 만들어질 원격 저장소를 생성했다. 생성한 후, 디렉토리로 이동하여 `git clone https://github.com/chanwoow/chanwoow.github.io.git` 를 통해 로컬 저장소에 연결시켰다.

- 그리고 [Jekyll 공식 사이트의 Windows 설치 안내](https://jekyllrb-ko.github.io/docs/installation/windows/)를 참고하여 RubyInstaller를 이용해 윈도우 환경에 Jekyll을 다운로드하였고, `gem install jekyll bundler` 명령을 입력하여 Jekyll과 Bundler를 설치하였다.

- 또한 `jekyll new . --force` 명령을 통해 현재 디렉토리에 Jekyll을 설치하였다.

- 그리고 `bundle exec jekyll serve`를 실행하는 과정에서 발생하는 의존성 문제를 해결하기 위해 `bundle add webrick` 명령을 사용하였다.

## 테마 설정
- 모든 환경 설정을 마친 후, 새로운 테마를 불러오기 위해 기존 원격 저장소를 삭제했다. 그리고 새 원격 저장소를 만들어 sylhare 유저의 Type-on-Strap 테마를 fork를 통해 불러왔고, 해당 저장소의 이름을 chanwoow.github.io로 변경했다. 그리고 fork한 결과를 로컬 저장소에 재연결시켰다.

- 처음 테마를 적용했을 때, 로컬에서 실행했을 때에는 정상적으로 사이트가 표시되지만 원격에서 실행하면 CSS가 깨지는 현상이 발생했다. 이를 해결하기 위해 구글링하는 과정을 거쳤고, `_config.yml`의 baseurl 부분을 빈 문자열로 처리하여 CSS 깨짐 문제를 해결하였다.


## 댓글 기능 추가
- 댓글 기능을 추가하기 위해 [Disqus 홈페이지](https://disqus.com/)에서 가입 절차를 거쳤고, 사이트 정보 입력, 플랫폼 중 Jekyll 선택 등의 과정을 거쳤다. 그리고 표시된 Universal Code를 복사했다.

- 처음에는 복사한 코드를 단순히 Post에 해당하는 파일인 `post.liquid`의 아랫부분에 붙여넣었다. 그랬더니 정상적으로 표시는 되었지만, 댓글이 포스트의 가로 영역을 벗어나 미적으로 좋아보이지 않았다.

- 확인해보니, 본 테마의 템플릿에 Disqus 댓글 적용을 위한 `disqus.liquid`라는 별도의 파일이 있었고, 해당 파일을 이용하기 위해 `_config.yml`의 disqus shortname 부분을 알맞게 채워넣은 후 다시 적용하니 기대했던 대로 포스트의 가로 영역을 벗어나지 않도록 변경되었다.

## 불필요한 데이터 삭제 및 수정
- 다른 유저의 테마를 fork한 것이기 때문에 템플릿에 기본적으로 포함되어 있는 불필요한 post 파일을 삭제해야 했고, About 페이지나 Portfolio 페이지의 텍스트 등을 수정할 필요가 있었다.

- 따라서 `about.md`, `portfolio.md` 등 각 파일에 진입하여 불필요한 부분들을 삭제 및 수정하는 과정을 거쳤다.

## 포스트 추가
- Markdown 형식에 맞추어 강의에서 배웠던 Markdown에 대한 간략한 설명과 문법들을 정리한 포스트를 업로드했다.

- Google Analytics를 사이트에 적용한 후 적용 과정에 관한 포스트를 업로드했다.

## favicon 추가
- 본 테마에 원래 favicon이 설정되어 있었으나, 나는 다른 favicon을 설정하기 위해 png 확장자의 외부 이미지를 ino 확장자로 변환하여 assets 폴더에 추가했다.

- 그리고 이 이미지를 favicon으로 사용하기 위해 `_config.yml`의 `facicon` 부분에 이미지의 경로를 입력하여 적용했다.

