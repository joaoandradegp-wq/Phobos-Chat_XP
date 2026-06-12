<h1 align="center">💬 Phobos Chat XP</h1>

<p align="center">
Aplicação de chat peer-to-peer desenvolvida em Delphi 7 para comunicação em rede local utilizando sockets TCP/IP nativos do Windows.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Status-Legado-yellow">
  <img src="https://img.shields.io/badge/Linguagem-Delphi%207-blue">
  <img src="https://img.shields.io/badge/Tipo-Chat%20LAN-lightgrey">
</p>

---

<h2>📌 Sobre</h2>

<p>
O <b>Chat XP</b> foi desenvolvido como uma solução leve para comunicação direta entre computadores em rede local, sem necessidade de servidores externos, banco de dados ou internet.
</p>

<p>
A aplicação utiliza os componentes nativos <b>TServerSocket</b> e <b>TClientSocket</b> do Delphi para criar conexões TCP/IP entre dois computadores, permitindo comunicação em tempo real.
</p>

<p>
O sistema opera em modo cliente/servidor, onde uma máquina pode ficar aguardando conexões enquanto outra estabelece comunicação informando apenas o endereço IP da rede.
</p>

<p>
Além do envio de mensagens, o aplicativo também possui notificações sonoras, integração com a System Tray, alertas visuais e personalização da interface.
</p>

---

<h2>⚙️ Como funciona</h2>

<p>O funcionamento da aplicação ocorre em dois modos:</p>

<ul>
  <li><b>Modo Escuta (Servidor)</b>
    <ul>
      <li>A aplicação abre uma porta TCP/IP</li>
      <li>Fica aguardando conexões na rede</li>
      <li>Recebe mensagens em tempo real</li>
    </ul>
  </li>

  <li><b>Modo Conexão (Cliente)</b>
    <ul>
      <li>Usuário informa o IP do computador remoto</li>
      <li>A conexão TCP é estabelecida</li>
      <li>As mensagens passam a ser trocadas instantaneamente</li>
    </ul>
  </li>
</ul>

<p>
Todo o processo acontece utilizando comunicação direta via socket, sem dependência de serviços externos.
</p>

---

<h2>🧠 Recursos implementados</h2>

<p>Durante a execução, o sistema oferece:</p>

<ul>
  <li>Conexão cliente/servidor via TCP/IP</li>
  <li>Troca de mensagens em tempo real</li>
  <li>Modo escuta automático ao iniciar</li>
  <li>Notificações sonoras para novas mensagens</li>
  <li>Alertas visuais na bandeja do sistema</li>
  <li>Piscar do ícone TrayIcon ao receber mensagens</li>
  <li>Personalização de fonte e cor da interface</li>
  <li>Minimização para System Tray</li>
  <li>Controle de conexão/desconexão</li>
  <li>Bloqueio automático do campo de envio quando desconectado</li>
  <li>Status de conexão em tempo real</li>
</ul>

---

<h2>🌐 Comunicação em rede</h2>

<p>
A aplicação utiliza os componentes nativos de socket do Delphi:
</p>

<ul>
  <li><b>TServerSocket</b> → responsável por aguardar conexões</li>
  <li><b>TClientSocket</b> → responsável por conectar em outro host</li>
</ul>

<p>
Quando uma conexão é estabelecida:
</p>

<ul>
  <li>O endereço IP remoto é identificado</li>
  <li>O status da sessão é atualizado</li>
  <li>O campo de digitação é liberado automaticamente</li>
  <li>As mensagens passam a trafegar via socket TCP</li>
</ul>

---

<h2>🔔 Sistema de notificações</h2>

<p>
Um dos principais recursos implementados no sistema é o mecanismo de alertas de mensagens.
</p>

<p>Quando uma nova mensagem é recebida:</p>

<ul>
  <li>Um som WAV é reproduzido</li>
  <li>O horário da última mensagem é registrado</li>
  <li>O TrayIcon começa a piscar automaticamente</li>
  <li>O status visual da aplicação é atualizado</li>
</ul>

<p>
O usuário também pode desativar os alertas sonoros através da barra de ferramentas.
</p>

---

<h2>🖥️ Interface</h2>

<p>
A interface foi construída utilizando componentes VCL clássicos do Delphi 7.
</p>

<ul>
  <li>Área de mensagens recebidas</li>
  <li>Campo de envio de mensagens</li>
  <li>Status de conexão</li>
  <li>Toolbar com atalhos rápidos</li>
  <li>Menus de conexão e edição</li>
  <li>Popup menu da bandeja do sistema</li>
  <li>Indicadores visuais de atividade</li>
</ul>

---

<h2>🎨 Personalização</h2>

<p>O sistema permite personalização básica da interface:</p>

<ul>
  <li>Alteração de fonte</li>
  <li>Alteração de cor de fundo</li>
  <li>Seleção total do texto</li>
  <li>Funções de copiar, colar e recortar</li>
</ul>

<p>
As alterações são aplicadas dinamicamente durante a execução.
</p>

---

<h2>🧩 Integração com System Tray</h2>

<p>
A aplicação possui integração completa com a bandeja do sistema através do componente <b>abfTrayIcon</b>.
</p>

<p>Recursos disponíveis:</p>

<ul>
  <li>Minimizar sem fechar a aplicação</li>
  <li>Restaurar com duplo clique</li>
  <li>Alertas visuais por animação de ícone</li>
  <li>Menu rápido na bandeja</li>
</ul>

---

<h2>⚠️ Tratamento de erros</h2>

<p>
O sistema possui validações básicas de conexão e tratamento de falhas de rede.
</p>

<p>Entre os comportamentos implementados:</p>

<ul>
  <li>Exibição de erros de conexão</li>
  <li>Reconexão do modo escuta após desconexão</li>
  <li>Bloqueio do envio sem conexão ativa</li>
  <li>Reset automático do estado visual</li>
</ul>

---

<h2>🚀 Fluxo de utilização</h2>

<ol>
  <li>Abra a aplicação</li>
  <li>Escolha entre escutar ou conectar</li>
  <li>Informe o IP remoto (modo cliente)</li>
  <li>Aguarde a conexão</li>
  <li>Digite mensagens e pressione ENTER</li>
  <li>Receba notificações em tempo real</li>
</ol>

---

<h2>🛠️ Tecnologias</h2>

<ul>
  <li>Delphi 7</li>
  <li>VCL (Visual Component Library)</li>
  <li>TServerSocket / TClientSocket</li>
  <li>Windows API</li>
  <li>abfComponents</li>
  <li>TCP/IP Sockets</li>
</ul>

---

<h2>📸 Preview</h2>

<p align="center">
  <img width="465" height="459" alt="image" src="https://github.com/user-attachments/assets/9a7deba8-8a00-4fc6-9059-47ab2e6cc875" />
</p>

---

<p align="center">
Aplicação clássica de comunicação via intranet inspirado no Winpopup LAN Messenger. 🗨️
</p>
