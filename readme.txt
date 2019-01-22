установка реакт приложения 

mkdir app-react-folder
cd app-react-folder
yarn add react react-dom
yarn add --dev parcel-bundler babel-preset-env babel-preset-react

добавить плагины спреад оператор  
yarn add --dev babel-plugin-transform-object-rest-spread

и плагин трансформации свойств класса
yarn add --dev  babel-plugin-transform-class-properties

создать файл .babelrc

записать в него пресеты и плагины для babel

{
  "presets": ["env", "react"],
  "plugins": ["transform-object-rest-spread",
			"transform-class-properties"]
}

В package.json  прописать скрипты для старта и сборки:


 "react-dom": "16.2.0"
  },
  "devDependencies": {
    "babel-preset-env": "1.6.1",
    "babel-preset-react": "6.24.1",
    "parcel-bundler": "1.5.0"
  },
 "scripts": {
   "start": "parcel public/index.html",
   "build": "parcel build src/index.js"
 }
}

запуск сервера:

yarn start

сборка :
yarn build

при копировании файлов в проект необходимо очищать папку кэша 

для продакшена включить файлы index.css и index.js в html файл





