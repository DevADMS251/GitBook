---
icon: lightbulb-exclamation-on
---

# TCP/IP

## ⁉️TCP/IP란 무엇입니까?

* 컴퓨터 네트워크에서 정보를 주고받기 위해 사용되는 통신 프로토콜의 모음
* TCP (Transmission Control Protocol)는 데이터의 신뢰성 있는 전달을 보장
* IP (Internet Protocol)는 패킷의 주소 지정과 라우팅을 담당
* TCP/IP 모델은 두 개의 기기 간에 데이터를 전송하는 것을 담당

***

## ⁉️TCP/IP: 4계층

<figure><img src=".gitbook/assets/그림6.png" alt=""><figcaption></figcaption></figure>

* L4 응용 계층 (Application Layer)
  * 역할: 응용 프로그램 간 데이터 송수신을 지원하며, 사용자와 직접 상호 작용하는 서비스를 제공합니다.
  * 주요 기능:
    * 데이터 표현 및 변환
    * 응용 프로토콜을 통한 통신
    * 관련 프로토콜: HTTP, FTP, SMTP, DNS 등



* L3 전송 계층 (Transport Layer)
  * 역할: 호스트 간 신뢰성 있는 데이터 전송을 보장하며, 데이터의 전달을 확인하고 오류를 수정합니다.
  * 주요 기능:
    * 데이터 세그먼트화 및 재조립
    * 흐름 제어 및 오류 검출
    * 관련 프로토콜: TCP, UDP



* L2 인터넷 계층 (Internet Layer)
  * 역할: 데이터를 패킷으로 나누어 논리적 주소(IP 주소)를 사용하여 목적지까지 전달하며, 네트워크 간의 데이터 전송과 라우팅을 담당합니다.
  * 주요 기능:
    * IP 주소를 통한 패킷의 주소 지정 및 경로 설정
    * 네트워크 간 라우팅
    * 관련 프로토콜: IP, ARP, ICMP, RARP 등



* L1 네트워크 엑세스 계층 (Network Access Layer)
  * 역할: 데이터를 실제 네트워크 매체를 통해 전송하는 방법을 정의합니다. OSI 모델의 물리 계층과 데이터 링크 계층의 기능을 포함합니다.
  * 주요 기능
    * 물리적 주소(MAC 주소)를 사용하여 장치 간 데이터 링크 설정
    * 데이터 프레임화 및 오류 검출
    * 관련 프로토콜: Ethernet 등
