---
title: 'Capítulo 5: Actualizar y almacenar datos'
TOCTitle: 'Chapter 5: Updating and Persisting Data'
ms:assetid: 77acb763-1c60-1945-791d-3e83d684fb0d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249493(v=office.15)
ms:contentKeyID: 48545732
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 91c747c970988a9ca853f0be66f5c0b485f5c3f6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483624"
---
# <a name="chapter-5-updating-and-persisting-data"></a>Capítulo 5: Actualizar y almacenar datos


**Se aplica a**: Access 2013 | Office 2013

En capítulos anteriores, se explicó cómo usar ADO para obtener datos de un origen de datos, cómo desplazarse por ellos y cómo modificarlos. Por supuesto, si un objetivo de la aplicación es permitir que los usuarios realicen cambios en los datos, deberá saber cómo guardar esos cambios. Puede hacer que los cambios realizados en un **Recordset** se conserven en un archivo mediante el método **Save**, o bien, puede enviar los cambios de vuelta al origen de datos para su almacenamiento mediante los métodos **Update** o **UpdateBatch**.

En los capítulos anteriores, se cambiaron datos en varias filas de un **Recordset**. ADO admite dos nociones básicas relacionadas con la adición, la eliminación y la modificación de filas de datos.

La primera noción es que los cambios no se implementan inmediatamente en el **Recordset**; en vez de ello, se realizan en un *búfer de copia* interno. Si no desea conservarlos, se descartan en el búfer de copia. Por el contrario, si decide conservarlos, se aplicarán desde el búfer de copia al **Recordset**.

La segunda noción es que los cambios se que cualquiera propagan al origen de datos en cuanto se declara el trabajo completado en una fila (modo *inmediato* ), o todos los cambios a un conjunto de filas se recopilan hasta que se declara el trabajo para el conjunto completo de (que es el modo de *proceso por lotes* ). La propiedad **LockType** determina cuándo se realizan los cambios en el origen de datos subyacente. **adLockOptimistic** o **adLockPessimistic** especifican el modo inmediato, mientras que **adLockBatchOptimistic** especifica el modo de proceso por lotes. La propiedad **CursorLocation** puede determinar qué configuraciones de **LockType** están disponibles. Por ejemplo, el valor **adLockPessimistic** no se admite si la propiedad **CursorLocation** se establece en **adUseClient**.

En el modo inmediato, cada llamada al método **Update** propaga los cambios al origen de datos. En el modo de proceso por lotes, cada llamada a **Update** o movimiento de la posición actual de fila guarda los cambios en el búfer de copia, pero sólo el método **UpdateBatch** propaga los cambios al origen de datos.

