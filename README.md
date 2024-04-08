A *very* basic (I cannot stress enough how basic this is) *temporary* theme switcher for Neovim 0.9.5 and later (this may work on prior versions of nvim I just don't know when Lua functions like this started being supported, I think maybe 0.5.x something?). 

Easiest installation/config: 

Copy/paste this into your 'init.lua' after you 'require.setup()' your installed themes:

vim.keymap.set("n", "<leader>t", function() -- <leader>t is just my preferential binding for this, you can replace with whatever you'd like
    local selected_theme = vim.fn.input("colorscheme(rose-pine, tokyonight, gruvbox, terafox, carbonfox, nightfox): ")
    vim.cmd("colorscheme " .. selected_theme)
end)

*Note: this theme set will be overridden every time you exit Neovim. Recommended to set an "all the time" theme, and use this for temporary changes of mood.
