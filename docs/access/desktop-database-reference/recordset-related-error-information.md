---
title: Información de errores relacionados con el conjunto de registros
TOCTitle: Recordset-related error information
ms:assetid: 388308c7-e121-bd12-228a-312c897b8c55
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249136(v=office.15)
ms:contentKeyID: 48544222
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5b0dc56ba591263cd834e26ca4e89a371f272d5a
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946471"
---
# <a name="recordset-related-error-information"></a>Información de errores relacionados con el conjunto de registros

**Se aplica a**: Access 2013, Office 2013

Durante un proceso por lotes, la propiedad **Status** del objeto **Recordset** proporciona información sobre cada registro del **conjunto de registros**. Antes de que se realice una actualización por lotes, la propiedad **Status** del **conjunto de registros** refleja información sobre los registros que se van a agregar, cambiar y eliminar. 

Después de haber llamado a **UpdateBatch**, la propiedad **Status** indica si la operación se ha realizado correctamente o no. A medida que se mueve por los registros del **conjunto de registros**, el valor de la propiedad **Status** cambia para describir el estado del registro activo.

