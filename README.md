# 티스토리 블로그에 tailwind 적용하기

github 주소
https://github.com/thisisone/tistory_tailwind

tailwind 따라하기 문서
https://tailwindcss.com/docs/installation/tailwind-cli

Prettier 설정 문서
https://velog.io/@gangk_99/VS-Code-Prettier-%EC%84%A4%EC%A0%95%ED%95%98%EA%B8%B0

Prettier 설정전에 티스토리에거 사져온 html 이 문제가 있는 경우가 있다.
이러면 저장해도 자동 정렬이 되지 않는다.
그걸 확인해보자

1.먼저 내 편집기에 test.html 을 만든다.

```
<html>
  <head></head>
  <body>
    <div>aaaa
    </div>
  </body>
</html>
```

이런식으로 작성하고 저장해본다.
자동정렬이 된다면 Prettier 문제가 아니고
티스토리의 html 파일이 문제이니 잘 찾아서 고쳐야 겠다.

문제의 테그
s_cover_item_thumbnail
search 
s_list 안에 테그 오류



Prettier 설정하기

1. ctrl + , 입력
2. default formatter 검색
3. 스크롤 내리다보면 `settings.json 편집` 이란 버튼이 나온다
   클릭
4. 마지막줄 바로위에 에 이걸 넣어준다.

```
 ~~~
} <-- 이런 기호로 끝난다.
```

여기를

```
   , "[html]": {
      "editor.defaultFormatter": "esbenp.prettier-vscode"
   }
}
```

이런식으로 json 포맷 잘 맞춰서 넣어준다.

# 순서

1. 티스토리에서 html 코드를 복사하여
   index.html 에 붙인다.

2. 티스토리에서 css 코드를 복사하여
   index.css 에 붙인다.

3. index.css 제일 위에 이걸 넣는다.

```
@import "tailwindcss";
```

4. 터미널 열고 명령어를 실행한다.
   index.css 를 고치면 style.css 가 빌드된다.

```
npx @tailwindcss/cli -i ./src/index.css -o ./src/style.css --watch
```

5. 잡업이 완료되면
   index.html 은 html 에
   style.css 은 css 에
   복붙한다.

   images 파일도 추가했다면 업로드한다.

# 할일

vscode 에서 저장하면 자동으로 빈칸 정령해주던데
편하다 방법 알아보는중
