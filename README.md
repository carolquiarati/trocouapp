# Trocou! 👶

Protótipo de app mobile para monitoramento de fralda inteligente — avisa em tempo real quando o bebê fez xixi ou cocô, com histórico de trocas e estatísticas do dia.

**[Ver demo ao vivo →](#)** *(link do GitHub Pages depois de publicar)*

![status](https://img.shields.io/badge/status-prot%C3%B3tipo-blue) ![tech](https://img.shields.io/badge/stack-HTML%20%2F%20CSS%20%2F%20JS-8FB996)

## Sobre o projeto

Este é o front-end de um sistema de monitoramento infantil baseado em IoT, desenvolvido como projeto acadêmico. A ideia completa envolve um sensor de umidade capacitivo conectado a um microcontrolador ESP32, que detecta quando a fralda está molhada e envia a informação via Wi-Fi para este app, notificando o responsável em tempo real.

Este repositório contém a interface do app — a camada que o usuário final vê e interage.

## Funcionalidades

- **Status em tempo real** — indicador visual com animação de pulso, mudando de cor conforme o tipo de evento detectado
- **Notificação simulada** — banner que replica o comportamento de uma notificação push, disparado a cada novo evento
- **Histórico de trocas** — lista cronológica com horário de cada troca
- **Estatísticas** — total de trocas no dia e tempo decorrido desde a última
- **Persistência local** — os dados continuam salvos mesmo depois de fechar e reabrir o navegador
- **Simulador de sensor** — como o hardware físico é uma etapa futura do projeto, os botões de simulação replicam o comportamento que o ESP32 teria ao detectar umidade

## Arquitetura planejada do sistema completo

```
Sensor de umidade (fralda) → ESP32 → Wi-Fi → Backend (Firebase/Node.js) → App (este repositório)
```

## Stack utilizada

- HTML5, CSS3 e JavaScript puro (sem frameworks — foco em performance e simplicidade)
- `localStorage` para persistência de dados no navegador
- Tipografia: Fraunces (display), Inter (corpo de texto) e IBM Plex Mono (dados/timestamps)

## Como rodar localmente

Não precisa de instalação — é um único arquivo HTML.

```bash
git clone https://github.com/SEU-USUARIO/trocou-app.git
cd trocou-app
# abra o index.html no navegador
```

## Próximos passos

- [ ] Integração real com hardware ESP32 via HTTP/MQTT
- [ ] Backend para receber e armazenar os eventos do sensor
- [ ] Notificações push reais (Firebase Cloud Messaging)
- [ ] Suporte a múltiplos bebês/perfis

## Autor

Projeto desenvolvido para fins acadêmicos.
