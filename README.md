# 🌦️ Weather API

[![License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE)
[![Go Report Card](https://goreportcard.com/badge/github.com/robertoduessmann/weather-api)](https://goreportcard.com/report/github.com/robertoduessmann/weather-api)
[![GoDoc](https://godoc.org/github.com/robertoduessmann/weather-api?status.svg)](https://godoc.org/github.com/robertoduessmann/weather-api)

> A REST API to check the current weather.

API REST desenvolvida em Go para consultar informações meteorológicas por cidade, com exemplos de temperatura, vento, descrição do clima e previsão do tempo.

## 📑 Sumário

- [Visão geral](#-visão-geral)
- [Endpoints](#-endpoints)
- [Pré-requisitos](#-pré-requisitos)
- [Instalação e execução](#-instalação-e-execução)
- [Utilização](#-utilização)
- [Exemplo de resposta](#-exemplo-de-resposta)
- [Clientes web](#-clientes-web)
- [Licença](#-licença)

## 🌍 Visão geral

O `weather-api` oferece endpoints HTTP para consulta de informações meteorológicas por cidade.

## 🔗 Endpoints

### API pública

**Consultar o clima de uma cidade**

```http
GET https://goweather.xyz/v2/weather/{city}
```

Exemplo para Berlim:

```http
GET https://goweather.xyz/v2/weather/Berlin
```

Substitua `{city}` pelo nome da cidade desejada.

> A disponibilidade atual do serviço público não foi verificada. Os endereços acima refletem as URLs registradas no projeto.

### API local

Quando a aplicação estiver em execução localmente:

```http
GET http://localhost:3000/weather/{city}
```

## 🛠️ Pré-requisitos

- Go instalado no ambiente.
- Git para clonar o repositório.

## 🚀 Instalação e execução

### 1. Clone o repositório

```bash
git clone https://github.com/robertoduessmann/weather-api.git
cd weather-api
```

### 2. Compile o projeto

```bash
go build
```

### 3. Execute a aplicação

No macOS ou Linux:

```bash
./weather-api
```

No Windows, caso o executável gerado seja `weather-api.exe`:

```powershell
.\weather-api.exe
```

## 📡 Utilização

Faça uma requisição à API local utilizando `curl`:

```bash
curl http://localhost:3000/weather/Curitiba
```

Para consultar o endpoint público:

```bash
curl https://goweather.xyz/v2/weather/Curitiba
```

## 📦 Exemplo de resposta

Exemplo ilustrativo do formato JSON documentado no projeto:

```json
{
  "temperature": "29 °C",
  "wind": "20 km/h",
  "description": "Partly cloudy",
  "forecast": [
    {
      "day": "1",
      "temperature": "27 °C",
      "wind": "12 km/h"
    },
    {
      "day": "2",
      "temperature": "22 °C",
      "wind": "8 km/h"
    }
  ]
}
```

### Descrição dos campos

| Campo | Descrição |
|---|---|
| `temperature` | Temperatura atual. |
| `wind` | Velocidade do vento. |
| `description` | Descrição das condições meteorológicas. |
| `forecast` | Lista de previsões. |
| `forecast[].day` | Identificador do dia previsto. |
| `forecast[].temperature` | Temperatura prevista. |
| `forecast[].wind` | Velocidade do vento prevista. |

**Nota:** os valores apresentados são exemplos e não representam dados meteorológicos em tempo real.

## 🖥️ Clientes web

Projetos de clientes web listados na documentação original. A compatibilidade atual com a API precisa ser confirmada.

### 1. React Tempo

- **Aplicação:** https://reacttempo.netlify.app/
- **Repositório:** https://github.com/GabrielCampos99/appTempo

### 2. Weather App

- **Aplicação:** https://emaniaditya.github.io/weather-app
- **Repositório:** https://github.com/emaniaditya/weather-app/

### 3. Weather React TSX

- **Aplicação:** https://weather-react-tsx.netlify.app/
- **Repositório:** https://github.com/keissiant/weather-api-react.tsx

## 🤝 Contribuição

Contribuições para a documentação e o código são bem-vindas.

1. Faça um fork do repositório.
2. Crie uma branch para sua alteração.
3. Implemente e teste as mudanças.
4. Envie um pull request com uma descrição clara.

Consulte as orientações existentes no repositório antes de contribuir.

## 📄 Licença

Este projeto utiliza a licença MIT, conforme indicado na documentação original.

Consulte o arquivo [LICENSE](LICENSE) para acessar os termos completos.

## 🔗 Repositório

Código-fonte: https://github.com/robertoduessmann/weather-api
