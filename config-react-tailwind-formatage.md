## Pour l'organisation des classes Tailwind CSS dans React :

1ère étape : Dans le terminal de VS Code, saisissez ceci :
npm install --save-dev prettier prettier-plugin-tailwindcss
ou
npm install -D prettier prettier-plugin-tailwindcss
(la partie `-D` est un raccourci de `--save-dev`)

---

2ème étape : Créez un fichier de configuration Prettier nommé `.prettierrc` et ajoutez-y ceci :
{
"plugins": ["prettier-plugin-tailwindcss"]
}

---

3ème étape : Dans le fichier de configuration VS Code nommé `settings.json`, qui se trouve dans le dossier `.vscode`, ajoutez ceci :
{
"files.associations": {
"_.css": "tailwindcss",
"_.scss": "tailwindcss"
},
"editor.quickSuggestions": {
"strings": "on"
},
"editor.formatOnSave": true,
"editor.defaultFormatter": "esbenp.prettier-vscode",
"[javascript]": {
"editor.defaultFormatter": "esbenp.prettier-vscode"
},
"[javascriptreact]": {
"editor.defaultFormatter": "esbenp.prettier-vscode"
},
"[typescript]": {
"editor.defaultFormatter": "esbenp.prettier-vscode"
},
"[typescriptreact]": {
"editor.defaultFormatter": "esbenp.prettier-vscode"
}
}

---

4ème et dernière étape : Redémarrez VS Code.
