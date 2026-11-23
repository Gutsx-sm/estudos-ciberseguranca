# 🛡️ Diário de Estudos em Cibersegurança

Bem-vindo ao meu repositório de estudos! Comecei minha jornada aos 13 anos com o objetivo de construir uma base sólida em tecnologia, redes e segurança da informação, mirando uma carreira internacional no futuro.

## 🎯 Objetivos Atuais
- [ ] Concluir o curso *Introdução à Cibersegurança* (Cisco NetAcad)
- [ ] Aprender os fundamentos de Redes (IP, DNS, HTTP/HTTPS)
- [ ] Dar os primeiros passos no terminal Linux e Windows
- [ ] Iniciar lógica de programação com Python

## 📅 Registro de Progresso

### Dia 01 - O Início
- Criei meu repositório no GitHub para documentar minha evolução.
- Aprendi como funciona a base da internet: Cliente/Servidor, IP, DNS e HTTP/HTTPS.
- Testei meus primeiros comandos no terminal (`ping` e `whoami`).

---
*“A consistência vence a intensidade.”*

## 📅 Dia 1 de estudos — Data: 23/11/2026

Hoje eu aprendi sobre **Cliente e Servidor**, **IP (IPv4 e IPv6)**, **DNS**, **HTTP/HTTPS**, **Firewall** e **Latência (ms)**.

Imagine que a internet é um grande **sistema de entregas de comida**:

### 1. Cliente e Servidor (Você vs. O Restaurante)
- **Cliente:** É o seu celular ou computador (quem faz o pedido). Quando você abre o TikTok ou o Google, seu navegador é o cliente.
- **Servidor:** É um supercomputador ligado 24 horas por dia em algum lugar do mundo que guarda os vídeos, sites e dados (o restaurante que prepara e entrega o pedido).

### 2. Endereço IP: IPv4 e IPv6 (O CEP da Casa)
- Para o restaurante entregar sua comida, ele precisa do seu endereço exato. Na internet, todo aparelho conectado ganha um código único chamado **Endereço IP**. Sem ele, os servidores não saberiam para qual computador enviar os sites ou vídeos pedidos.
- **IPv4:** É a versão clássica do IP, formada por 4 blocos de números separados por pontos (exemplo: `192.168.0.15` ou `8.8.8.8`). Como o número de aparelhos conectados no mundo explodiu, os endereços IPv4 acabaram.
- **IPv6:** É a versão moderna criada para substituir o IPv4. Ele usa números e letras separados por dois-pontos (exemplo: `2800:3f0:4001:808::200e`) e permite uma quantidade quase infinita de endereços na internet.

### 3. DNS (A Agenda Telefônica)
- Ninguém decora números como `142.250.219.14` para entrar no Google. Nós digitamos `google.com`.
- O **DNS** (*Domain Name System*) é o sistema que traduz o nome do site (`google.com`) para o número IP verdadeiro do servidor dele. Quando você digita um site, seu PC pergunta ao DNS: *"Qual é o IP do google.com?"*, pega o endereço e faz a conexão.

### 4. HTTP e HTTPS (O Idioma e o Caminhão Blindado)
- **HTTP:** É a regra (protocolo) de como o seu navegador e o servidor conversam para pedir e entregar páginas web. O problema do HTTP antigo é que os dados viajam "abertos" — se um hacker interceptar sua rede Wi-Fi, ele lê tudo o que você digitou (inclusive senhas).
- **HTTPS (com o "S" de *Secure*):** É o HTTP dentro de um caminhão-forte. Ele usa **criptografia** para embaralhar toda a conversa entre você e o site. Mesmo que alguém intercepte os dados no meio do caminho, só verá códigos embaralhados impossíveis de ler (é aquele cadeado ao lado do endereço do site no navegador).

### 5. Outros Conceitos Importantes
- **Latência (Ping / ms):** É o tempo de atraso que um pacote de dados leva para sair do meu computador, chegar até um servidor e voltar. É medida em milissegundos (`ms`). Quanto menor o número, mais rápida e responsiva é a conexão (essencial tanto para jogos quanto para testes de rede).
- **Firewall (Parede de Fogo):** É um sistema de segurança (pode ser um programa no PC ou um equipamento físico na rede) que funciona como um "segurança de balada". Ele analisa todo o tráfego de dados que tenta entrar ou sair e decide o que passa e o que é bloqueado com base em regras de segurança (como vimos no Salto 2 do comando `tracert`, onde o roteador bloqueou a resposta).

---

### Parte 2 (Ainda no dia 23/11/2026) — Portas de Rede e VPN

#### 6. Portas de Rede (Os Apartamentos do Prédio)
- Se o **Endereço IP** é o endereço do prédio (o servidor), a **Porta de Rede** é o número do apartamento (o programa ou serviço específico dentro daquele servidor).
- Um computador possui **65.535 portas** numeradas para organizar as conexões.
- **Portas mais importantes que aprendi:**
  - **Porta 80:** Usada para tráfego web comum (**HTTP**).
  - **Porta 443:** Usada para tráfego web seguro e criptografado (**HTTPS**).
  - **Porta 22:** Usada para acesso remoto seguro via terminal (**SSH**).
- *Importância na segurança:* Analistas e hackers escaneiam portas abertas para descobrir quais serviços estão rodando em um servidor e se algum está vulnerável.

#### 7. VPN — Virtual Private Network (O Túnel Secreto)
- É uma tecnologia que cria um **túnel criptografado** entre o meu dispositivo e um servidor seguro da VPN antes de acessar a internet.
- **Privacidade no Wi-Fi:** Impede que pessoas na mesma rede (como Wi-Fi público) ou a operadora de internet espionem os dados que estou enviando.
- **Mascaramento de IP:** O site final enxerga o IP do servidor da VPN em vez do meu IP residencial real.

---

### Parte 3 (Ainda no dia 23/11/2026) — Criptografia

#### 8. O que é Criptografia?
- É o processo de embaralhar informações legíveis (**Texto Claro**) em códigos incompreensíveis (**Texto Cifrado**) para que apenas pessoas autorizadas consigam ler, usando uma **Chave** matemática.

#### 9. Criptografia Simétrica vs. Assimétrica
- **Criptografia Simétrica (Chave Única):** Usa a **mesma chave** para trancar e destrancar a mensagem. É muito rápida, mas tem o risco de alguém interceptar a chave na hora de enviá-la para a outra pessoa.
- **Criptografia Assimétrica (Par de Chaves):** Usa duas chaves diferentes:
  - **Chave Pública:** Pode ser compartilhada com qualquer pessoa; serve apenas para **trancar** (criptografar) os dados.
  - **Chave Privada:** Fica em segredo absoluto com o dono; é a única capaz de **destrancar** (descriptografar) o que foi fechado com a Chave Pública.
- *Uso real:* O protocolo **HTTPS** usa criptografia assimétrica no início da conexão para trocar chaves com segurança, e depois usa criptografia simétrica para transmitir os dados do site rapidamente.
