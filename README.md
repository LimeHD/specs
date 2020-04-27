# Внутренние спецификации Lime HD

## HTTP API

### Принципы и стандарты

При разработке клиента придерживаемся следующих стандартов и принципов

* HTTP 1.1
  * [RFC7230](https://tools.ietf.org/html/rfc7230)
  * [RFC7231](https://tools.ietf.org/html/rfc7231)
  * [RFC7232](https://tools.ietf.org/html/rfc7232)
  * [RFC7233](https://tools.ietf.org/html/rfc7233)
  * [RFC7234](https://tools.ietf.org/html/rfc7234)
  * [RFC7235](https://tools.ietf.org/html/rfc7235)
* [REST](https://en.wikipedia.org/wiki/Representational_state_transfer)
* [JSON:API v1.0](https://jsonapi.org)
* [Semantic Versioning 2.0.0](https://semver.org)

Принципы:

* Явная передача параметров в запросе.
* В запросе указывается ожидаемый тип контента `Accept` и `Accept-Language`

## Отправляемые заголовки

Все запросы на внутренее API совершаются со следующими  HTTP-заголоками:

Обязательные:

* `X-Device-Name` – наименование устройства (до 40 символов), например "HONOR+AUM-L29".
* `X-Device-Id` – идентификатор устройства (до 40 символов), например "2a2849ec114c2ede".
* `X-App-Id` – идентификатор приложения из маркета, например "limehd.ru.lite".
* `X-Platform` – наименование платформы. 'ios' или 'android'.
* `X-App-Version-Code` (ex version_code)
* `X-App-Version` (ex version_name)

Желательные:

* `X-Android-Sdk` – номер версии Android SDK которой собрано приложение, например "28". Не обязательный.

## Принимаемые заголовки

* `X-Server-Addr` – адрес сервера, отработавшего запрос.
* `X-Server-Name` – доменное имя сервера, отработавшего запрос.
* `X-Request-Id` – уникальный идентификатор запроса.
* `X-Request-Time` – время обработки запроса.
