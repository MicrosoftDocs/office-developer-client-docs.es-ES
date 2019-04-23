---
title: Actualización de datos (referencia de base de datos de escritorio de Access)
TOCTitle: Updating Data
ms:assetid: 02e82066-77c8-cbb2-db28-98e2fc94404c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248794(v=office.15)
ms:contentKeyID: 48542970
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8e6989468e23fc1c9c611eb091172822a6ffe938
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313570"
---
# <a name="updating-data"></a>Actualización de datos


**Se aplica a:** Access 2013, Office 2013

El comportamiento y la funcionalidad de las operaciones de actualización dependen en gran medida del modo de actualización (tipo de bloqueo), del tipo de cursor y de su ubicación.

Use el método **Update** para guardar los cambios efectuados en el registro actual de un objeto **Recordset** desde la llamada al método **AddNew** o desde el cambio de alguno de los valores de campo de un registro existente. El objeto **Recordset** debe ser compatible con actualizaciones.

Si el objeto **Recordset** admite la actualización por lotes, se pueden almacenar en la memoria caché local varios cambios realizados en uno o varios registros hasta que se llame al método **UpdateBatch**. Si modifica el registro actual o agrega un nuevo registro mientras llama al método **UpdateBatch**, ADO llamará automáticamente al método **Update** para guardar todos los cambios pendientes en el registro actual antes de transmitir los cambios por lotes al proveedor.

El registro actual sigue siendo el actual después de la llamada a los métodos **Update** o **UpdateBatch**.

Esta sección incluye los siguientes temas:

- [Modo Inmediato](immediate-mode.md)
- [Procesamiento de transacciones](transaction-processing.md)
- [Batch Mode (ADO)](batch-mode.md)

