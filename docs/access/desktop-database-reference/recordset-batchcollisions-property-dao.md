---
title: Recordset.BatchCollisions Property (DAO)
TOCTitle: BatchCollisions Property
ms:assetid: 53e5572b-770c-9ea5-31a5-984abdf66faa
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194079(v=office.15)
ms:contentKeyID: 48544881
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4818ff1ceda746a0acb72a47e87eda58f87b2dfc
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882605"
---
# <a name="recordsetbatchcollisions-property-dao"></a>Recordset.BatchCollisions Property (DAO)


**Se aplica a**: Access 2013, Office 2013

## <a name="syntax"></a>Sintaxis

*expresión* . BatchCollisions

*expresión* Variable que representa un objeto **Recordset** .

## <a name="remarks"></a>Observaciones

Esta propiedad contiene una matriz de marcadores que hacen referencia a las filas que encontraron un conflicto durante la llamada **[Update](recordset-update-method-dao.md)** del lote que se intentó en último lugar. La propiedad **[BatchCollisionCount](recordset-batchcollisioncount-property-dao.md)** indica el número de elementos de la matriz.

Si se establece la propiedad **[Bookmark](recordset-object-dao.md)** del objeto **[Recordset](recordset-bookmark-property-dao.md)** de trabajo en los valores de marcador de la matriz **BatchCollisions**, puede desplazarse a cada registro que no finalizó la última operación de actualización en modo de proceso por lotes.

Una vez corregidos los registros del conflicto, puede llamar de nuevo al método **Update** en modo de proceso por lotes. En este punto, DAO intenta llevar a cabo otra actualización del lote y la propiedad **BatchCollisions** refleja de nuevo el conjunto de registros con error en el segundo intento. Los registros que finalizaron correctamente en el intento anterior no se envían en el intento actual, ya que ahora tienen una propiedad **[RecordStatus](recordset-recordstatus-property-dao.md)** de dbRecordUnmodified. Este proceso puede continuar hasta que dejen de producirse conflictos o hasta que se abandonen las actualizaciones y se cierre el conjunto de resultados.

Esta matriz se vuelve a crear cada vez que se ejecuta un método **Update** en modo de proceso por lotes.

