# 해외망을 여행하는 히치하이커를 위한 안내서

가끔씩 해외망을 이용한 다운로드에서 미쳐버린 속도를 경험하신 적이 있나요? 몇메가 되지도 않는 파일을 몇 분 동안 다운로드 받아보신 적이 있나요? 좋아요. 제대로 찾아오셨습니다.

공유기의 문제 같다고요? 그럴 수도 있지만, 아마 아닐겁니다. 랜카드의 문제라고요? 그럴 수도 있지만, 아마 그 것도 아닐겁니다. 뭔 병신같은 소리냐구요? 애초에 우리들의 친구인 ISP가 처음부터 해외망 속도를 박살내놨으니까요! 와!!!

하지만 이제 걱정하지 마세요. 해외망 연방의 의뢰로 2077-14-42에 제작된 이 안내서는 새로운 워프 방식을 이용해 광속으로 해외망을 여행할 수 있는 방법을 알려줍니다.

## 준비물

- wireguard
	- [https://www.wireguard.com/](https://www.wireguard.com/)
	- 미리 설치해두세요
- wgcf
	- [https://github.com/ViRb3/wgcf](https://github.com/ViRb3/wgcf)

## 시작하기

### 1.1.1.1 warp?

> [https://blog.cloudflare.com/1111-warp-better-vpn/](https://blog.cloudflare.com/1111-warp-better-vpn/)

새로운 워프 방식의 시작이자 끝입니다

### 1. wgcf로 1.1.1.1 warp 등록 및 프로파일 생성

`1.1.1.1 warp`는 아직 PC 환경을 지원하지 않습니다. 직접 등록하고 `wireguard`에 쓰일 프로파일을 만들어야 합니다.
 
> [https://github.com/ViRb3/wgcf/releases](https://github.com/ViRb3/wgcf/releases)

위의 링크로 들어가 자신의 환경에 맞는 `wgcf`를 받아주세요. 요즘 사용되는 대부분의 컴퓨터는 `windows_amd64`를 다운받으면 됩니다.

#### 1.1.1.1 warp 등록

> 리빙포인트) 터미널에서 사용되는 `wgcf`는 다운받은 wgcf 파일의 이름입니다

```
wgcf register
```
`Do you agree?`가 보인다면 YES를 선택하세요.

`Successfully created Cloudflare Warp account`가 보이나요? 축하합니다. 성공했습니다! 와!!!

#### wireguard에 쓰일 프로파일 생성

위의 과정으로 아마 `.toml` 파일이 만들어졌을겁니다. 그런데 그 것만으로는 warp의 은총을 받을 수 없어요.  `wgcf`로 하나만 더 해봅시다.

```
wgcf generate
```
됐나요? ` Successfully generated WireGuard profile: wgcf-profile.conf`가 보인다면 드디어 새로운 워프 방식을 사용할 준비가 된겁니다. 이제 `wireguard`에 연결만 해주면 됩니다.

### wireguard 연결
![](https://i.ibb.co/NFsVMbM/1.png)

먼저 `wireguard`를 열어 `Add Tunnel`을 클릭해주세요. 그 다음 만들어진 `.conf`를 선택하면 됩니다. 끝입니다. 그냥 `Activate`만 눌러주세요.

축하합니다. 여러분들은 이제 진정한 해외망을 여행하는 히치하이커가 되셨습니다.

## 살짝 꿀팁

- ISP도 무시하는데 다른 건 안되겠나요? 지금 생각하는 그거 맞습니다. 행복한 시간 보내세요^^~
