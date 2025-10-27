# 📱 configApplication

![Status](https://img.shields.io/badge/status-active-brightgreen)
![Android](https://img.shields.io/badge/platform-Android-blue)
![Language](https://img.shields.io/badge/language-Kotlin-orange)
![License](https://img.shields.io/badge/license-MIT-lightgrey)
![Version](https://img.shields.io/badge/app_version-1.0-green)

O **configApplication** é um módulo de configuração utilizado em aplicações Android para gerenciar parâmetros dos ambientes de **Produção** e **Desenvolvimento** utilizando arquivos YAML.

---

## 🎯 Objetivo

Garantir que as configurações do app sejam centralizadas e separadas por ambiente, facilitando o ciclo de desenvolvimento e deploy.

---

## 📂 Estrutura do Projeto

| Ambiente | Arquivo |
|---------|---------|
| Desenvolvimento | `config-dev.yml` |
| Produção | `config-prod.yml` |

Os arquivos possuem sempre o mesmo nome base (**config**) e se diferenciam apenas pelo sufixo indicando o ambiente.

---

## 🧩 Conteúdo dos Arquivos

```yml
appVersion: "1.0"
apiHost: "http://tracker-device.com/"
clientId: "android"
urlNewVersionApp: ""
dataBaseVersion: 1
```

### 🔍 Propriedades

| Propriedade | Descrição |
|------------|-----------|
| `appVersion` | Versão da aplicação |
| `apiHost` | Host da API |
| `clientId` | Identificador do cliente |
| `urlNewVersionApp` | URL de atualização do app |
| `dataBaseVersion` | Versão do banco de dados local |

---

## 🌐 Alternância de Ambiente

Pode ser realizada utilizando:

✅ Build Variants e Flavors do Android  
✅ Variáveis de ambiente  
✅ Scripts de CI/CD  
✅ Copiando o arquivo do ambiente desejado no momento do build

---

## 🚀 Benefícios

- Melhor controle de versões e deploy
- Zero alteração no código ao trocar ambiente
- Configurações organizadas e escaláveis
- Menos riscos com configurações erradas em produção

---

## 🛠 Sugestão de Estrutura no Android

```
app/src/
 ├─ main/
 │   └─ assets/config-prod.yml
 ├─ dev/
 │   └─ assets/config-dev.yml
```

> O app deve selecionar automaticamente o arquivo conforme o flavor.

---

## ❤️ Autor

**configApplication** — Automatizando sua vida Android, uma config por vez 😄  
Gerado em: 27/10/2025 21:52:57

---

Se precisar, posso incluir:
✅ Script em Kotlin para ler o YML  
✅ Configuração completa de Flavors no build.gradle  
✅ Versão em inglês do README  

