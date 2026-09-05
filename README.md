# remnanode-smux · pinned build v3.2.5

Копия ноды [legiz-ru/remnanode-smux](https://github.com/legiz-ru/remnanode-smux) версии **v3.2.5** со зафиксированной версией ядра **Xray v26.9.5-0936** ([Jolymmiles/Xray-core](https://github.com/Jolymmiles/Xray-core)).

Предназначено для панели версии **2.8.1**, где образы ноды 3.3.x не применяются.

## Образ

```
ghcr.io/yandexru45/remnanode-smux:v3.2.5-panel281
ghcr.io/yandexru45/remnanode-smux:v3.2.5-xray26.9.5-0936
```

Платформы: `linux/amd64`, `linux/arm64`.

Оба тега указывают на одну сборку: первый — «стабильное» имя для compose, второй — версия с зашитой версией ядра.

## Как собирается

GitHub Actions берёт официальный исходник апстрима на теге `v3.2.5` и меняет только build-args:

```
XRAY_CORE_VERSION=v26.9.5-0936
UPSTREAM_REPO=Jolymmiles
```

Код ноды при этом не модифицируется вообще.

## Пересборка

Actions → build-image → Run workflow: можно указать другой тег ноды или другую версию ядра.
