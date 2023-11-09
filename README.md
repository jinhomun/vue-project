# vue를 이용한 포트폴리오 사이트 만들기
VUE.JS는 현대적인 웹 애플리케이션을 개발하기 위한 JavaScript 프레임워크입니다. VUE.JS는 사용자 인터페이스를 구성하기 위해 사용되며, 컴포넌트 기반 아키텍처를 가지고 있습니다.

VUE.JS의 핵심 개념은 "반응형"입니다. 이는 데이터의 변화에 따라 자동으로 화면을 업데이트하여 사용자에게 동적인 경험을 제공하는 것을 의미합니다. VUE.JS는 데이터와 화면을 연결하기 위해 "바인딩"이라는 개념을 제공하며, 데이터의 변경이 화면에 자동으로 반영됩니다.

또한 VUE.JS는 가상 DOM(Virtual DOM)을 사용하여 효율적인 렌더링을 수행합니다. 가상 DOM은 실제 DOM과 동기화되어 화면을 업데이트하는 과정에서 최소한의 작업만 수행하여 성능을 향상시킵니다.

VUE.JS는 다른 JavaScript 라이브러리나 프레임워크와의 통합이 용이합니다. 필요한 경우 jQuery와 같은 라이브러리와 함께 사용할 수 있으며, 이미 존재하는 프로젝트에도 쉽게 통합할 수 있습니다.

또한 VUE.JS는 단일 파일 컴포넌트 구조를 지원하여 코드의 재사용성과 유지보수성을 높여줍니다. 이를 통해 개발자는 각각의 컴포넌트를 독립적으로 개발하고 테스트할 수 있으며, 필요한 경우 다른 프로젝트에서도 쉽게 재사용할 수 있습니다.

VUE.JS는 간단하고 직관적인 API를 가지고 있어 쉽게 배우고 사용할 수 있습니다. 또한 VUE CLI(Command Line Interface)를 통해 프로젝트를 구성하고 관리할 수 있으며, Vue Devtools와 같은 개발 도구를 제공하여 개발 과정을 보다 효율적으로 할 수 있습니다.

많은 회사와 개발자들이 VUE.JS를 사용하여 다양한 웹 애플리케이션을 개발하고 있으며, VUE.JS의 인기는 계속해서 증가하고 있습니다.

## 셋팅
`npm init vue@latest`
√ Project name: ... vue-project
   
√ Add TypeScript? ... <span style="color: blue">No</span> / Yes   
   
√ Add JSX Support? ... No / <span style="color: blue">YES</span>   
    
√ Add Vue Router for Single Page Application development? ... No / <span style="color: blue">YES</span>   
   
√ Add Pinia for state management? ... <span style="color: blue">No</span>/ Yes   
   
√ Add Vitest for Unit Testing? ... <span style="color: blue">No</span>/ Yes   
   
√ Add an End-to-End Testing Solution? » No    
   
√ Add ESLint for code quality? ... No / <span style="color: blue">YES</span> 
     
√ Add Prettier for code formatting? ... No /<span style="color: blue">YES</span>   
   

gsap 설치 :  `npm install gsap`   
sass 설치 : `npm install sass`   
lenis 설치 : `npm install @studio-freight/lenis`   

