# ssh key 파일 여러 개 사용하기

`ssh-keygen`으로 ssh key 파일을 만들면 기본값으로 `~/.ssh/id_rsa`, `~/.ssh/id_rsa.pub` 파일이 생성되고, 어딘가 ssh 로 접근할 때 이 파일을 이용해서 접근하게 된다.

ssh key를 하나만 쓴다면 문제 없지만 ssh key를 여러 개 쓰려면 어떻게 설정해 줘야 할까?

다음과 같이 하면 된다.

1. ssh-key 를 `id_rsa`가 아닌 다른 이름(여기에서는 id_rsa_homoefficio)으로 생성하고,

>ssh-keygen -f ~/.ssh/id_rsa_homoefficio

2. `~/.ssh/config` 파일에 다음과 같이 따로 지정한다.

아래와 같이 하나의 호스트를 대상으로 여러 개의 ssh key 파일을 우선 순위에 따라 사용할 수 있다.

![Imgur](https://i.imgur.com/mxAKh2E.png)
