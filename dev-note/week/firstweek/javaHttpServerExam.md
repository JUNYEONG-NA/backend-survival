## java HTTP Server 실습 코드

    public class App {
        public static void main(String[] args) throws IOException {
            App app = new App();
            app.run();
        }

        private void run() throws IOException {
            InetSocketAddress address = new InetSocketAddress(8080);
            HttpServer httpServer = HttpServer.create(address, 0);

    //        HttpHandler handler;
            httpServer.createContext("/", exchange -> {
                // 1. Request

                String method = exchange.getRequestMethod();
                System.out.println("method : " + method);

                URI uri = exchange.getRequestURI();
                String path = uri.getPath();
                System.out.println("Path : " + path);

                Headers headers = exchange.getRequestHeaders();
                for (String key : headers.keySet()) {
                    List<String> values = headers.get(key);
                    System.out.println(key + " : " + values);

                }

                InputStream inputStream = exchange.getRequestBody();
    //            byte[] bytes = inputStream.readAllBytes();
    //            String body = new String(bytes);
                String body = new String(inputStream.readAllBytes());
                System.out.println(body);
                // 2. Response


                String content = "hello, world!";
                byte[] bytes = content.getBytes();

                exchange.sendResponseHeaders(200, bytes.length);
                OutputStream outputStream = exchange.getResponseBody();
                outputStream.write(bytes);
                outputStream.flush();

                // 3.
            });


            httpServer.start();
        }
    }