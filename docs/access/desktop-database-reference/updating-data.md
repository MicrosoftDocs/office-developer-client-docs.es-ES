---
title: Actualización de datos (referencia de escritorio de la base de datos de Access)
TOCTitle: Updating Data
ms:assetid: 02e82066-77c8-cbb2-db28-98e2fc94404c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248794(v=office.15)
ms:contentKeyID: 48542970
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8e6989468e23fc1c9c611eb091172822a6ffe938
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726340"
---
# <a name="updating-data"></a>Actualización de datos


**Se aplica a**: Access 2013, Office 2013

El comportamiento y la funcionalidad de las operaciones de actualización dependen en gran medida del modo de actualización (tipo de bloqueo), del tipo de cursor y de su ubicación.

Use el método **Update** para guardar los cambios efectuados en el registro actual de un objeto **Recordset** desde la llamada al método **AddNew** o desde el cambio de alguno de los valores de campo de un registro existente. El objeto **Recordset** debe ser compatible con actualizaciones.

Si el objeto **Recordset** admite la actualización por lotes, se pueden almacenar en la memoria caché local varios cambios realizados en uno o varios registros hasta que se llame al método **UpdateBatch**. Si modifica el registro actual o agrega un nuevo registro mientras llama al método **UpdateBatch**, ADO llamará automáticamente al método **Update** para guardar todos los cambios pendientes en el registro actual antes de transmitir los cambios por lotes al proveedor.

El registro actual sigue siendo el actual después de la llamada a los métodos **Update** o **UpdateBatch**.

Esta sección incluye los temas siguientes:

- [Modo Inmediato](immediate-mode.md)
- [Procesamiento de transacciones](transaction-processing.md)
- [Modo de proceso por lotes (ADO)](batch-mode.md)

