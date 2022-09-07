# Kubernetes_Training_Project
## Kubernetes MetalLB, Ingress, NFS, HPA 를 활용한 Training Project - 2022.09.07
#### [개발 내용 블로그](https://velog.io/@lijahong/0%EB%B6%80%ED%84%B0-%EC%8B%9C%EC%9E%91%ED%95%98%EB%8A%94-Kubernetes-%EA%B3%B5%EB%B6%80-%EC%A2%85%ED%95%A9-%EC%8B%A4%EC%8A%B5)

### Project 간단 정리 
![image](https://user-images.githubusercontent.com/69387517/188799546-5daaf890-63e6-4e2a-a929-ea69fe9b06b4.png)
> - 위와 같은 구조의 WEB 제공 서비스를 구현한다

### 구현 결과

#### curl 확인

![](https://velog.velcdn.com/images/lijahong/post/9a6cfe56-77a1-4856-8f20-d3f78c869778/image.png)
> - 해당 페이지의 html 내용을 잘 가져온다

#### Web 접속 확인

![](https://velog.velcdn.com/images/lijahong/post/1a9bbdd5-132f-45b8-b1a0-d5a1b2185db2/image.png)
> - /, /shop, /news 접속시 Ingress 를 통해 각각의 NodePort Service 에 연결되어 Pod 의 서비스가 잘 제공된다
> - NFS 를 통해 지정한 index.html 이 잘 출력된다

![](https://velog.velcdn.com/images/lijahong/post/c7c35134-e5da-4f13-8157-db06431175aa/image.png)
> - master Node 의 브라우저에서는 hosts 에 등록한 주소로 접속이 가능하다
> ![](https://velog.velcdn.com/images/lijahong/post/54fe7c18-87aa-4688-aa66-91a6a49508d6/image.png)
> - 다른 페이지도 모두 잘 접속된다
> 
> ![](https://velog.velcdn.com/images/lijahong/post/0151b291-8f70-4ed6-8c7b-ebd1ef9c837f/image.png)
