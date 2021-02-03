# Ambiente-Windows
## Minhas configurações no ambiente Windows


### 1. Instalar o gerenciador de pacotes Chocolatey
  Com Windows Power Shell como ADM execute:
 * comando: 
  `Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072;     iex ((New-   Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))`
__________________________________________________________________________________________________________________________
### 2. Instalar o editor de texto VSCODE
  * comando: `choco install vscode`
  
  ## Plugins:
  
  * ColorHighlight – Esse plugin mostra a cor exata de todos RGB’s ou HEX em seu código, muito útil para quem trabalha com CSS ou SASS;
  
  * DotEnv – Plugin que utilizo para ter suporte à sintaxe .env, muito útil para quem trabalha com NodeJS, ReactJS ou qualquer outro tipo de projeto web;
  
  * Dracula Official – Tema que utilizo no meu VSCode e em todos outros editores/terminais, pra mim foi o tema que mais me agradou durante mais tempo e olha que já usei muitos;
  
  * EditorConfig – Plugin utilizado para padronizar quebra de linha, indentação, espaços e tabs entre desenvolvedores de um mesmo projeto;
  
  * ESLint – Plugin utilizado para padronizar código entre desenvolvedores como utilização de pontos e vírgulas, tamanho máximo de caracteres em linhas e todo outro tipo de padronização. Recomendo muito a utilização desse plugin junto aos guias de estilo do AirBnB;
  
  * Markdown All in One – Plugin que utilizo para escrever e ler Markdown dentro do VSCode, muito útil para documentações o README’s do Github;
  
  * Material Icon Theme – Utilizo para exibir os ícones de acordo com a linguagem utilizada na minha sidebar. Fica muito legal mesmo pois esse plugin identifica a grande parte de libs e ferramentas.
  
  * ##### Configurações do settings.json:
  
           {
          "workbench.colorTheme": "Dracula",

          "workbench.iconTheme": "material-icon-theme",

          "terminal.integrated.shell.osx": "/bin/zsh",

          "workbench.startupEditor": "newUntitledFile",

          // Configura tamanho e família da fonte

          "editor.tabSize": 2,

          "editor.fontSize": 18,

          "editor.lineHeight":24,

          "editor.fontFamily":"Fira Code",

          "editor.fontLigatures":false,

          "explorer.compactFolders": true,

          "workbench.editor.labelFormat": "short",

          "extensions.ignoreRecommendations": true,

          // Aplica linhas verticais para lembrar de quebrar linha em códigos muito grandes

          "editor.rulers": [

          80,

          120

          ],

          "breadcrumbs.enabled": true,

          // Aplica um sinal visual na esquerda da linha selecionada

          "editor.renderLineHighlight":"gutter",

          // Aumenta a fonte do terminal

          "terminal.integrated.fontSize":14,

          // Define o tema dos ícones na sidebar

          }
      
    * Em breve link de repositorio das configurações do VSCODE
___________________________________________________________________________________________________________________________


### 3. - Instalar o NODE
  * comando: `choco install nodejs-lts`
  

### 4. Instalar o GIT
  * bash: `choco install git`` 
  
  #### Configurações no arquivo .gitconfig:  
  
        [color]
        ui = true

      [color"status"]
        added = green
        changed = yellow
        untranked = red

      [color"branch"]
        current = white
        remote = red

      [color"diff"]
        meta = yellow
        old = red
        new = green

      [alias]
        ci = commit
        co = checkout
        cm = checkout master
        cb = checkout -b
        st = status -sb
        sf = show --name-only
        lg = log --pretty=format:'%Cred%h%Creset %C(bold)%cr%Creset %Cgreen<%an>%Creset %s' --max-count=30
        incoming = !(git fetch --quiet && git log --pretty=format:'%C(yellow)%h %C(white)- %C(red)%an %C(white)- %C(cyan)%d%Creset %s %C(white)- %ar%Creset' ..@{u})
        outgoing = !(git fetch --quiet && git log --pretty=format:'%C(yellow)%h %C(white)- %C(red)%an %C(white)- %C(cyan)%d%Creset %s %C(white)- %ar%Creset' @{u}..)
        unstage = reset HEAD --
        undo = checkout --
        rollback = reset --soft HEAD~1  
        
   #### Em breve criarei repositório das configurações do meu git 
  ______________________________________________________________________________________________________________________

### 4. Instalar o terminal Windows Terminal
  * comando: `choco install microsoft-windows-terminal`
  
  #### 4.1. Colar as configurações no terminal para o arquivo config abrindo o terminal e pressionando ctrl + , :
  
    
   `// This file was initially generated by Windows Terminal 1.5.10271.0
    // It should still be usable in newer versions, but newer versions might have additional
    // settings, help text, or changes that you will not see unless you clear this file
    // and let us generate a new one for you.

    // To view the default settings, hold "alt" while clicking on the "Settings" button.
    // For documentation on these settings, see: https://aka.ms/terminal-documentation
    {
        "$schema": "https://aka.ms/terminal-profiles-schema",

        "defaultProfile": "{61c54bbd-c2c6-5271-96e7-009a87ff44bf}",

        // You can add more global application settings here.
        // To learn more about global settings, visit https://aka.ms/terminal-global-settings

        // If enabled, selections are automatically copied to your clipboard.
        "copyOnSelect": false,

        // If enabled, formatted data is also copied to your clipboard
        "copyFormatting": false,

        // A profile specifies a command to execute paired with information about how it should look and feel.
        // Each one of them will appear in the 'New Tab' dropdown,
        //   and can be invoked from the commandline with `wt.exe -p xxx`

        "theme": "dark",

        // To learn more about profiles, visit https://aka.ms/terminal-profile-settings
        "profiles":
        {
            "defaults":
            {
                "fontFace": "Fira Code",
                "fontSize": 14,
                "padding": "8, 8, 8, 8",
                "cursorShape": "filledBox",
                "colorScheme": "Dracula",
                "cursorColor": "#000",
                "useAcrylic": true,
                "acrylicOpacity": 0.7,
                "backgroundImage": "C:\\Users\\Isaac\\Downloads\\Awesome Wallpapers - wallhaven_cc.jpg",
                "backgroundImageStretchMode": "uniformToFill",
                "backgroundImageOpacity": 0.15



                // Put settings here that you want to apply to all profiles.
            },
            "list":
            [
                {
                    // Make changes here to the powershell.exe profile.
                    "guid": "{61c54bbd-c2c6-5271-96e7-009a87ff44bf}",
                    "name": "Windows PowerShell",
                    "commandline": "powershell.exe",
                    "hidden": false
                },
                {
                    // Make changes here to the cmd.exe profile.
                    "guid": "{0caa0dad-35be-5f56-a8ff-afceeeaa6101}",
                    "name": "Prompt de comando",
                    "commandline": "cmd.exe",
                    "hidden": false
                },
                {
                    "guid": "{b453ae62-4e3d-5e58-b989-0a998ec441b8}",
                    "hidden": true,
                    "name": "Azure Cloud Shell",
                    "source": "Windows.Terminal.Azure"
                }
            ]
        },

        // Add custom color schemes to this array.
        // To learn more about color schemes, visit https://aka.ms/terminal-color-schemes
        "schemes": [
            {
                "name": "Dracula",
                "cursorColor": "#F8F8F2",
                "selectionBackground": "#44475A",
                "background": "#282A36",
                "foreground": "#F8F8F2",
                "black": "#21222C",
                "blue": "#BD93F9",
                "cyan": "#8BE9FD",
                "green": "#50FA7B",
                "purple": "#FF79C6",
                "red": "#FF5555",
                "white": "#F8F8F2",
                "yellow": "#F1FA8C",
                "brightBlack": "#6272A4",
                "brightBlue": "#D6ACFF",
                "brightCyan": "#A4FFFF",
                "brightGreen": "#69FF94",
                "brightPurple": "#FF92DF",
                "brightRed": "#FF6E6E",
                "brightWhite": "#FFFFFF",
                "brightYellow": "#FFFFA5"
            }
        ],

        // Add custom actions and keybindings to this array.
        // To unbind a key combination from your defaults.json, set the command to "unbound".
        // To learn more about actions and keybindings, visit https://aka.ms/terminal-keybindings
        "actions":
        [
            // Copy and paste are bound to Ctrl+Shift+C and Ctrl+Shift+V in your defaults.json.
            // These two lines additionally bind them to Ctrl+C and Ctrl+V.
            // To learn more about selection, visit https://aka.ms/terminal-selection
            { "command": {"action": "copy", "singleLine": false }, "keys": "ctrl+c" },
            { "command": "paste", "keys": "ctrl+v" },

            // Press Ctrl+Shift+F to open the search box
            { "command": "find", "keys": "ctrl+shift+f" },

            // Press Alt+Shift+D to open a new pane.
            // - "split": "auto" makes this pane open in the direction that provides the most surface area.
            // - "splitMode": "duplicate" makes the new pane use the focused pane's profile.
            // To learn more about panes, visit https://aka.ms/terminal-panes
            { "command": { "action": "splitPane", "split": "auto", "splitMode": "duplicate" }, "keys": "alt+shift+d" }
        ],

        "keybindings": [{"command":"newTab", "keys":["ctrl+t"]}]    
    }  
   
 __________________________________________________________________________________________________________
  
### 5. Instalar a consulta de documentações DevDocs
  * comando: `choco install devdocs-app`
  
### 6. Instalar o Notion
  * comando: `choco install notion`
  
### 7. Instalar GitHub Desktop
  * comando: `choco install github-desktop`
  
### 8. Instalar o Ubuntu WSL
  * comando: `choco install wsl-ubuntu-2004`
  
### 9. Extensões do chrome:
  * JSON viewer;
  * React developer tools;
  * Octotree;
   
### 10. Ferramentas:
   * Whimsical #UX;
   * Insominia #API;
