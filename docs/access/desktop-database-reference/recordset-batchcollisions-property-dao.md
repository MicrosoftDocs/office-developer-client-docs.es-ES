---
title: Propiedad Recordset. BatchCollisions (DAO)
TOCTitle: BatchCollisions Property
ms:assetid: 53e5572b-770c-9ea5-31a5-984abdf66faa
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194079(v=office.15)
ms:contentKeyID: 48544881
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 61f60567ac170a0ecde2d4bd46589d2308b7788f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300864"
---
# <a name="recordsetbatchcollisions-property-dao"></a>Propiedad Recordset. BatchCollisions (DAO)


**Se aplica a:** Access 2013, Office 2013

## <a name="syntax"></a>Sintaxis

*expresión* . BatchCollisions

*expresión* Variable que representa un objeto **Recordset** .

## <a name="remarks"></a>Comentarios

Esta propiedad contiene una matriz de marcadores que hacen referencia a las filas que encontraron un conflicto durante la llamada **[Update](recordset-update-method-dao.md)** del lote que se intentó en último lugar. La propiedad **[BatchCollisionCount](recordset-batchcollisioncount-property-dao.md)** indica el número de elementos de la matriz.

Si se establece la propiedad **[Bookmark](recordset-object-dao.md)** del objeto **[Recordset](recordset-bookmark-property-dao.md)** de trabajo en los valores de marcador de la matriz **BatchCollisions**, puede desplazarse a cada registro que no finalizó la última operación de actualización en modo de proceso por lotes.

Una vez corregidos los registros del conflicto, puede llamar de nuevo al método **Update** en modo de proceso por lotes. En este punto, DAO intenta llevar a cabo otra actualización del lote y la propiedad **BatchCollisions** refleja de nuevo el conjunto de registros con error en el segundo intento. Los registros que finalizaron correctamente en el intento anterior no se envían en el intento actual, ya que ahora tienen una propiedad **[RecordStatus](recordset-recordstatus-property-dao.md)** de dbRecordUnmodified. Este proceso puede continuar hasta que dejen de producirse conflictos o hasta que se abandonen las actualizaciones y se cierre el conjunto de resultados.

Esta matriz se vuelve a crear cada vez que se ejecute un método **Update** en modo de actualización por lotes.

