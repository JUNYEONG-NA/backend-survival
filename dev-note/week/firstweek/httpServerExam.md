## Http Server 실습 코드

    public class App {
        public static void main(String[] args) throws IOException {
            App app = new App();
            app.run();
        }

        private void run() throws IOException {
            // 1. Listen

            ServerSocket listener = new ServerSocket(8080, 0);

            System.out.println("Listen");

            // 2. Accept
            while (true) {
                Socket socket = listener.accept();

                System.out.println("Accept");

                // 3. Request 처리
                Reader reader = new InputStreamReader(socket.getInputStream());
                socket.getInputStream();

                CharBuffer charBuffer = CharBuffer.allocate(1_000_000);
                reader.read(charBuffer);

                charBuffer.flip();
                System.out.println(charBuffer.toString());

                // 4. Response

    //            String body = "Hello, world";
                String body = """
                        <!DOCTYPE html>
                        <html lang="ko">
                            <head>
                            <title>example</title>
                            </head>
                            <body>
                                <p> Hello, World! </p>
                            </body>
                        </html>
                                            
                        """;
                byte[] bytes = body.getBytes();

                String message = "" +
                        "HTTP/1.1 200 OK\n" +
                        "Content-Type: text/plain; charset=UTF-8\n" +
                        "Content-Length: " + bytes.length + "\n" +
                        "\n" +
                        body;


                Writer writer = new OutputStreamWriter(socket.getOutputStream());
                writer.write(message);
                writer.flush();

                // 4. Close

                socket.close();
            }
        }

    }
