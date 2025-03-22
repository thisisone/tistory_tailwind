# 티스토리 블로그에 tailwind 적용하기

github 주소
https://github.com/thisisone/tistory_tailwind

tailwind 따라하기 문서
https://tailwindcss.com/docs/installation/tailwind-cli

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
