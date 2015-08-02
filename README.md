# facebook-react-tut
tut: [https://facebook.github.io/react/docs/tutorial.html](https://facebook.github.io/react/docs/tutorial.html)

* JSX : Js 에 Xml 문법 같이 사용할 수 있도록. -> Js 로 다시 트랜스파일해주는 트랜스 파일러가 필요함(JSXTransformer.js)

> 실행: 
> ```
> python -m SimpleHTTPServer
> open http://localhost:8000/index.html
```

### 1. 태그 만들기

```js
var CommentForm = React.createClass({
	render: function(){
		return (
			<div className="commentForm">
				Hello, world! I am a Commentform.
			</div>
			);
	}
});
```
> 이렇게 커스텀 태그를 정의 할 수 있고 다른곳에서도 써먹 을 수 있다.

### 2. html에 붙이기
```js
React.render(
	<CommentBox/>,
	document.getElementById('content')
);
```
> 랜더링할 태그를 적고, 2번째 인자로 어디다가 붙일지 찾아서 넣는다.

### 3. 태그에 데이터 넘겨주기

```js
React.render(
	<CommentBox data={data}/>,
	document.getElementById('content')
);
```
태그의 애트리뷰트로 넘겨주면 되는데, 받는 태그(클래스?)에선 this.props 로 접근해서 찾아오면 된다.