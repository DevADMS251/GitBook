---
icon: stairs
---

# example: client code

```csharp
using System;
using System.Net.Sockets;
using System.Text;

class TcpClientExample
{
    static void Main()
    {
        // 서버의 IP 주소와 포트 번호를 설정합니다.
        string serverIp = "192.168.0.1";
        int port = 5000;

        // TcpClient 객체를 생성하여 서버에 연결을 시도합니다.
        TcpClient client = new TcpClient(serverIp, port);
        Console.WriteLine($"서버({serverIp}:{port})에 연결되었습니다.");

        // 네트워크 스트림을 통해 데이터 송수신을 수행합니다.
        NetworkStream stream = client.GetStream();

        // 서버로 전송할 메시지를 설정하고, UTF8 인코딩을 사용하여 바이트 배열로 변환합니다.
        string message = "안녕하세요, 서버님!";
        byte[] messageBytes = Encoding.UTF8.GetBytes(message);

        // 서버로 메시지를 전송합니다.
        stream.Write(messageBytes, 0, messageBytes.Length);
        Console.WriteLine($"서버로 메시지를 전송했습니다: {message}");

        // 서버로부터의 응답을 수신하기 위한 버퍼를 설정합니다.
        byte[] buffer = new byte[1024];
        int bytesRead = stream.Read(buffer, 0, buffer.Length);

        // 수신된 데이터를 UTF8 인코딩을 사용하여 문자열로 변환합니다.
        string response = Encoding.UTF8.GetString(buffer, 0, bytesRead);
        Console.WriteLine($"서버로부터 받은 응답: {response}");

        // 서버와의 연결을 종료합니다.
        client.Close();
        Console.WriteLine("서버와의 연결이 종료되었습니다.");
    }
}

```

