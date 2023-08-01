# SCSS Architecture (패턴 / 폴더 구조)

One Paragraph of project description goes here

## Installation

Provide code examples and explanations of how to get the project.

```
styles/

– abstracts/
    – _variables.scss    
    – _mixins.scss       

– vendors/
    – _bootstrap.scss    

– base/
    – _reset.scss        
    – _typography.scss   

– layout/
    – _navigation.scss   
    – _grid.scss         
    – _header.scss       
    – _footer.scss       
    – _sidebar.scss      
    – _forms.scss        

– components/
    – _buttons.scss      
    – _carousel.scss     
    – _cover.scss        
    – _dropdown.scss     

– pages/
   – _home.scss         
   – _contact.scss      

– themes/
   – _theme.scss        
   – _admin.scss        

– app.scss
```

## abstracts

absctracts 폴더는 프로젝트 전체에서 사용되는 모든 Sass 도구와 도우미를 담고 있다.

예를 들어 모든 전역 변수, 함수, mixin 및 표시자를 넣어주면 된다.

```
_variables.scss
_mixins.scss
_functions.scss
_placeholders.scss
```

## vendors

프로젝트에서 사용하는 외부 라이브러리 및 프레임워크의 모든 CSS 파일을 담고 있다.

```
_bootstrap.scss
_jquery-ui.scss
_select2.scss
```

## base

프로젝트의 상용구 코드라고 부를 수 있는 내용을 담고 있다.

사이트 전반에 사용될 폰트, 디폴트 스타일이 여기에 해당된다.

```
_base.scss (HTML 요소 - html, body 등 디폴트)
_reset.scss (브라우저 기본 CSS 초기화)
_typography.scss (폰트)
_animations.scss (@keyframes를 포함한 애니메이션)
```

## layout

```
_grid.scss
_header.scss
_footer.scss
_sidebar.scss
_forms.scss
_navigation.scss
```

## components

layout보다 더 작은 구성 요소들을 담고 있다.

즉, 소형 레이아웃 같은 의미로 사이트 내에서 재사용 가능한 작은 부분들을 의미하는데, buttons, slider, loader, widgets 등이 포함된다.

```
_buttons.scss
_media.scss
_carousel.scss
_thumbnails.scss
```

## page

모든 페이지가 동일한 스타일을 사용하지는 않기 때문에, 페이지 고유의 스타일이 있는 경우 페이지 이름을 딴 파일을 만들어서 이 폴더에 넣어 사용한다.

```
_home.scss
_contact.scss d
```

## themes

대규모 사이트와 애플리케이션에는 다양한 모드의 테마를 사용하고는 하는데, 각 모드에 따라서 각기 다른 스타일을 지정하여 담아두는 곳이다.

```
_theme.scss
_admin.scss
```

## app.scss

위와 같이 각 폴더 기준에 따라 scss파일들을 분류했다면, 이 모든 파일들을 단 하나의 파일로 모아서 사용한다.

해당 파일은 직접적으로 스타일을 정의하지 않고 단지 "import"만을 담당하는 파일이다.

```
@import 'abstracts/variables';
@import 'abstracts/mixins';

@import 'vendors/bootstrap';

@import 'base/reset';
@import 'base/typography';

@import 'layout/navigation';
@import 'layout/grid';
@import 'layout/header';
@import 'layout/footer';
@import 'layout/sidebar';
@import 'layout/forms';

@import 'components/buttons';
@import 'components/carousel';
@import 'components/cover';
@import 'components/dropdown';

@import 'pages/home';
@import 'pages/contact';

@import 'themes/theme';
@import 'themes/admin';
```