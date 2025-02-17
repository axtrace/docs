# Вопросы о {{ PG }}

#### Как импортировать данные в кластер базы данных {{ PG }} в {{ mpg-short-name }}? {#migrate}

Используйте встроенный инструмент `pg_dump` для миграции данных в {{ PG }}-кластер {{ mpg-short-name }}.

#### Какие версии {{ PG }} поддерживает {{ mpg-short-name }}? {#supported-version}

{{ mpg-short-name }} поддерживает {{ PG }} 10, 11, 12, 13 и 14, а также PostgreSQL 10, 11 и 12 для 1С.

#### Включено ли резервное копирование кластеров БД по умолчанию? {#backup}

Да, по умолчанию резервное копирование включено. Для {{ PG }}-кластеров выполняется полное резервное копирование один раз в сутки и сохраняются все журналы транзакций кластера БД. Это позволяет восстановить состояние кластера на любой момент времени в пределах периода хранения резервных копий, за исключением последних 30 секунд.

#### Шифруется ли соединение с кластером БД {{ PG }}? {#encryption}

Соединение между кластером БД и приложением всегда шифруется с использованием SSL. Отключить шифрование соединений с кластером нельзя.

#### Что такое реплика для чтения в {{ PG }}? {#read-only-instance}

Реплика для чтения — это доступный только для чтения хост в кластере БД {{ PG }}, данные на котором синхронизируются с хостом-мастером (применимо только если в кластере работает более 1 хоста). Вы можете использовать реплику для чтения для снижения нагрузки на мастер в базах данных с большим объемом запросов на чтение.

#### Какие расширения для {{ PG }} поддерживаются в {{ mpg-short-name }}? {#pg-extension}

Список поддерживаемых расширений для {{ PG }} приведен в разделе [{#T}](../operations/cluster-extensions.md).

#### Какие ограничения накладываются на кластеры БД {{ PG }}? {#instance-limitations}

Подробнее об ограничениях {{ mpg-short-name }} см. раздел [{#T}](../concepts/limits.md). В разделе [{#T}](../concepts/instance-types.md) приведены характеристики кластеров, которые можно создать с помощью {{ mpg-short-name }}.


#### Какие значения LC_COLLATE и LC_CTYPE по умолчанию выставляются для баз данных? {#which-lc-collate-and-lc-lctype-values-are-set-for-databases-by-default}

По умолчанию для создаваемых баз данных выставляются значения `LC_CTYPE=C` и `LC_COLLATE=C`. Для базы данных, которую вы создаете вместе с кластером, эти настройки изменить нельзя, но вы можете [создать новую базу](../operations/databases.md) и указать нужные значения для нее.
