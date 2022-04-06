# movieWeb

# 해야할 것
** 메뉴 추가로 더 만들기 **

# 공부 중

## 2.0(instoduction)

    ReactJS
    해결하고자 하는 문제를 정확하게 파악하고 해결을 해야한다.

    바닐라 JS의 코드와 ReactJS의 코드를 비교해가며 기존 코드의 문제점과 React의 장점을 볼 것이다.
    interactive한 사이트를 만들 것이다.

## 2.1(Before React)

    html, js로 작성

## 2.2(Our First React Element)

    ReactJs는 html을 페이지에서 직접 작성하지 않는다.

    개발자들이 개발하는 방식은아니다. 더 쉬운 방식이 있고 도구를 제작해서 더 편리하게 개발을 한다.
    이번에 다루는 방식은 다른 사람들이 사용하지 않는 방식이다.
    하지만 우선 어려운 것을 먼저 해봐야한다. 이 방식을 살펴보며 React의 본질을 살펴봐야한다.

    React는 엔진이고 React-dom은 작성한 코드를 html로 옮겨준다.

    모든 것이 JS에서 시작해서 HTML로 옮겨감. React JS가 결과물인 HTML을 업데이트 할 수 있다. JS상에서 유저에게 보여질 내용을 컨트롤 할 수 있다.

## 2.3 (Events in React)

    btn
    React의 방식으로 EventListener을 넣어봄.
    interactive한 작업을 위해서 이렇게 작업하는게 편하다.
    Js에서 이벤트를 등록하였다.

    ReactDOM DOM은 대문자로 해줘야함.

## 2.4(Recap)

    React element를 가져다가 html로 바꾸어야했다.
    ReactDOM은 render함수를 통해 html로 바꾸어준다.

## 2.5(JSX)

    JSX는 JS를 확장시킨 문법이다.

    에러가 발생하였는데 에러문장을 꼼꼼히 확인하지 않고 설정 오류인줄 알고 설정 값을 확인하였는데
    아래 타이핑에서 오타가 있었던 것이였다.
    => 에러 나온 것을 좀 더 꼼꼼히 읽어야겠다.

## 2.6(JSX part Two)

    21 <Title/> 과같은 컴포넌트의 첫글자는 반드시 대문자여야한다.
    만약 소문자면 React랑 JSX는 이게 HTML button태그라고 생각을 할 것이다.

    {}와 ()
    return 과
    < Button />

## 3.0(Understanding State)

    지난 강의에서는 react element를 생성하는 방법에 대해 배웠다.

    react element를 함수내에 담으면 원하는 만큼 사용 할 수 있다는 것도 배웠다.

    rerender을 하는 기법 ui에 적용이 되지 않고 변수만 증가한다.
    값을 바꿀 때마다 다시 렌더링하는걸 잊어버리면 안된다.

    바닐라 js에서는 요소가 바뀌면 html요소 전체가 업데이트가 되는데
    react js에서는 h3 button 과 같은건 바뀌지 않고 ui에서 바뀌는 부분만 업데이트 해준다.(유일하게 바뀌는건 숫자 뿐이다)
    =>일반 자바스크립트를 쓴 브라우저는 노드정보가 바뀔때마다 노드 트리를 처음부터 다시 시작하는데 
    리액트는 가상돔을 써서 우리 시야에 보이는 부분만 수정해서 보여주고 모든 업데이트가 끝나면 일괄로 합쳐져 실제 돔에 던져준다고 합니다. 
    render == 렌더트리 


    rerender을 코드로 직접 해주야하므로 그렇게 효율적이진 않다. 새로운 값이 계속 바뀌면 효율 적이지 않다.
    다음 강의에서는 데이터를 바꾸고 다시렌더링해주는 것을 할 것이다.
    우리가 리렌더링하면 컴포넌트도 바로 바뀐 데이터를 가지고 바뀔 것이다. `

    (또 코드를 잘못 적어서 오류가 한참 났다. 우선 코드를 하나하나 꼼꼼하게 보는 실력을 길러야겠다.)

    
    front는 렌더트리를 얼마나 최적화 하는 것이 중요하다.

## 3.2(setState part One)

    우리가 click me를 클릭 할때 물론 Container 컴포넌트 전체를 리렌더링하는 거지만 사실은 html코드에서는 오로지 숫자만 바뀌는 거다.
    새 countainer 컴포넌트를 생성하고 교체해 줄거라고 생각하지만 바뀐부분만 새로 생성 할 수 있게 해준다. 
    자동으로 rerendering 될 수 있는 방법

    useState()함수에서 얻어 올 수 있는건 함수를 사용할때 쓸 data와 data를 바꿀떄 사용하는 함수이다.

     const [counter, modifier] = React.useState();
        /*위 코드와 같은 코드이다.
        const data = React.useState(0);
        const counter = data[0];
        const modifiier = data[1];*/

## 3.3(setState part Two)
    리렌더링을 해줘야한다.
    modifier함수는 어떤 값을 부여하던 그 값으로 업데이트 하고 리렌더링을 일으킬 것이다.
    
    usestate 한 줄로 conuter과 같은 함수를 숫자형 데이터로 건네줄 것이고 그 데이터 값을 modifier 로 바꿔줄 것이다. 
    그리고 컴포넌트도 rerendering 될 것이다.

    13 const[counter,setConter]

    ** 주소는 절대 바뀌지 않지만 그 객체는 변경이 가능해서 counter이 변경이 가능해보인다 **

    에서 let이 사용하는const를 사용하는 이유 : const는 상수 취급이며 재할당이 불가하다. 
    => object를 const로 지정할 경우 주소가 참조되는데 이때, 주소가 바뀌는 로직이 업다면 헤당 객체 내의 값을 변경해주면서 사용이 가능하다.

    => 그리고 재할당이 필요한 변수가 아닌라면 const를 사용하는 것이 안전하다 왜냐하면 const는 항상 같은 객체를 가리키고 있기 때문이다.

    React.useState()
    보통 데이터에는 counter 처럼 원하는대로 붙이고 f는 set뒤에 데이터 이름을 붙힌다.

    인자로 넘겨주는 값은 state의 초기값이다.
     count를 갱신하기 위해 this.setState()를 호출합니다.

## 3.3(Rec
    modifier함수를 사용해 state를 바꿀떄 컴포넌트(app()) 전체가 재생성 될거다.
    return도 생성되고 새로운 counter의 값을 가지고 한번 더 실행이 될거다. 

## 3.4(State Functions)



    //setCouter(counter + 1);
    setCounter((cuurent) => current +1); //이게 더 안전한 방법이다. 

## 3.5(inputs and State)
    label에 for이라는 prop은 JS의 용어이다 이미 선점된 단어이다. 
    지금은 우리는 JSX를 쓰고 있어서 괜찮은거다. 이나중에는 class를 className이라고 써야하고 for을 HtmlFor이라고 사용해야한다.

    
    
    
    
    지금은 production.min.js버전을 사용중이여서 가능하다.

    아직 ReactJS를 쓰지 않아서 괜찮다.

    ReactJs는 우리가 사용하고 있는 normal JS와 비슷하다

    event.target.value에서 값을 찾아오는 것도 같다. 

    onchange가 일어났을때 onchange()(발생한 event에 대해서 event.target.value의 값을 가져오는 역할)가 실행되어서 데이터를 업데이트 해준다. 
    input은 스스로 값을 업데이트한다. 
    
## 3.6(State Practive part One)
    
    우리가 onchange = onchange()을 삭제하게 되면
    input id=minutes 의 value가 state이고 default값이 0이기 떄문에 값의 입력이 되지 않는다.
    업데이트가 이루워지지 않는다.

    disable의 속성을 주면 클릭을 할 수 없다.     

## 3.7(State Practice part Two)

    Flip function만들기

    state를 조작해서 만들어 줄 것이다.
    state 값으로 input을 enabled 할지 안할지 정해줄 수 있다.

    hour에 
    changeon함수를 사용하고 싶읖떈 value를 바꿔줘야했다.
    기존의 코드는 minute를 썻을때에 한에서만 값을 바꿔주는 것이였다.

    disable
    
## 3.8(recap)
    hour과 minutes의 disable은 항상 반대이다. 
    
    hour과 minutes의 onchange에 같은 함수를 사용하였으니까 
    amount를 이용해서 입력값을 받게해준다.

    flipped의 상태에 따라 input에 값이 다르게 보여진다. 


## 3.9(final practice and recap)
    사용자가 원하는 단위를 변환할 수 있게 메뉴바를 만들어줌.


## 4.0(props)
    로직에서 isolation과 encapsulation을 적용시켜서
    이걸 이용하면 분할 할 수 있다. 
    우린 이 컴포넌트를 가지고 우리가 원하는만큼 이동 시킬 수 있다. 

    이 로직을 고립시켜서 분리된 컴포넌트로 만들을 것이다.

    footer인지 header인지 nav인지 

    각각의 로직들을 각각의 조각들로 분리시켜서 만드는게 좋다. 

    html과 jsx를 합쳐서 매우 큰 것

    prop 
    어플리케이션은 수 많은 버튼을 가지고 있음. 
    //props는 첫번쨰이자 유일한 인자다. 이 btn이 전달 받는 유일한 인자이다.

    컴포넌트 : 단지 함수다. (어떤 JSX를 반환하는)

    완전 같은 컴포넌트인데 글씨만 다르다면 
    우리들의 컴포넌트들을 조금은 설정이가능하게 해주는 것이다.
 
    실제로는 props를 자주 쓰지는 않을 것이다. 
    디른 더 좋은 방법이 있다. 그것을 자주 사용할 것이다.
    => {text} 이렇게 사용하는 것이다.

## 4.1(memo)
    Btn태그 내부의 onclick은 prop의 일부로서 이벤트 리스너의 역할이 아니다 btn안에 전달 되고 있는 것이다. 
    prop을 전달하는거지 react가 이벤트 리스너로 해주는 것이 아니다.
    button 태그를 위한 이벤트 리스너가 아니다. BTN의 prop이다.


    컴포넌트의 prop가 변경되지 않는한에서 바꿀 수 있다.
    state가 변경된다면 아래의 컴포넌트도 변해야한다 props는 변하기 떄문이다.

    부모의 컴포넌트가 rerender되면 자녀의 컴포넌트도 전부 rerender가 되기떄문에 프로그램이 느려지는 원인이 될 수도 있다.
    그러니까 props가 변경되지 않는다면 굳이 다시 그릴 필요가 없다는 것이다.

## 4.2(prop type)
    porps에 대한 정리

    state prop 
    그리고 리엑트 프로젝트를 만들 것이다.
    props type

    리액트가 너에게 실수를 하고 있는지 말해주지 않는다. 
    그러나 proptype  어떤 타입의 prop를 받고 있는지 체크해준다.




# 하고 싶은 공부
