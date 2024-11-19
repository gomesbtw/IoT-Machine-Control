<h1 align="center">Controle Remoto de Máquinas com IoT</h1>

<p align="center">
  Este projeto utiliza IoT para controle remoto de máquinas em ambientes industriais. A comunicação é feita via protocolo MQTT, permitindo acionamento remoto e feedback de sensores em tempo real.
</p>

---

<h2>📚 Como reproduzir</h2>
<ol>
  <li>Baixe este repositório.</li>
  <li>Siga as instruções de hardware e software descritas abaixo.</li>
  <li>Carregue o código <code>codigo.ino</code> na plataforma ESP32 utilizando o Arduino IDE ou outra IDE compatível.</li>
  <li>Certifique-se de instalar as bibliotecas necessárias antes de compilar o código.</li>
</ol>

---

<h2>⚙️ Hardware utilizado</h2>
<ul>
  <li><b>ESP32</b> (Plataforma principal)</li>
  <li><b>LEDs</b> (Vermelho e Verde)</li>
  <li><b>Resistores</b> de 220 Ω</li>
  <li><b>Receptor IR</b></li>
  <li><b>SW-420</b> (Sensor de vibração)</li>
  <li><b>Controle IR</b> (Para comandos manuais)</li>
  <li><b>Protoboard</b></li>
  <li><b>Jumpers</b> (Macho-macho)</li>
</ul>

---

<h2>🔗 Comunicação</h2>
<ul>
  <li><b>Protocolo:</b> MQTT</li>
  <li><b>Broker:</b> Adafruit IO</li>
  <li><b>Mensagens publicadas:</b> <code>sensor/vibration</code> (detecção de vibração)</li>
  <li><b>Mensagens recebidas:</b> <code>command/led</code> (controle dos LEDs)</li>
</ul>

---

<h2>🌐 Configuração de Rede</h2>
<p>Edite o arquivo <code>codigo.ino</code> para inserir as credenciais de Wi-Fi e MQTT:</p>

```cpp
#define WIFI_SSID "SEU_SSID"
#define WIFI_PASSWORD "SUA_SENHA"
#define AIO_USERNAME "SEU_USUARIO_ADAFRUIT"
#define AIO_KEY "SUA_CHAVE_ADAFRUIT"
```
h2>📦 Configuração de Software</h2> <p>Instale as seguintes bibliotecas no Arduino IDE:</p> <ul> <li><b>IRremote:</b> Para comunicação infravermelha.</li> <li><b>Adafruit MQTT:</b> Para comunicação com o broker MQTT.</li> <li><b>WiFi:</b> Para conexão com redes Wi-Fi.</li> </ul> <p>Para instalar uma biblioteca:</p> <ol> <li>Abra o Arduino IDE.</li> <li>Vá em <b>Sketch → Incluir Biblioteca → Gerenciar Bibliotecas</b>.</li> <li>Pesquise pelo nome da biblioteca e clique em "Instalar".</li> </ol>
<h2>🚀 Funcionamento do Projeto</h2> <p>O sistema consiste nos seguintes módulos:</p> <ul> <li><b>Receptor IR:</b> Recebe comandos do controle remoto para ligar/desligar LEDs.</li> <li><b>Sensor de Vibração:</b> Detecta vibrações e envia um alerta ao broker MQTT.</li> <li><b>Broker MQTT:</b> Gerencia as mensagens entre a ESP32 e outros dispositivos.</li> <li><b>LEDs:</b> Indicadores visuais para ações manuais (controle remoto) ou automáticas (detecção de vibração).</li> </ul> <p>O fluxo básico de funcionamento é:</p> <ol> <li>O usuário pode enviar comandos via controle remoto ou pelo Adafruit IO para controlar os LEDs.</li> <li>O sensor de vibração monitora o ambiente e publica eventos no tópico MQTT <code>sensor/vibration</code>.</li> <li>O broker Adafruit IO retransmite esses eventos para sistemas conectados.</li> </ol>
<h2>👨‍💻 Autor</h2> <p>Projeto desenvolvido por <b>Luan Gabriel Ferreira</b>. Para dúvidas ou sugestões, entre em contato:</p> <ul> <li><b>Email:</b> luan.gab.f@gmail.com</li> <li><b>GitHub:</b> <a href="https://github.com/gomesbtw">https://github.com/gomesbtw</a></li> </ul> 
