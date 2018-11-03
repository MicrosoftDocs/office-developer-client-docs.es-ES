---
title: Modo de proceso por lotes (referencia de escritorio de la base de datos de Access)
TOCTitle: Batch mode
ms:assetid: b73921f6-5a12-9b26-ea65-99b32dd763f6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249883(v=office.15)
ms:contentKeyID: 48547294
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9541e8b7888f5fb5f16bcfb343d545cf304b1afd
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945792"
---
# <a name="batch-mode"></a>Modo de proceso por lotes

**Se aplica a**: Access 2013, Office 2013

El modo de proceso por lotes está activo cuando la propiedad **LockType** se ha establecido en **adLockBatchOptimistic** y el proveedor admite la actualización por lotes. Algunas opciones de configuración del tipo de bloqueo no están disponibles según cuál sea la ubicación del cursor. Por ejemplo, un tipo de bloqueo pesimista no está disponible cuando **CursorLocation** está establecido en **adUseClient**. A la inversa, es posible que un proveedor no admita un bloqueo optimista por lotes cuando la ubicación del cursor esté en el servidor. La actualización por lotes se debe utilizar únicamente con un conjunto de claves o con un cursor estático.

El método **UpdateBatch** se utiliza para enviar cambios en un **conjunto de registros** guardados en el búfer de copia hasta el servidor, para actualizar el origen de datos. En la sección siguiente, abriremos un **conjunto de registros** en modo de proceso por lotes, realizaremos cambios en el búfer de copia y a continuación, enviaremos nuestros cambios al origen de datos mediante una llamada a **UpdateBatch**.

Esta sección incluye los temas siguientes:

- [Enviar actualizaciones: UpdateBatch](sending-the-updates-updatebatch.md)
- [Filtrar registros actualizados](filtering-for-updated-records.md)
- [Tratar actualizaciones con errores](dealing-with-failed-updates.md)
- [Detectar y resolver conflictos](detecting-and-resolving-conflicts.md)
- [Desconectar y volver a conectar el objeto Recordset](disconnecting-and-reconnecting-the-recordset.md)
- [Actualizar los resultados de JOIN: tabla única](updating-joined-results-unique-table.md)

