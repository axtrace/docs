---
sourcePath: ru/ydb/ydb-docs-core/ru/core/maintenance/_includes/backup_and_recovery/06_s3_5_restore.md
---
### Восстановление из S3-совместимых хранилищ {#s3_restore}

Предварительно нужно подключить бакет, содержащий файлы с резервной копией базы YDB в s3-совместимом хранилище, чтобы она была доступна через операции с файловой системой.

После успешного подключения следует загрузить данные из копии в YDB по инструкции, описанной в разделе [Восстановление из резервной копии на файловой системе](#filesystem_restore).