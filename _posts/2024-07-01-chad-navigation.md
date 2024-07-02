---
layout: post
title: Nvchadhad ᲜᲐᲕᲘᲒᲐᲪᲘᲐ 
---


### ᲨᲔᲡᲐᲕᲐᲚᲘ
ამ ფაილში გამოყენებულია `nvchad.mappings` მოდულის ფუნქციები და `vim.keymap.set` ფუნქცია Neovim-ში ცხელი კლავიშების კონფიგურაციისთვის. ქვემოთ აღწერილია ბრძანებები და კლავიშების კომბინაციები, რომლებიც მუშაობენ სხვადასხვა რეჟიმებში, როგორებიცაა ნორმალური (n) და ჩასმის (i) რეჟიმები.

### ᲫᲘᲠᲘᲗᲐᲓᲘ ᲑᲠᲫᲐᲜᲔᲑᲔᲑᲘ

```lua
map("n", ";", ":", { desc = "CMD enter command mode" })
```
- გადადის საკომანდო რეჟიმში (ანალოგ `:`).

```lua
map("n", "<leader>w", "<cmd>w<CR>", { desc = "Save" })
```
- ინახავს მიმდინარე ფაილს (ანალოგ `:w`).

### ᲧᲕᲔᲚᲐ ᲑᲣᲤᲔᲠᲘᲡ ᲓᲐᲮᲣᲠᲕᲐ

```lua
map("n", "<leader>cx", function()
  require("nvchad.tabufline").closeAllBufs()
end, { desc = "Close All Buffers" })
```
- ხურავს ყველა გახსნილ ბუფერს.

### ᲓᲐᲕᲐᲚᲔᲑᲔᲑᲘᲡ ᲛᲝᲫᲔᲑᲜᲐ

```lua
map("n", "<leader>ft", "<cmd>TodoTelescope<CR>", { desc = "Find Todo" })
```
- ხსნის დავალებების საძიებო ფანჯარას `Telescope` პლაგინის გამოყენებით.

### ᲤᲐᲜᲯᲠᲘᲡ ᲕᲔᲠᲢᲘᲙᲐᲚᲣᲠᲘ ᲒᲐᲧᲝᲤᲐ

```lua
map("n", "\\", "<cmd>:vsplit <CR>", { desc = "Vertical Split" })
```
- ვერტიკალურად ჰყოფს ფანჯარას.

### Tmux ᲤᲐᲜᲯᲠᲔᲑᲘᲡ ᲜᲐᲕᲘᲒᲐᲪᲘᲐ

```lua
map("n", "<c-l>", "<cmd>:TmuxNavigateRight<cr>", { desc = "Tmux Right" })
map("n", "<c-h>", "<cmd>:TmuxNavigateLeft<cr>", { desc = "Tmux Left" })
map("n", "<c-k>", "<cmd>:TmuxNavigateUp<cr>", { desc = "Tmux Up" })
map("n", "<c-j>", "<cmd>:TmuxNavigateDown<cr>", { desc = "Tmux Down" })
```
- Tmux ფანჯრების ნავიგაცია სხვადასხვა მიმართულებით.

### Trouble

```lua
map("n", "<leader>qx", "<cmd>TroubleToggle<CR>", { desc = "Open Trouble" })
map("n", "<leader>qw", "<cmd>TroubleToggle workspace_diagnostics<CR>", { desc = "Open Workspace Trouble" })
map("n", "<leader>qd", "<cmd>TroubleToggle document_diagnostics<CR>", { desc = "Open Document Trouble" })
map("n", "<leader>qq", "<cmd>TroubleToggle quickfix<CR>", { desc = "Open Quickfix" })
map("n", "<leader>ql", "<cmd>TroubleToggle loclist<CR>", { desc = "Open Location List" })
map("n", "<leader>qt", "<cmd>TodoTrouble<CR>", { desc = "Open Todo Trouble" })
```
- მართვა Trouble პლაგინით სხვადასხვა დიაგნოსტიკისა და დავალებების სიისთვის.

### ᲢᲔᲡᲢᲘᲠᲔᲑᲐ

```lua
map("n", "<leader>tt", function()
  require("neotest").run.run()
end, { desc = "Run nearest test" })
map("n", "<leader>tf", function()
  require("neotest").run.run(vim.fn.expand "%")
end, { desc = "Run file test" })
map("n", "<leader>to", ":Neotest output<CR>", { desc = "Show test output" })
map("n", "<leader>ts", ":Neotest summary<CR>", { desc = "Show test summary" })
```
- ტესტების გაშვება `neotest` პლაგინის გამოყენებით.

### ᲓᲔᲑᲐᲒᲘᲜᲒᲘ

```lua
map("n", "<leader>du", function()
  require("dapui").toggle()
end, { desc = "Toggle Debug UI" })
map("n", "<leader>db", function()
  require("dap").toggle_breakpoint()
end, { desc = "Toggle Breakpoint" })
map("n", "<leader>ds", function()
  require("dap").continue()
end, { desc = "Start" })
map("n", "<leader>dn", function()
  require("dap").step_over()
end, { desc = "Step Over" })
```
- დებაგინგის მართვა DAP (Debug Adapter Protocol) პლაგინის გამოყენებით.

### Git

```lua
map("n", "<leader>gl", ":Flog<CR>", { desc = "Git Log" })
map("n", "<leader>gf", ":DiffviewFileHistory<CR>", { desc = "Git File History" })
map("n", "<leader>gc", ":DiffviewOpen HEAD~1<CR>", { desc = "Git Last Commit" })
map("n", "<leader>gt", ":DiffviewToggleFile<CR>", { desc = "Git File History" })
```
- Git-ის მუშაობის ბრძანებები, როგორებიცაა ისტორიის და ლოგების ნახვა.

### ᲢᲔᲠᲛᲘᲜᲐᲚᲘ

```lua
map("n", "<C-]>", function()
  require("nvchad.term").toggle { pos = "vsp", size = 0.4 }
end, { desc = "Toogle Terminal Vertical" })
map("n", "<C-\\>", function()
  require("nvchad.term").toggle { pos = "sp", size = 0.4 }
end, { desc = "Toogle Terminal Hiorizontal" })
map("n", "<C-f>", function()
  require("nvchad.term").toggle { pos = "float" }
end, { desc = "Toogle Terminal Float" })
map("t", "<C-]>", function()
  require("nvchad.term").toggle { pos = "vsp" }
end, { desc = "Toogle Terminal Vertical" })
map("t", "<C-\\>", function()
  require("nvchad.term").toggle { pos = "sp" }
end, { desc = "Toogle Terminal Horizontal" })
map("t", "<C-f>", function()
  require("nvchad.term").toggle { pos = "float" }
end, { desc = "Toogle Terminal Float" })
```
- ტერმინალის გახსნა სხვადასხვა პოზიციებში (ვერტიკალურად, ჰორიზონტალურად, მცურავ ფანჯარაში).
ტერმინალის გახსნა ხდება მოცემული ერთერთი ბრძანებით, ხოლო მისი დახურვა მოხდება, თუ გამოვიყენებთ ნებისმიერს ამ ბრძანებებიდან.

### ᲫᲘᲠᲘᲗᲐᲓᲘ ᲑᲠᲫᲐᲜᲔᲑᲔᲑᲘ ᲩᲐᲡᲛᲘᲡ ᲠᲔᲟᲘᲛᲨᲘ

```lua
map("i", "jj", "<ESC>")
```
- ჩასმის რეჟიმიდან გამოსვლა ორჯერ `j` დაჭერის შემდეგ.

```lua
map("i", "<C-g>", function()
  return vim.fn["codeium#Accept"]()
end, { expr = true })
```
- ავტოდოპლეტის მიღება `Ctrl+G` კომბინაციის გამოყენებით.

ეს ბრძანებები ამარტივებს Neovim-თან მუშაობას, სწრაფად წვდომას ხშირად გამოყენებულ ფუნქციებთან და პლაგინებთან.
