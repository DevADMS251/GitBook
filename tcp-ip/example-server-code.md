---
icon: stairs
---

# example: server code

```csharp
using System;
using System.Net;
using System.Net.Sockets;
using System.Text;

class TcpServer
{
    static void Main()
    {
        // 서버의 IP 주소와 포트 번호를 설정합니다.
        IPAddress ipAddress = IPAddress.Parse("192.168.0.1");
        int port = 5000;

        // TcpListener 객체를 생성하여 지정된 IP 주소와 포트에서 수신 대기합니다.
        TcpListener listener = new TcpListener(ipAddress, port);

        // 서버를 시작하여 클라이언트의 연결 요청을 받기 시작합니다.
        listener.Start();
        Console.WriteLine($"서버가 {ipAddress}:{port}에서 시작되었습니다.");

        while (true)
        {
            // 클라이언트의 연결 요청을 대기하고, 연결이 수락되면 TcpClient 객체를 반환합니다.
            TcpClient client = listener.AcceptTcpClient();
            Console.WriteLine("클라이언트가 연결되었습니다.");

            // 네트워크 스트림을 통해 데이터 송수신을 수행합니다.
            NetworkStream stream = client.GetStream();

            // 클라이언트로부터 데이터를 수신하기 위한 버퍼를 설정합니다.
            byte[] buffer = new byte[1024];
            int bytesRead = stream.Read(buffer, 0, buffer.Length);

            // 수신된 데이터를 UTF8 인코딩을 사용하여 문자열로 변환합니다.
            string message = Encoding.UTF8.GetString(buffer, 0, bytesRead);
            Console.WriteLine($"클라이언트로부터 받은 메시지: {message}");

            // 클라이언트에게 응답 메시지를 전송합니다.
            string response = "메시지를 받았습니다.";
            byte[] responseBytes = Encoding.UTF8.GetBytes(response);
            stream.Write(responseBytes, 0, responseBytes.Length);
            Console.WriteLine("클라이언트에게 응답을 전송했습니다.");

            // 클라이언트와의 연결을 종료합니다.
            client.Close();
            Console.WriteLine("클라이언트 연결이 종료되었습니다.");
        }
    }
}

```

