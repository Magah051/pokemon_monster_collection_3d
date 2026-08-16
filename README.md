# Pokémon Monster Collection 3D

*Protótipo 3D de exploração com coleção de criaturas estilo Pokémon, desenvolvido em **C#** com a engine **Unity** (HDRP). O jogador se move em um cenário low-poly, com animação e pets/NPCs Pokémon no mundo. Diversos conceitos foram aplicados aqui, dentre eles:*

- Movimento 3D relativo à câmera (`CharacterMovement`)
- Input do player (`Playerinput`)
- Animações via componente `Animate`
- Modelos 3D de Pokémon (Beedrill, Butterfree, Cyndaquil, Scyther)
- Integração com assets low-poly de natureza/cidade
- Importação de modelos (Sketchfab For Unity)

---

## Sobre o projeto

Cenário 3D de estudo/protótipo em que o player caminha pelo mapa com movimento baseado na direção da câmera, rotação suave (Slerp) e animação de locomotion. Foram adicionados Pokémon como NPCs/pets próximos ao jogador.

## Tecnologias

| Item | Detalhe |
|------|---------|
| Engine | Unity **2022.3.16f1** (LTS) |
| Linguagem | C# |
| Render | **HDRP** |
| Modelos | Sketchfab + packs low-poly |

## Estrutura do projeto

```
pokemon_monster_collection_3d/
├── Assets/
│   ├── Scripts/
│   │   ├── CharacterMovement.cs   # Movimento + rotação + gravidade
│   │   ├── Playerinput.cs         # Leitura de input
│   │   └── Animate.cs             # Motion para animator
│   ├── Characters/
│   │   ├── Player/
│   │   └── Pokemons/
│   │       ├── beedrill/
│   │       ├── butterfree/
│   │       ├── cyndaquil/
│   │       └── scyther-slash/
│   ├── Scenes/SampleScene.unity
│   ├── Sounds/
│   ├── Import/
│   ├── Location Assets For Tutorial/   # Nature pack + town low-poly
│   ├── HDRPDefaultResources/
│   └── Sketchfab For Unity/
├── Packages/
└── ProjectSettings/
```

## Pokémon incluídos

- **Beedrill**
- **Butterfree**
- **Cyndaquil**
- **Scyther** (scyther-slash)

## Como abrir no Unity

1. Instale o **Unity Hub** e a versão **2022.3.16f1** com suporte a **HDRP**.
2. Clone o repositório:
   ```bash
   git clone https://github.com/Magah051/pokemon_monster_collection_3d.git
   ```
3. Abra o projeto no Unity Hub e aguarde a importação HDRP.
4. Abra `Assets/Scenes/SampleScene.unity`.
5. Pressione **Play**.

## Controles

| Ação | Controle |
|------|----------|
| Mover | Eixos Horizontal / Vertical (WASD ou setas) |
| Olhar / câmera | Conforme setup da câmera na cena |

O movimento usa a direção da câmera (`forward` + `right`) e ignora o eixo Y na direção, aplicando gravidade via `Physics.gravity`.

## Status

Protótipo em evolução: movimento do player, câmera, colliders de chão e adição de pets/Pokémon NPCs.

## Aviso

Pokémon e marcas relacionadas pertencem a seus respectivos donos (Nintendo / Game Freak / Creatures). Este repositório é um **projeto de estudo/portfólio**, sem fins comerciais.
