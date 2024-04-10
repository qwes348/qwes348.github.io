# Hugo 블로그 저장소

## 설치

> [!IMPORTANT]  
>  저장소 clone 시 submodule로 들어가있는 blowfish 테마를  
>  포함해서 clone해야 합니다.

```shell
$ git clone --recursive https://github.com/username/repo.git
```

이미 클론을 받아버린 뒤 라면

```shell
$ git submodule update --init --recursive
```

<br/>

> [!IMPORTANT]  
> 댓글 기능을 위한 partial HTML파일을 추가해야 합니다.

`themes\blowfish\layouts\partials` 경로에 추가해주세요

```html
comments.html
<!-- Utteranc댓글 -->
<script
  src="https://utteranc.es/client.js"
  repo="{{ .Site.Params.utteranc.repository }}"
  issue-term="{{ .Site.Params.utteranc.issue_term }}"
  theme="{{ .Site.Params.utteranc.theme }}"
  crossorigin="anonymous"
  async
></script>
```
