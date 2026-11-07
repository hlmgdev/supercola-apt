# Repositório apt do Super Cola

Este repositório guarda as atualizações do [Super Cola](https://github.com/hlmgdev/supercola), publicadas em `https://hlmgdev.github.io/supercola-apt`.

Você não precisa configurar nada. O pacote `supercola`, a partir da 1.2.0, já traz o endereço e a chave, e as versões novas chegam junto com as atualizações do sistema. Para instalar pela primeira vez, siga o [README do Super Cola](https://github.com/hlmgdev/supercola#instalação).

## Assinatura

Os índices são assinados com esta chave Ed25519, que vence em 6 de novembro de 2031:

```text
8EC40968C091F69686334ECFF36E6858EC0E92C2
```

A chave pública está em [`supercola-archive-keyring.asc`](supercola-archive-keyring.asc). A chave privada nunca passa pelo GitHub: as versões são assinadas no computador do mantenedor.

O apt confere a assinatura em toda atualização e recusa um índice adulterado ou assinado por outra chave. O pacote também instala uma regra que impede o apt de instalar daqui qualquer pacote que não seja o `supercola`.

## Conteúdo

| Caminho | O que é |
|---|---|
| `dists/stable/` | Índices assinados (`InRelease`, `Release` e `Release.gpg`) |
| `pool/main/s/supercola/` | As três versões mais recentes do pacote |
| `publicadas.txt` | Cada versão já publicada e o SHA-256 do pacote. Uma versão nunca é republicada com outro conteúdo |
| `supercola-archive-keyring.asc` | Chave pública |

Os arquivos são gerados pelo `packaging/publish-apt.sh` do repositório principal. Não edite à mão.
