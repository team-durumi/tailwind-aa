# 범용적으로 사용할 수 있는 aa-starter-theme

## 진행

- UI 기준에 잡혀있는데로, 테마 설정을 시도한다. (color, typo)
- html에 찍고 있는 partial에 데이터를 data/user-marketing.yml 로 옮겨본다.
- alpinejs 를 사용하도록 할 수 도 있고, js 적용을 다시 결정할 수도 있다.



## As a Project

```bash
npm install
hugo server
```

## As a Theme

Import `github.com/bep/hugo-starter-tailwind-basic/v2` (use `github.com/bep/hugo-starter-tailwind-basic` if you want/need Tailwind 1.x.) into your project, and then run:

```bash
hugo mod npm pack
npm install
```

You need to add this to your `config.toml` (the stats are used by the CSS purging):

```toml
[build]
writeStats = true
```

Then run your project as usual.
