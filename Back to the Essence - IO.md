# Back to the Essence - I/O

I/O가 뭔지 어떻게 동작하는지 아주 옛날에 잠시 찾아봤을 뿐이고, 그 후로 꽤 오랫동안 별 생각없이 그냥 언어나 라이브러리에서 제공해주는 API를 사용해오기만 하다보니, 어디선가 약간의 로우 레벨 내용이 나오면 잘 모르겠더라능..

그래서 저수준의 내용을 다루는 글을 보더라도 어색하지 않도록 이쯤에서 되짚어보려 한다.

찾다보니 [How Java I/O Works Internally at Lower Level?](https://howtodoinjava.com/java/io/how-java-io-works-internally-at-lower-level/) 이 글만한 것이 없는 것 같다. 한땀한땀 원문 그대로 번역하는 것이 귀찮아서 그냥 서술했지만, 대부분의 내용은 이 글에서 가져왔다고 봐도 무방하다.

## I/O란?

조금 추상적일 수 있지만 다음 표현이 적절한 것 같다.

>I/O(Input/Output, 입/출력)은 하나의 컴퓨터와 그 컴퓨터를 제외한 세상 모든 것과의 인터페이스다.
>
>또는
>
>I/O는 하나의 프로그램과 그 프로그램이 실행되는 컴퓨터의 나머지 모든 것과의 인터페이스다.

(출처: https://howtodoinjava.com/java/io/difference-between-standard-io-and-nio/)

좀 없어보이기는 해도 쉽게 말하면 서로 다른 주체 사이의 통신이라고 봐도 크게 틀리지 않을 것 같다.

## Buffer

일반적으로 버퍼는 물리적 충격을 완화하는 완충장치를 의미한다. 전산에서는 물리적 충격이 아니라 양이나 속도의 차이를 완화하는 역할을 하는 것을 버퍼라고 부른다.

I/O가 `서로 다른 주체 사이`의 `통신`이라고 했는데, `서로 다른 주체 사이`에는 처리할 수 있는 양이나 속도에 차이가 있다. 그래서 I/O가 효율적으로 원활히 처리되려면 둘 사이의 차이를 완화해 줄 수 있는 버퍼가 필수다. `통신`을 정보의 이동이라고 본다면 결국 버퍼에 정보를 넣고 빼는 것이 I/O 처리의 시작이라고 볼 수 있다.

----

이건 따로 정리하려면 일이 너무 커질 것 같아서 잘 정리된 문서 링크 모아두는 걸로 쫑내자..

https://cs.nyu.edu/~gottlieb/courses/2000s/2002-03-fall/os/lectures/lecture-13.html

https://howtodoinjava.com/java/io/how-java-io-works-internally-at-lower-level/

https://howtodoinjava.com/java7/nio/java-nio-2-0-working-with-buffers/

https://howtodoinjava.com/java-io-tutorial/

https://www.javacodegeeks.com/2012/08/io-demystified.html

https://slideplayer.com/slide/10013778/



