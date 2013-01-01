추억의 터미널 영한사전
======================

아득한 추억이된 터미널에서 사용가능한 `edic` 영한사전입니다.
이제는 최초에 어느분이 개발해주셨는지도 알수가 없는 상황입니다.
각종 검색엔진에서 찾아보아도 너무 오래전이라서 그런지 알수가 없네요
문득 생각이나서 찾아 보니 PHPSCHOOL에 `알짜 리눅스`시절의 rpm 패키지를
구할 수 있었습니다. 

출처
----
현재 원저작자가 누구인지 알 수 없는 상태입니다.
혹시 아시는분은 알려주시면 감사하겠습니다.
github 저장소에 업로드한 `edic` 은 PHPSCHOOL에 올라왔던 RPM 패키지 파일을 이용했습니다.
아래링크 참고

* http://www.phpschool.com/gnuboard4/bbs/board.php?bo_table=download&wr_id=33


수정내용
--------
* 인코딩 변경 : alien을 이용하여 deb로 변환한 후 우분투에 설치해보니 잘 작동 하더군요.
다만, 십수년전 버전이라서 euc-kr로 인코딩된 사전데이터들을 iconv를 이용하여 utf-8로 
변경 하였습니다.

* 스크립트 수정 : edic 스크립트를 약간 수정하여 인코딩을 euc-kr 과 utf-8을 선택할 수 있도록 하였습니다.
(luit 명령어를 이용하여 인코딩을 바꿀수 도 있지만, utf-8 인코딩 파일을 포함하였습니다.)

* 디렉토리 변경 : /usr/share/engdic 에 사전데이터를 포함하고 있었는데, 이를 data/euc-kr , data/utf-8 로
분리하여 각각의 인코딩 데이터를 포함하도록 하였습니다.

* euc-kr용 edic인 edic.euckr 과 utf-8용 edic.utf8 을 각각 data/euc-kr 과 data/utf-8 디렉토리에 생성

* edic 실행 스크립트가 $LANG 환경변수에 따라(ko_KR.UTF-8 혹은 ko_KR.eucKR) edic.euckr과 edic.utf8을 실행 할 수 있도록 수정함


사용법
------
* edic 가져오기 : git clone https://github.com/liks79/edic.git
* 'edic' 이 존재하는 디렉토리에 PATH 설정하기
* PATH 적용 후 `edic` 실행


라이선스
--------
원저작자도 알수없고, 라이선스 표시도 되어 있지 않습니다.
다만, 십수년전 당시에 나우누리, 하이텔 리눅스 동호회에서 널리 퍼진것으로 알고 있습니다.
해당 라이선스에 대해서 준수 사항이 있다면 알려 주시기 바랍니다.
배포에 문제가 발생한다면 바로 저장소를 삭제하겠습니다.
(당시 알짜(ALZZA) 리눅스 배포본에 기본으로 포함되어 있었습니다. 아마도 GPL에 준하는 라이선스이지 않을까 생각됩니다.)

* 다음은 원본 RPM 패키지에 포함되어있던 COPYRIGHT 정보입니다.

    Copyright: distributable
    
    Information from the binary package:
    
    Name        : engdic
    Version     : 0.1
    Release     : 6
    Architecture: noarch
    Install Date: (not installed)
    Group       : Extensions/Korean/Utilities/Text
    Size        : 2291146
    License     : distributable
    Signature   : RSA/MD5, 1998년 11월 19일 (목) 오전 10시 58분 22초, Key ID 369a7855d7341f8d
    Source RPM  : engdic-0.1-6.src.rpm
    Build Date  : 
    Build Host  : linux.sarang.net
    Relocations : (not relocatable)
    Packager    : ALzzA Team <alzza@linux.sarang.net>
    Vendor      : Alzza Team
    Summary     : Little korean - english dictionary
    
    Description :
    Little korean - english dictionary



스크린샷
--------
* ScreenShot.png
![ScreenShot](https://github.com/liks79/edic/blob/master/ScreenShot.png "스크린샷")

