<h1 align="center">Controle Remoto de Máquinas com IoT</h1>

<p align="center">
  Este projeto utiliza IoT para controle remoto de máquinas em ambientes industriais. A comunicação é feita via protocolo MQTT, permitindo acionamento remoto e feedback de sensores em tempo real.
</p>

---

<h2>📚 Como reproduzir</h2>
<ol>
  <li>Baixe este repositório.</li>
  <li>Siga as instruções de hardware e software descritas abaixo.</li>
  <li>Carregue o código na plataforma ESP32 utilizando o Arduino IDE ou outra IDE compatível.</li>
</ol>

---

<h2>⚙️ Hardware utilizado</h2>
<ul>
  <li><b>ESP32</b> (Plataforma principal)</li>
  <li><b>LEDs</b> (Vermelho e Verde)</li>
  <li><b>Resistores</b> de 220 Ω</li>
  <li><b>Receptor IR</b></li>
  <li><b>Protoboard</b></li>
  <li><b>SW-420</b></li>
  <li><b>Controle IR</b></li>
  <li><b>Jumpers</b> (Macho-macho)</li>
</ul>

<p>Detalhes do hardware e esquemas de ligação estão disponíveis no arquivo <code>HARDWARE.md</code>.</p>

---

<h2>🔗 Comunicação</h2>
<ul>
  <li><b>Protocolo:</b> MQTT</li>
  <li><b>Broker:</b> Adafruit IO</li>
  <li><b>Mensagens publicadas:</b> <code>sensor/vibration</code> (detecção de vibração)</li>
  <li><b>Mensagens recebidas:</b> <code>command/led</code> (controle dos LEDs)</li>
</ul>

<p>Configurações detalhadas do protocolo e das interfaces estão descritas no arquivo <code>COMMUNICATION.md</code>.</p>

---

<h2>🌐 Configuração de Rede</h2>
<ul>
  <li>Edite o arquivo <code>config.h</code> e insira as credenciais de Wi-Fi:</li>
</ul>

```cpp
define WIFI_SSID "SEU_SSID"
define WIFI_PASSWORD "SUA_SENHA"
#define AIO_USERNAME "SEU_USUARIO_ADAFRUIT"
#define AIO_KEY "SUA_CHAVE_ADAFRUIT"
```
<ul> <li>Certifique-se de que o Adafruit IO esteja configurado corretamente com suas credenciais MQTT:</li> </ul>
<h2>📁 Estrutura do Repositório</h2> <ul> <li><code>src/</code>: Contém os códigos-fonte do projeto.</li> <li><code>HARDWARE.md</code>: Detalhamento dos componentes de hardware e esquemas de montagem.</li> <li><code>COMMUNICATION.md</code>: Documentação dos protocolos e interfaces.</li> <li><code>README.md</code>: Este arquivo, com instruções gerais do projeto.</li> </ul>
<h2>📈 Métricas</h2> <p>Os tempos médios de resposta foram medidos para garantir a eficiência da comunicação:</p> <table align="center"> <thead> <tr> <th>Núm. Medida</th> <th>Sensor/Atuador</th> <th>Tempo de Resposta (ms)</th> </tr> </thead> <tbody> <tr> <td>1</td> <td>Sensor</td> <td>2 ms</td> </tr> <tr> <td>2</td> <td>Atuador</td> <td>2 ms</td> </tr> <tr> <td>3</td> <td>Sensor</td> <td>2 ms</td> </tr> <tr> <td>4</td> <td>Atuador</td> <td>2 ms</td> </tr> </tbody> </table>
<h2>👨‍💻 Autor</h2> <p>Projeto desenvolvido por <b>[Seu Nome]</b>. Para dúvidas ou sugestões, entre em contato:</p> <ul> <li><b>Email:</b> seuemail@dominio.com</li> <li><b>GitHub:</b> <a href="https://github.com/seuusuario">github.com/seuusuario</a></li> </ul>

