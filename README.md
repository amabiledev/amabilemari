# amabilemari
Projeto da disciplina de Iot Aplicada, do curso de Engenharia da Computação da UniSatc, solicitado pelo professor Vagner Rodrigues e desenvolvido pelas acadêmicas Amábile Freitas e Mariane Melo.

## Exercício Socket TCP Server
Projeto da disciplina de Iot Aplicada, do curso de Engenharia da Computação da UniSatc, solicitado pelo professor Vagner Rodrigues e desenvolvido pelas acadêmicas Amábile Freitas e Mariane Melo. Avaliação do desenvolvimento de uma aplicação que disponibilize as informações de temperatura, umidade e distância através de uma conexão socket TCP fornecida pelo ESP32.

## Antes de iniciar a parte da programação, é necessário ter o esquema com os seguintes componentes:
1 ESP 32
1 Sensor DHT11 (Sensor de temperatura e umidade)
1 Resistor 1.2k (Para o DHT11)
1 Sensor Ultrassônico
9 Jumpers (ou quantos forem necessários)

## Configuração dos primeiros passos do projeto:
1) Verificar a versão do SDK, precisa ser a ESP-IDF v4.1
2) Abrir o CMD do ESP-IDF
3) Copiar o caminho da pasta do projeto do seu computador, ex: cd "C:\esp-idf\examples\protocols\sockets\tcp_server"
4) Depois inserr o comando "idf.py menuconfig". Irá abrir este menu: 
![menu](https://user-images.githubusercontent.com/50503950/99743133-c787a400-2ab3-11eb-8adf-c69fd0ed0d47.png)
 
Devem-se fazer estas alterações:
4.1) Serial flasher config > Flash size (4 MB) > Salvar > ESC
4.2) Example Configuration > (3333) Port  > Salvar > ESC
4.3) Example Connection Configuration > (MeuWifi) Wi-fi SSID - (minhasenha) WiFi Password e desmarcar o "Obtain IPv6 link local address", porque nós usamos o IPv4 > Salvar > ESC
4.4) Salvar tudo e ESC para sair
5) Depois inserir no CMD do ESP_IDF o comando "idf.py flash monitor" para gravar o programa. (Em alguns casos se aparece “Conecting......connecting....” tem que pressionar o botão “boot” na placa). 
6) Assim, se tudo ocorrer bem é possível ver no CMD as seguintes informações:
![cmd](https://user-images.githubusercontent.com/50503950/99743126-c3f41d00-2ab3-11eb-9b62-e7d3b178de43.png)
 
Para testar com o cliente:
1) Abrir o RealTerm
2) Na aba port fazer essas alterações:
Em "Port"- n°doIP:n°port ex: 192.168.0.13:3333
Depois clicar em "open" para conectar
3) Na aba "Send" digitar a mensagem desejada e clicar em Send ASCII
![cliente](https://user-images.githubusercontent.com/50503950/99743134-c8203a80-2ab3-11eb-8d82-7a27be48b4a8.png)

4) Se o cliente enviar umas dessas mensagens: Temp, Umid ou Dist, ele receberá o retorno dos valores:
![print](https://user-images.githubusercontent.com/50503950/99743621-d1f66d80-2ab4-11eb-88c5-fa421b9a3010.jpeg)
 
## Fotos do esquema:
![esquema](https://user-images.githubusercontent.com/50503950/99743127-c5254a00-2ab3-11eb-874f-b0f7a677df4d.jpg)
![esquema2](https://user-images.githubusercontent.com/50503950/99743129-c6567700-2ab3-11eb-9b6e-52cfb445d51f.jpg)
