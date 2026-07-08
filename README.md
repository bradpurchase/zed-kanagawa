# Kanagawa.nvim for Zed

![image](https://github.com/ethangilmore/zed-kanagawa/assets/90002503/705282e8-82d7-497b-8b69-4a1db8ec1058)

![Kanagawa Theme](https://img.shields.io/badge/Theme-Kanagawa-blueviolet)

Faithful Zed port of [rebelot's Kanagawa.nvim](https://github.com/rebelot/kanagawa.nvim), a colorscheme inspired by Katsushika Hokusai's famous painting.

## Description

This fork focuses on making the Zed theme match Kanagawa.nvim's Wave syntax colors as closely as Zed's theme system allows. It keeps the upstream variants available, while tuning `Kanagawa Wave` and `Kanagawa` for closer Neovim parity.

Some differences can remain because Zed and Neovim do not always assign the same Tree-sitter captures or semantic-token scopes.

## Optional Semantic Token Settings

Kanagawa.nvim can use LSP semantic highlighting to color readonly/const-like variables as constants. Zed does not enable that behavior from themes, so users who want closer TypeScript/TSX parity can add this to `settings.json`:

```json
{
  "semantic_tokens": "combined",
  "global_lsp_settings": {
    "semantic_token_rules": [
      {
        "token_modifiers": ["readonly"],
        "style": ["constant"]
      }
    ]
  }
}
```

## Preview

- **Kanagawa**: A dark Wave-based theme with soft and relaxing colors.
  ![Kanagawa Theme](./previews/Kanagawa.png)
- **Kanagawa Dragon**: A dark variant with deeper, contrasting tones.
  ![Kanagawa Dragon Theme](./previews/Kanagawa_dragon.png)
- **Kanagawa Wave**: The primary faithful Wave port.
  <img width="1512" alt="Screenshot 2024-04-13 at 4 20 56 PM" src="https://github.com/ethangilmore/zed-kanagawa/assets/90002503/16c69365-332b-4244-ac13-3b52737f8d19">
- **Kanagawa Lotus**: A light theme inspired by the serenity of lotuses.
  ![Kanagawa Lotus Theme](./previews/Kanagawa_lotus.png)

## Contribution

Issues and pull requests are welcome, especially for concrete mismatches with Kanagawa.nvim.

## Credit

All credit goes to [rebelot](https://github.com/rebelot) for creating Kanagawa.nvim. You can thank him [here](https://github.com/rebelot/kanagawa.nvim#donate).

This fork is based on [ethangilmore/zed-kanagawa](https://github.com/ethangilmore/zed-kanagawa).
