# SPA(Single Page Application)
- Web App과 함께 자주 등장할 용어 SPA
- 이전까지는 사용자의 요청에 대해 적절한 페이지 별 template을 반환
- SPA는 서버에서 최초 1장의 HTML만 전달받아 모든 요청에 대응하는 방식
  - 어떻게 한 페이지로 모든 요청에 대응 할 수 있을까?
  - CSR(Client Side Rendering) 방식으로 요청을 처리하기 때문

# SSR (Server Side Rendering)
- 기존의 요청 처리 방식은 SSR
- Server가 사용자의 요청에 적합한 HTML을 렌더링하여 제공하는 방식
- 전달 받은 새 문서를 보여주기 위해 브라우저는 새로고침을 진행

# CSR(Client Side Re    ndering)
- 최초 한 장의 HTML을 받아오는 것은 동일
  - 단, server로부터 최초로 받아오는 문서는 html 문서
- 각 요청에 대한 대응을 JavaScript를 사용하여 필요한 부분만 다시 렌더링
    1. 필요한 페이지를 서버에 AJAX로 요청
    2. 서버는 화면을 그리기 위해 필요한 데이터를 JSON 방식으로 전달
    3. JSON 데이터를 JavaScript로 처리, DOM 트리에 반영(렌더링)

# timer.html
```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
</head>

<body>

    <div id="app">
        {{startTimer()}}
        <p>시간이 흐른다 : {{ time }}</p>
    </div>

    <script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
    <script>
        const app = new Vue({
            el:'#app',
            data: {
                time: 0,
            },
            methods: {
                startTimer(){
                    setTimeout(() => {
                       this.time++; 
                    }, 1000);
                }
            },
        })
    </script>

</body>

</html>
```