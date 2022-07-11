(https://stackoverflow.com/questions/8772746/difference-between-framework-vs-library-vs-ide-vs-api-vs-sdk-vs-toolkits)
https://you9010.tistory.com/147

```IDE```는 Integrated Development Environment로, 여러가지 기능들이 포함되어있는 텍스트 에디터. Eclipse, Visual Studio Code 등이 있다.

--

```Library```는 우리가 어떤 기능을 하기 위해 일일이 프로그램 코드를 작성할 필요 없이, 빠르고 쉽게 그 기능을 수행할 수 있도록 하는 Chunk of Code다. 우리가 개발할 때,

동적/정적으로 라이브러리를 추가해서 그 안에 있는 함수들을 call함으로써 사용한다.

--

```API```는 Application Programming Interface로, 라이브러리 안의 함수/메소드 를 의미한다. 즉, 라이브러리에 대한 인터페이스.

--

```SDK```는 Software Development Kit으로, 하나 혹은 여러개의 라이브러리를 포함하며, extra tool application, data files, sample code 등도 종종 포함된다.

특정한 시스템(Windows, DirectX, Arduino 등)을 사용할 때 개발을 도와준다. 여전히 하나의 기능을 제공하는데 포커스가 맞춰져 있다.

--

```framework```는 큰 라이브러리 혹은 엄청 많은 라이브러리들의 모음이다. 보통 라이브러리와 SDK와는 달리 단일 서비스를 제공하는게 아니라 많은 서비스를 제공하는데

초점이 맞춰져있다. ex. 닷넷(.NET)같은 경우에는 application을 만들기 위해 필요한 모든 기능들을 다 가지고 있다. 그리고 이미 사전에 구현되어있는 이 프레임워크는

우리가 코드를 call하는 라이브러리와 달리, 프레임워크 차원에서 부르게 될 callback 함수 등을 우리가 구현함으로써, 프레임워크가 call할 수 있게 해준다.

누가 누구를 호출하느냐는 차이가 있다.
