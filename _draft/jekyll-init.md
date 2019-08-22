---
layout: doc
title: Jekyll init
date: 2019-08-21
categories: [jekyll]
tags: [jekyll, init, start]
---

## Jekyll 시작 요약

```shell
# '${}'는 사용자가 임의로 정해야 하는 프로젝트 명

$jekyll new ${project_name}
$cd ${project_name}
$jekyll build
$jekyll serve
```

## Jekyll 구조 요약

```shell
# '${}'는 사용자가 임의로 정한 디렉토리 명

├── ${project_name}
│   ├── ...
│   ├── _config.yml
│   ├── _include
│   ├── _layout
│   ├── _posts
│   ├── _site
│   ├── index.md or index.html
│   └── assets
...
```

반드시 있어야 하는 것은, `_config.yml`과 `index.md` 혹은 `index.html` 이다. ( index는 md일 경우, html로 변경해준다. 그리고 md일 경우, 올바른 front matter 작성이 필요하다. )

이외에 `_posts`의 경우, default collection 이며 사용하지 않아도 된다.
 
 `_include`와 `_layout`은 프로젝트의 화면들을 기본적으로 구성할 부분요소들과 틀요소들을 저장하는 곳이다.
 
 `assets`는 추가적으로 더 필요한 자료들을 담아두기 위해 만든 디렉토리로 명칭은 반드시 `assets`일 필요는 없다.

 `_site`는 `jekyll build` 명령어가 실행되었을 때, 위의 모든 것들을 가지고 만든 결과물을 저장한다. 실제 web server를 띄울 때 사용하는 부분이다.

 ## Jekyll 변수 요약

 기본적으로 사용하는 전역 변수는 다음과 같습니다.
 - site
 - page
 - layout
 - content
 - paginator ( 따로 paginator gem을 사용할 때 )

 하지만 여기서 가장 자주 사용하면서 중요한 변수는 `site` 하나만 알아두셔도 충분합니다. `site` 변수에 담겨있는 값들은 `_config.yml`에 정의한 값이거나 기본적으로 정의되어 있는 값입니다.

 `page` 변수에 담겨있는 값들은 `front matter`에 있는 값들이나 기본적으로 정의되어 있는 값입니다.

 `content` 변수는 정의 해놓은 layout을 사용하는 것들에 작성된 내용을 넣어주는 값입니다.