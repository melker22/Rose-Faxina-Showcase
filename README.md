<p align="center">
  <img src="docs/logo.png" alt="Rose Faxina" width="120" />
</p>

<h1 align="center">Rose Faxina — Showcase</h1>

<p align="center">
  <strong>Limpeza residencial com carinho</strong><br />
  Marketplace que conecta clientes, profissionais de confiança e a equipe admin.
</p>

<p align="center">
  <img alt="Kotlin" src="https://img.shields.io/badge/Kotlin-2.1-7F52FF?style=flat-square&logo=kotlin&logoColor=white" />
  <img alt="Compose Multiplatform" src="https://img.shields.io/badge/Compose-Multiplatform-4285F4?style=flat-square&logo=jetpackcompose&logoColor=white" />
  <img alt="Ktor" src="https://img.shields.io/badge/Ktor-3.1-00AFD8?style=flat-square" />
  <img alt="PostgreSQL" src="https://img.shields.io/badge/PostgreSQL-16%20%2B%20PostGIS-4169E1?style=flat-square&logo=postgresql&logoColor=white" />
  <img alt="Redis" src="https://img.shields.io/badge/Redis-7-DC382D?style=flat-square&logo=redis&logoColor=white" />
  <img alt="Android" src="https://img.shields.io/badge/Android-8.0%2B-3DDC84?style=flat-square&logo=android&logoColor=white" />
  <img alt="LGPD" src="https://img.shields.io/badge/LGPD-consentimentos-D080B0?style=flat-square" />
</p>

> Repositório **público de vitrine**. O código do app fica em um repositório privado. Aqui você vê o que o produto é, a stack e o site.

---

## Sobre

O **Rose Faxina** é um marketplace de limpeza residencial. O cliente pede a faxina e paga no app; profissionais próximos recebem a oferta; o primeiro aceite captura o pagamento; o acompanhamento é em tempo real.

| Papel | O que faz |
|--------|-----------|
| **Cliente** | Cadastra, aceita LGPD, solicita faxina, paga (PIX ou cartão), acompanha e avalia |
| **Faxineiro(a)** | Fica online, recebe ofertas no raio, aceita o pedido, atualiza o status e compartilha GPS |
| **Admin** | Pedidos, disputas, precificação e estatísticas — no app e no painel web |

| Plataforma | Status |
|------------|--------|
| **Android** | App principal (Compose Multiplatform) |
| **iOS** | Módulo shared preparado |
| **Admin web** | Painel servido pelo backend |

Site: [Rose-Faxina-Site](https://github.com/melker22/Rose-Faxina-Site)

---

## Funcionalidades

- Precificação por m², cômodos, banheiros e extras
- Pagamento no app via **Mercado Pago** (PIX + cartão)
- Ofertas geográficas para faxineiros (raio configurável)
- Rastreamento em tempo real (WebSocket + mapa no Android)
- Disputas, LGPD (consentimentos, exportação e exclusão)
- Sessão segura no Android

---

## Stack

| Camada | Tecnologia |
|--------|------------|
| Linguagem | Kotlin 2.1 · JDK 17 |
| UI | Compose Multiplatform · Material 3 |
| App Android | minSdk 26 · Koin · Google Maps |
| API | Ktor · JWT · Flyway · Exposed |
| Dados | PostgreSQL 16 + PostGIS · Redis 7 · Docker |
| Pagamentos | Mercado Pago Checkout Transparente |

---

## Arquitetura (visão)

```text
App (KMP / Compose)  →  API Ktor (JWT)  →  PostgreSQL + PostGIS
                                      →  Redis
Android: Maps + GPS em foreground
```

---

## Design

Paleta (tokens da marca):

| Token | Hex | Uso |
|-------|-----|-----|
| Fundo | `#FCEEF5` | Telas |
| Primário | `#D080B0` | Marca |
| CTA | `#B84472` | Botões |
| Texto | `#161516` | Títulos |

Mascote **Rosita** e identidade visual alinhadas ao negócio Rose Faxina.

---

## Autor

[Melker Halberd Pereira Alves](https://github.com/melker22) · Mineiros, GO

---

## Licença

Código-fonte do app: **privado** (todos os direitos reservados).  
Este showcase (README e assets públicos): documentação de portfólio — sem liberar o código do produto.
