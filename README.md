# Nginx com Docker Swarm

Este repositório contém os arquivos necessários para configurar o Nginx como proxy reverso ou servidor web em um ambiente Docker Swarm. Inclui suporte para redes overlay e volumes persistentes.

Recursos
Configuração simples para Nginx no Docker Swarm.
Rede overlay para comunicação entre serviços.
Suporte para volumes persistentes para armazenar configurações e logs.
Fácil escalabilidade e manutenção.

Configure os arquivos do Nginx
Personalize o arquivo nginx/nginx.conf conforme necessário.
Adicione arquivos HTML ou estáticos ao diretório nginx/html.

Implemente a stack
Use o comando abaixo para iniciar o Nginx no Swarm:

docker stack deploy -c nginx.yml nginx

Configuração do Docker Compose

Serviço
Nginx:
Usa a imagem oficial do Nginx.
Configuração customizada é montada a partir do diretório nginx/.
Porta 80 exposta no host para acesso público.

Rede
nginx_network: Rede overlay que permite a comunicação com outros serviços no Swarm.

Volumes
nginx_config: Armazena o arquivo de configuração do Nginx.

Personalização
Configuração do Nginx
Você pode personalizar o comportamento do Nginx editando o arquivo nginx/nginx.conf

Contribuindo
Contribuições são bem-vindas! Se você tiver sugestões, problemas ou melhorias, abra uma issue ou envie um pull request.
