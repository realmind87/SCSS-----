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

# components

```

_buttons.scss
_media.scss
_carousel.scss
_thumbnails.scss

```

# components

```

_home.scss
_contact.scss

```