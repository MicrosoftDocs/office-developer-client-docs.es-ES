---
title: Recordset2.BatchCollisions (DAO)
TOCTitle: BatchCollisions Property
ms:assetid: 07d6c25f-baf5-f7d6-d225-0447e0f78fe6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844993(v=office.15)
ms:contentKeyID: 48543085
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101180
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ea75da06c0db4eeb4e846bacfddc9f125c03fc84
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307493"
---
# <a name="recordset2batchcollisions-property-dao"></a>Recordset2.BatchCollisions (DAO)


**Se aplica a:** Access 2013, Office 2013

## <a name="syntax"></a>Sintaxis

*expresión* . BatchCollisions

*expresión* Variable que representa un objeto **Recordset2.**

## <a name="remarks"></a>Comentarios

Esta propiedad contiene una matriz de marcadores para las filas en las que se produce un conflicto durante el último intento de llamada de actualización por lotes **[Update](recordset2-update-method-dao.md)**. La propiedad **[BatchCollisionCount](recordset2-batchcollisioncount-property-dao.md)** indica el número de elementos en la matriz.

Si establece la propiedad activa [**Bookmark**](recordset2-bookmark-property-dao.md) del objeto **Recordset** en los valores de marcador en la matriz **BatchCollisions**, podrá desplazarse a cada uno de los registros que no completaron la última operación Update en modo de actualización por lotes.

Después de corregir los registros con conflictos, puede volver a llamar al método **Update** en modo de actualización por lotes. En este punto, DAO intenta otra actualización por lotes y la propiedad **BatchCollisions** refleja otra vez el error que se produjo en el conjunto de registros en el segundo intento. Cualquiera de los registros correctos en el intento anterior no se enviarán en el intento actual puesto que ahora tienen una propiedad **[RecordStatus](recordset2-recordstatus-property-dao.md)** de dbRecordUnmodified. Este proceso puede continuar tanto tiempo como conflictos se produzcan, o hasta que se abandonen las actualizaciones y se cierre el conjunto de resultados.

Esta matriz se vuelve a crear cada vez que se ejecute un método **Update** en modo de actualización por lotes.

