## CSS공부내용
___
### 부모자식선택자

* Tag를 이어붙이면 (EX: ul li) 부모-자식 관계로 CSS선택자 생성가능

* &#62;를 이용해서 직계 자식에게만 상속가능

* 쉼표(,)를 이용해서 여러 선택자 사용가능

___
### 선택자 공부 팁
[선택자 선택 게임](https://flukeout.github.io/)
* CSS Cheat Sheet

___
### 가상 클래스 선택자
(Ex: 링크방문여부 )와 같이 동적인 활동을 가상 클래스로 하여 선택 가능
*    :link - 방문한 적이 없는 링크
*    :visited - 방문한 적이 있는 링크
*    :hover - 마우스를 롤오버 했을 때
*    :active - 마우스를 클릭했을 때  
(Ex: a:visied{})

___
### 상속
* border는 상속되지 않음
* vscode 여러줄 주석: ctrl + k and ctrl + c

___
### 캐스케이딩 소개
* CSS : Cascading Stlye Sheet
* CSS의 기본원칙은 사용자나 저자가 원하는 방식으로 웹페이지를 변경할 수 있어야 한다는 것
* 우선순위는 웹브라우저\<사용자\<저자

___
### 캐스케이딩 실습
* 여러 선택자가 동시에 선택됐을 때, 해당 태그에 직접 style로 명시된 부분이 우선순위를 가진다.
* id선택자가 class선택자보다 우선순위를 가진다.
* 가장 구체적 규칙이 우선순위를 가진다 (구체적 규칙 > 포괄적 규칙)
* important가 붙으면 우선순위가 제일 위로 감

___
### 크기 : font-size
* 폰트사이즈를 나타내는 단위 3가지: px, em, rem
* px는 크기가 고정돼있음
* em과 rem은 크기가 브라우저 창의 크기에 따라 가변적
* 최근에는 사용자의 권한을 지켜주는 것이 가능한 rem을 사용하는 추세
* 사용자가 창의 글꼴을 키웠을 때 px는 바뀌지 않지만, rem은 바뀜
* 개발자도구에서 styles 창 옆에 computed탭을 선택하면 현재 태그에 적용된 CSS속성을 볼 수 있음
* em은 상위 컴포넌트의 픽셀값, rem은 최상위 컴포넌트(html 속성)의 픽셀값

___
### 타이포그래피 : color
* 색상을 나타나는데는 크게 RGB방식, Hexadecimal(16진수) 방식이 있음 (+ 색상이름으로 표시)
* [링크](https://www.w3schools.com/css/css_colors.asp)에서 다양한 color를 볼 수 있음
* Hexadecial 6자리중에 각 2자리는 각각 R,G,B에 대응함. (2개의 16진수 자리로 256을 표현)

___
### 정렬: text-align
*[링크](https://www.lipsum.com/) : 의미없는 TEXT를 만들어 줌
* text-align의 justify 속성을 통해 텍스트의 좌우여백을 공평하게 만들 수 있음


___
### 타이포그래피: font
* [오픈튜토리얼즈 링크](https://opentutorials.org/module/2367/13361)
* font-family라는 속성으로 사용할 font를 지정함
* font는 한번에 여러개를 지정할 수 있음(사용자의 컴퓨터에 해당 폰트가 없을 수 있기 때문에)
* Serif는 영문자에 장식이 있다는 뜻
* font-weight: 폰트의 두께
* line-height: 자간
* font 속성에 (font-style font-variant font-weight font-size/line-height )

___
### 웹폰트
* 사용자가 가지고있지 않은 폰트가 깨지는 현상을 해결하는 기술
* 사용자가 폰트를 가지고 있지 않으면 웹상에서 다운로드 받음(용량관리가 핵심문제)
* [웹폰트 링크](https://fonts.google.com/)
* 링크에서 사용할 폰트들을 선택하면 뜨는 링크에서 복사해서 link태그로 붙이고, 폰트를 사용하면 됨
* 개발자도구에 Network탭에서 폰트를 다운로드 받는 것을 확인할 수 있음
* webFont를 만들 수도 있음(font generator를 치면 나오는 다양한 사이트들 활용)

___
### 인라인 VS 블럭레벨
* a태그는 inline, h1태그는 blocklevel 엘리먼트임(화면 전체를 다쓰는 태그가 block level)
* display 속성으로 레벨을 변경할 수 있음


___
### 박스모델
* border 속성을 통해 경계선의 속성을 설정할 수 있음
* padding 속성을 통해 content와 border간 간격을 설정할 수 있음
* margin 속성을 통해 block element간 간격을 설정할 수 있음
* width 속성을 통해 content의 가로길이를 설정할 수 있음
* inline componenet에는 width 속성은 적용되지 않음
    
___
### box-sizing
* css초창기에는 width속성이 border와 margin을 제외한 순수 컨텐츠 영역의 넓이였음
* 그러다보니 width속성을 똑같이 해도 전체 사이즈가 다른 경우 발생
* 이를 해결하기위해 box-sizing속성이 나옴
* box-sizing:border-box를 통해 border영역에 맞춰서 영역의 넓이를 같게 할 수 있음

___
### 마진겹침1(margin-collapsing)
* margin이 있는 2개의 요소가 만났을 때, margin이 큰 요소의 margin값으로 이 요소들이 겹친다.

___
### 마진겹침2
* 부모-자식 요소간에는 border가 있으면 마진겹침이 일어나지 않고, border가 없으면 마진겹침이 발생한다.

___
### 마진겹침3
* border가 없는 경우, margin-top 과 margin-bottom의 요소중 큰 값이 두 곳 모두에게 적용된다.

___
### 포지션1: relative VS static
* offset속성(ex: left)변경을 통해 element의 위치를 이동할 수 있다.
* left가 right보다 우선하고, top이 bottom보다 우선함.
* position 속성을 relative로 설정해야 원하는대로 이동 가능.(기본 설정은 static)

___
### 포지션2: absolute
* absolute속성을 이용해 position 속성이 static이 아닌 첫 상위 컴포넌트로부터 위치를 지정할 수 있음.
* absolute 속성을 적용하면, 부모로 부터 독립되기 때문에, 크기가 본인의 content만큼으로 작아짐

___
### 포지션3: fixed
* fixed 속성은 화면에 해당 요소가 고정됨(스크롤에 상관없이)
* fixed도 absolute와 마찬가지로 부모 요소로부터 독립됨

___
### flex 소개
* flex는 문서의 Layout을 잡는 속성 
* 초기에는 Table이 사용됐지만 복잡하고, 구분이 잘 안돼는 문제가 있었음
* 이후 POSITION(absolute, relative)등을 통해 표현함
* 이후 FLEX를 통해 여러 속성으로 컴포넌트를 조작함
* FLEX를 쓰려면 container역할을 하는 부모 속성이 필요함
* container 속성과 item 속성이 구분 돼 있음

___
### flex 2: basic
* flex를 쓰려면 부모의 속성에서 display:flex를 해야함
* 이후 부모 속성에서 flex-direction 속성을 통해 item의 방향을 조정할 수 있음 (column, column-reverse, row, row-reverse)

___
### flex 3: grow & shrink
* flex-basis를 통해 기본 flex크기를 설정할 수 있음
* flex-grow를 통해 1로 설정하면 container에 아이템을 가득 채울 수 있음(default 값은 0)
* flex-grow를 1 이상의 수로해서 우선순위를 높이면 그 숫자만큼 화면이 더 가득참
* flex-shrink 속성을 통해 브라우저 창의 크기를 줄였을 때 요소가 줄어들 값을 설정할 수 있음(default: 1)(0으로 설정하면 줄어들지 않음)(1이상의 수로 하면 그 배수만큼 다른 요소보다 빨리 줄어듦)

___
### flex - holy grail layout
* flex basic, shrink를 통한 실습
* 페이지를 구역을 나눠서 표시하는 layout
* 여러 효율적인 구조를 찾는 과정이 있었어서 마치 성배를 찾았다는 뜻에서 holy grail layout이라는 이름이 붙음


___
### flex 5 - 기타 속성들
* wrap - nowrap (wrap 속성은 container의 크기보다 item들의 크기합이 더 크면 줄바꿈함)
* Align-Items - JustifyContent - Align-Content

___
### mediaquery 1 - 기본
* mediaquery: 특정 상태가 됐을 때만 css 속성을 적용할 수 있는 기능
* style에서 \@media를 통해 적용 가능

___
### mediaquery 2 - 응용
* mediaquery를 통해 특정 layout에서 크기가 일정 범위에 들면 layout을 변경할 수 있도록 조절할 수 있음

___
### float 기본
* flex가 나오기 이전에 사용되던 요소, 비슷한 기능을 함
* float를 이미지에 설정하면, 글자들이 이미지 옆에 자연스럽게 나옴
* 여러 요소들 중 일부 요소만 float를 사용하고 싶지 않으면, 해당 요소들에 style= "clear:both;"를 적용하면 됨

___
### float를 활용한 holy grail 레이아웃
* 본문에 3개의 요소를 나란히 놓을 필요가 있을 때 적용할 수 있음.
* 1번째를 float로 설정한 후에, 2번째 요소가 1번째 요소보다 크면 밑으로 흘러나오는 점을 해결하기 위해 2번쨰 요소도 float로 설정
* 이렇게하면 2번째 요소 전체가 1번쨰 요소로 오기 때문에 2번째 요소의 길이를 지정해줌
* 이렇게하면 2번째 요소와 1번째 요소가 화면에 같이 나올 수 있는 크기가 되면, 원했던 대로 가로로 표시됨
* 이제 밑의 footer 요소가 이전 요소들의 float속성 때문에 옆에 달려 나오는 문제를 해결하기위해, clear: both 설정을 해줌

___
### Multi Column Layout
* 신문과 같이 화면의 Layout이 클 때 사용하는 기법
* column-count를 통해 요소에서 가질 열의 개수를 지정할 수 있음
* column의 수를 지정 안하고 폭만 지정하면 해당 폭 만큼 열 개수가 생김
* column 수와 폭 둘다 지정하면 column-width가 보장 안될만큼 창이 작아지면 갯수가 줄어들지만, width가 무한정 늘어나도 column개수가 지정된 것 이상으로 많아지지는 않음

___
### background(배경)
* background-image 설정을 통해 요소의 배경이미지를 선택할 수 있다.
* 배경이미지에 transparent(투명)요소가 있으면 background-color와 중첩될 수 있다.
* 배경이미지가 요소보다 작다면, 이미지가 반복된다.
* 반복하지 않기 위해서는 background-repeat: no-repeat로 설정한다.

___
### filter(필터)
* 화면을 뿌옇게 하는 것과 같은 기능 (흑백, 블러 등등)
* codepen 사이트를 통해 css 필터들을 볼 수 있음