# 🛒 Minha Lista de Compras

**Aplicativo Android para importar preços de um CSV e montar uma lista de compras por código de barras.**

## O que o aplicativo faz

| Recurso | Para que serve |
| --- | --- |
| Importação de preços | Carregar dados de produtos e preços a partir de um arquivo CSV. |
| Lista por código de barras | Usar o código de barras como referência para montar a lista de compras. |

## Como usar

1. Prepare um arquivo CSV com os dados de preços no formato esperado pelo aplicativo.
2. Importe o arquivo no aplicativo Android.
3. Use os códigos de barras dos produtos para montar a lista.

## 📱 Onde encontrar o APK

Abra o [workflow **Gerar APK**](../../actions/workflows/apk.yml), selecione uma execução concluída com sucesso e baixe o artefato **Minha-lista-APK**, se estiver disponível. Dentro do arquivo baixado, você encontrará o `app-debug.apk`, uma versão de depuração para instalar e experimentar no Android.

## 🛠️ Como compilar

O código do aplicativo está em [Minha-lista-projeto.zip](Minha-lista-projeto.zip). Extraia o arquivo para obter a pasta `ListaCompras`. O workflow do repositório usa **Java 17**, **Android SDK** e **Gradle 8.11.1**.

Na pasta que contém `ListaCompras`, execute o mesmo comando usado pelo workflow:

```bash
gradle -p ListaCompras testDebugUnitTest assembleDebug
```

O APK de depuração é gerado em `ListaCompras/app/build/outputs/apk/debug/app-debug.apk`.
