EXTENSIONS:
    FROM: code --list-extensions > extensions.list
    APPLY (Windows): cat extensions.list |% { code --install-extension $_}
    APPLY (Linux):cat extensions.txt | xargs code --list-extensions {} vscode-extensions

PROFILES:
    Profiles: Export Profile


CONFIG:
    Windows location:
        C:\Users\%USERNAME%\AppData\Roaming\Code\User
    Linux location:
        .config/Code/User
