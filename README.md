<div align="center">

# Snacks picker for sonictemplate

</div>

## Features

Integration for vim-sonictemplate with snacks.nvim.

## Requirements

- [folke/snacks.nvim](https://github.com/folke/snacks.nvim)
- [mattn/vim-sonictemplate](https://github.com/mattn/vim-sonictemplate)
- [nvim-lua/plenary.nvim](https://github.com/nvim-lua/plenary.nvim)

## Installation

Install the plugin using your favorite plugin manager.

### lazy.nvim

```lua
{
    "folke/snacks.nvim",
    dependencies = {
        "IMOKURI/snacks-picker-sonictemplate.nvim",
        "mattn/vim-sonictemplate",
        "nvim-lua/plenary.nvim",
    },
    priority = 1000,
    lazy = false,
    keys = {
        { "<Leader>s", function() require("snacks_picker").sonictemplate() end, desc = "Sonictemplate" },
    },
    init = function()
        vim.g.sonictemplate_vim_template_dir = { string.format("%s/template", vim.fn.stdpath("config")) }
    end,
    ---@type snacks.Config
    opts = {
        picker = { enabled = true },
    },
}
```

## Special Thanks

- [tamago324/telescope-sonictemplate.nvim](https://github.com/tamago324/telescope-sonictemplate.nvim)
