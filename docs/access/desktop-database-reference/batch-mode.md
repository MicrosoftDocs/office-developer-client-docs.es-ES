---
title: Modo de proceso por lotes (referencia de base de datos de escritorio de Access)
TOCTitle: Batch mode
ms:assetid: b73921f6-5a12-9b26-ea65-99b32dd763f6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249883(v=office.15)
ms:contentKeyID: 48547294
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ac5f14d035a4e11cce67f01ca6636f3ebd39963e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296881"
---
# <a name="batch-mode"></a>Modo por lotes

**Se aplica a:** Access 2013, Office 2013

El modo de proceso por lotes está activo cuando la propiedad **LockType** se ha establecido en **adLockBatchOptimistic** y el proveedor admite la actualización por lotes. Algunas opciones de configuración del tipo de bloqueo no están disponibles según cuál sea la ubicación del cursor. Por ejemplo, un tipo de bloqueo pesimista no está disponible cuando **CursorLocation** está establecido en **adUseClient**. A la inversa, es posible que un proveedor no admita un bloqueo optimista por lotes cuando la ubicación del cursor esté en el servidor. La actualización por lotes se debe utilizar únicamente con un conjunto de claves o con un cursor estático.

El método **UpdateBatch** se utiliza para enviar cambios en un **conjunto de registros** guardados en el búfer de copia hasta el servidor, para actualizar el origen de datos. En la sección siguiente, abriremos un **conjunto de registros** en modo de proceso por lotes, realizaremos cambios en el búfer de copia y a continuación, enviaremos nuestros cambios al origen de datos mediante una llamada a **UpdateBatch**.

Esta sección incluye los siguientes temas:

- [Envío de actualizaciones: UpdateBatch](sending-the-updates-updatebatch.md)
- [Filtro de registros actualizados](filtering-for-updated-records.md)
- [Tratamiento de las actualizaciones con errores](dealing-with-failed-updates.md)
- [Detección y resolución de conflictos](detecting-and-resolving-conflicts.md)
- [Desconexión y reconexión del conjunto de registros](disconnecting-and-reconnecting-the-recordset.md)
- [Actualización de resultados JOINed: tabla única](updating-joined-results-unique-table.md)

