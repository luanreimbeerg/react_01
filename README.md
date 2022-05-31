#Conceitos react/primeiro projeto

Começar o projeto
    - yarn init -y

Instalar react no projeto 
    - yarn add react
    - yarn add react-dom

node_modules => pasta de dependecias do projeto

Criar pastas 
    - src => todo codigo criado na aplicação
    - public => assets
    
Biblioteca babel
    - babel => converter codigo para browser
    - yarn add @babel/core @babel/cli @babel/preset-env -D
    - yarn add @babel/preset-react -D

Criar babel.config.js add:
    ---
        module.exports = {
            presents: [
                '@babel/present-env'
            ]
        }
    ---

Biblioteca Webpack: 
    - yarn add webpack webpack-cli -D
    - yarn add babel-loader -D

Criar webpack.config.js add: 
    ---
        const path = require('path')

        module.exports = {
            entry: path.resolve(__dirname, 'src', 'index.jsx'),
            output: {
                path: path.resolve(__dirname, 'dist'),
                filename: 'bundle.js'
            },
            resolve: {
                extensions: ['.js', '.jsx'],
            },
            module: {
                rules: [
                    {
                        test: /\.jsx$/,
                        exclude: /node_modules/,
                        use: 'babel-loader',
                    }
                ],
            }
        }
    ---

    - yarn add html-webpack-plugin -D
    - yarn add webpack-dev-server -D
#   r e a c t _ 0 1  
 