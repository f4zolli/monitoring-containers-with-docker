# monitoring-containers-with-docker

Script criado em Python para realizar o monitoramento de Containers que passam a ter o estado "die" dentro do docker, reportando através do webhook de um canal no Discord.


Créditos de todo aprendizado vindo das aulas da Comunidade DevOps (@mateuslinux_). Obrigado Xara.

============================================================================================================

Sistema Operacional: Linux Mint 21
OBSERVACOES: Vale ressaltar que o script foi criado em um ambiente de estudos e algumas anotacoes devem ser ressaltadas antes de iniciar a utilizacao.
O docker por padrao utiliza um socket de comunicação do tipo UNIX (/run/docker.sock), porém utilizaremos por HTTP (tcp://0.0.0.0:2375) podendo receber comunicacoes no localhost ou da propria rede, para isso devemos alterar o arquivo de serviço do Docker (usr/lib/systemd/system/docker.service).

Ferramentas: python3, docker

REFERENCIAS:
Doc API Docker: https://docs.docker.com/engine/api/v1.41/#tag/System/operation/SystemEvents
Docker SDK for Python: https://docker-py.readthedocs.io/en/stable/

# MODO DE USO (para teste):
1. Crie um diretorio
2. Realize a instalação:
```
git clone https://github.com/f4zolli/monitoring-containers-with-docker.git
``` 
3. DICA: Sempre que for trabalhar em um projeto python, utilize o .venv , assim voce cria um ambiente isolado e evita de quebrar algum ambiente que rode internamente no seu computador
```
python3 -m venv .venv
```
4. Ative o venv e trabalhe dentro dele com o comando:
```
source .venv/bin/activate
```
5. Edite o código e adicione o link do seu webhook do discord na linha 6.
