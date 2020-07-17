# kabug-rb
Repositorio do projeto Kabug com Cucumber, Capybara e Ruby

## Como executar o projeto

* importante ter o Ruby instalado (versão 2.5 ou superior)

### instalar o Bundler
`
gem install bundler
`

### Instalar as dependências do Ruby (projeto)
`
bundle install
`

### Executar localmente (minha maquina)
`
bundle exec cucumber
`

### Executar no servidor de CI (gerando reposts JSON)
`
bundle exec cucumber -p ci
`
