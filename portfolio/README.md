# Portfolio Personnel

Un portfolio professionnel créé avec Vue 3, Bootstrap 5 et Font Awesome.

## Technologies utilisées

- Vue.js 3
- Bootstrap 5
- Font Awesome
- Vite

## Fonctionnalités

- Design responsive
- Navigation fluide avec défilement
- Sections : Accueil, À propos, Projets, Compétences, Contact
- Formulaire de contact
- Liens vers les réseaux sociaux
- Animations et transitions

## Installation

1. Cloner le repository :
```bash
git clone [URL_DU_REPO]
cd portfolio
```

2. Installer les dépendances :
```bash
npm install
```

3. Lancer le serveur de développement :
```bash
npm run dev
```

4. Pour construire pour la production :
```bash
npm run build
```

## Personnalisation

1. Modifier les informations personnelles dans les composants
2. Ajouter vos propres projets dans `src/components/Projects.vue`
3. Mettre à jour les compétences dans `src/components/Skills.vue`
4. Personnaliser les liens sociaux dans `src/components/Contact.vue`

## Structure du projet

```
portfolio/
├── src/
│   ├── components/
│   │   ├── Home.vue
│   │   ├── About.vue
│   │   ├── Projects.vue
│   │   ├── Skills.vue
│   │   └── Contact.vue
│   ├── App.vue
│   └── main.js
├── public/
└── index.html
```

## License

MIT
