---
title: Recordset2.BatchCollisions Property (DAO)
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
ms.openlocfilehash: ee26b84237b1bf4a8603295a6e6d66e6f30303e9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885895"
---
# <a name="recordset2batchcollisions-property-dao"></a>Recordset2.BatchCollisions Property (DAO)


**Se aplica a**: Access 2013, Office 2013

## <a name="syntax"></a>Sintaxis

*expresión* . BatchCollisions

*expresión* Variable que representa un objeto **Recordset2** .

## <a name="remarks"></a>Observaciones

Esta propiedad contiene una matriz de marcadores para las filas en las que se produce un conflicto durante el último intento de llamada de actualización por lotes **[Update](recordset2-update-method-dao.md)**. La propiedad **[BatchCollisionCount](recordset2-batchcollisioncount-property-dao.md)** indica el número de elementos en la matriz.

Si establece la propiedad activa [**Bookmark**](recordset2-bookmark-property-dao.md) del objeto **Recordset** en los valores de marcador en la matriz **BatchCollisions**, podrá desplazarse a cada uno de los registros que no completaron la última operación Update en modo de actualización por lotes.

Después de corregir los registros con conflictos, puede volver a llamar al método **Update** en modo de actualización por lotes. En este punto, DAO intenta otra actualización por lotes y la propiedad **BatchCollisions** refleja otra vez el error que se produjo en el conjunto de registros en el segundo intento. Cualquiera de los registros correctos en el intento anterior no se enviarán en el intento actual puesto que ahora tienen una propiedad **[RecordStatus](recordset2-recordstatus-property-dao.md)** de dbRecordUnmodified. Este proceso puede continuar tanto tiempo como conflictos se produzcan, o hasta que se abandonen las actualizaciones y se cierre el conjunto de resultados.

Esta matriz se vuelve a crear cada vez que se ejecuta un método **Update** en modo de proceso por lotes.

