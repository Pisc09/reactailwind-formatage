## Instructions pour configurer un projet React avec Vite et TailwindCSS

### Étapes 1 à 9 : Exécution dans le terminal PowerShell de VSCode ou d'un autre IDE

### Étape 1 : Créer un nouveau projet Vite

1. Saisissez la commande suivante pour créer un projet avec Vite :
   ```powershell
   npm create vite@latest
   ```

### Étape 2 : Confirmation de l'installation

2. Lorsque vous êtes invité, saisissez "y" puis appuyez sur Enter pour confirmer.

### Étape 3 : Choisir le nom du projet

3. Entrez un nom pour le dossier du projet, puis appuyez sur Enter.

### Étape 4 : Sélectionner le framework

4. Choisissez "React" comme framework.

### Étape 5 : Sélectionner le langage

5. Sélectionnez "JavaScript + SWC". SWC est un compilateur rapide et performant qui optimise le code JavaScript, améliorant ainsi les performances globales du projet.

### Étape 6 : Vérifier les fichiers créés

6. Saisissez la commande suivante pour lister les fichiers dans votre dossier de projet :
   ```powershell
   ls
   ```

### Étape 7 : Ouvrir le projet dans VSCode

7. Saisissez la commande suivante pour ouvrir le projet dans VSCode :
   ```powershell
   code nom_du_dossier
   ```
   Remplacez "nom_du_dossier" par le nom que vous avez choisi à l'étape 3.

### Étape 8 : Installer TailwindCSS et ses dépendances

8. Installez TailwindCSS et les autres outils nécessaires avec la commande suivante :
   ```powershell
   npm install -D tailwindcss postcss autoprefixer
   ```

### Étape 9 : Initialiser la configuration TailwindCSS

9. Initialisez le fichier de configuration TailwindCSS en exécutant la commande suivante :
   ```powershell
   npx tailwindcss init -p
   ```

### Étape 10 : Configurer le fichier tailwind.config.js

10. Ouvrez le fichier `tailwind.config.js` et modifiez la propriété `content` pour inclure les chemins suivants :
    ```javascript
    content: ["./index.html", "./src/**/*.{html,js,jsx}"],
    ```

### Étape 11 : Supprimer le fichier App.css

11. Supprimez le fichier `App.css` dans le dossier `src`.

### Étape 12 : Nettoyer le fichier index.css

12. Ouvrez le fichier `index.css` dans le dossier `src` et supprimez tout son contenu.

### Étape 13 : Configurer Tailwind dans index.css

13. Ajoutez les directives TailwindCSS suivantes dans le fichier `index.css` :
    ```css
    @tailwind base;
    @tailwind components;
    @tailwind utilities;
    ```

### Étape 14 : Configurer le formatage dans VSCode

14. Créez un dossier nommé `.vscode` à la racine du projet, puis créez un fichier `settings.json` à l'intérieur de ce dossier.

### Étape 15 : Ajouter les paramètres de formatage

15. Ouvrez le fichier `settings.json` et collez-y le code suivant :

    ```json
    {
      "files.associations": {
        "*.css": "tailwindcss",
        "*.scss": "tailwindcss"
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
    ```

---

Vous avez maintenant terminé la configuration de votre projet React avec TailwindCSS et les paramètres de formatage optimisés dans VSCode. Vous pouvez commencer à développer votre application !