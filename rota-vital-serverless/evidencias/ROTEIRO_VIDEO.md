# Roteiro do vídeo (máx. 3 min, gravação de tela)

Apagar este arquivo antes de entregar (ou mantê-lo, tanto faz). Tenha dois terminais abertos, Docker rodando e a pasta do projeto aberta.

1. **0:00 a 0:20**: mostrar `sam --version`, `docker ps` e a pasta (`template.yaml`, `hello_world/app.py`). Falar em uma frase o que a função faz.
2. **0:20 a 1:00**: `sam build` e `sam local invoke -e events/pedido.json` duas vezes. Apontar a diferença de tempo (cold start vs. reaproveitamento).
3. **1:00 a 2:00**: `sam local start-api` no terminal 1; no terminal 2, três `curl` em `/guias`. Mostrar `invocacaoNesteAmbiente`. Se der tempo, subir com `--warm-containers LAZY` e repetir.
4. **2:00 a 3:00**: enviar `{"requisicaoId":"R-003","demorar":true}` e mostrar o erro de tempo limite (Timeout 3). Dizer que depois aumentou para 10 e a chamada funcionou.

## Prints para salvar nesta pasta

- `01-sam-version.png`
- `02-invoke-1.png` e `03-invoke-2.png` (com o tempo)
- `04-start-api-curls.png` (3 chamadas)
- `05-warm-containers.png`
- `06-timeout-erro.png`
- `07-timeout-10-ok.png`
