# 🧱 brlobby

**brlobby** é um plugin completo de lobby para servidores Minecraft com suporte a múltiplos mundos. Ele oferece uma experiência moderna e personalizável, ideal para servidores de minigames, hubs ou redes maiores.

## ✨ Recursos

- ✅ Suporte a múltiplos mundos de lobby
- ✅ Comando `/setlobby` para definir o ponto de lobby
- ✅ Teleporte automático ao entrar no mundo de lobby
- ✅ Itens personalizados no inventário:
  - 🧭 Bússola (*Minigames*)
  - 🧑 Cabeça do jogador (*Perfil*)
  - 💎 Esmeralda (*Loja*)
  - 🔍 Item de visibilidade (mostrar/ocultar jogadores)
- ✅ Sistema de visibilidade entre jogadores no lobby
- ✅ Scoreboard com informações úteis e personalizáveis
- ✅ Arquivo de configuração completo (`config.yml`)
- ✅ Suporte a placeholders básicos
- ✅ Compatível com versões 1.8+

---

## 📦 Instalação

1. Baixe o plugin `brlobby.jar`.
2. Coloque o arquivo na pasta `plugins/` do seu servidor.
3. Reinicie ou recarregue o servidor.

---

## ⚙️ Comandos

| Comando | Permissão | Descrição |
|--------|------------|-----------|
| `/setlobby` | `brlobby.setlobby` | Define a localização atual como lobby do mundo |
| `/lobby` | `brlobby.lobby` | Teleporta o jogador para o lobby definido |
| `/brlobby reload` | `brlobby.admin` | Recarrega a configuração do plugin |

---

## 🗂️ Configuração

O arquivo `config.yml` permite personalizar:

```yaml
# Exemplo de configuração
lobby:
  enabled: true
  location:
    world: "lobby"
    x: 0.5
    y: 100.0
    z: 0.5
    yaw: 0
    pitch: 0

items:
  compass:
    slot: 0
    name: "&aMinigames"
    command: "/minigames"
  profile:
    slot: 4
    name: "&bSeu Perfil"
    command: "/perfil"
  shop:
    slot: 7
    name: "&aLoja"
    command: "/loja"
  visibility:
    slot: 8
    enabled_name: "&eOcultar Jogadores"
    disabled_name: "&eMostrar Jogadores"

scoreboard:
  title: "&6&lLOBBY"
  lines:
    - "&7&m------------------"
    - "&fOnline: &a%online%"
    - "&fLobby: &b%lobby_name%"
    - "&fSite: &cseusite.com.br"
    - "&7&m------------------"
