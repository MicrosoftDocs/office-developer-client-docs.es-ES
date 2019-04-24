---
title: StayInSync (propiedad, ADO)
TOCTitle: StayInSync property (ADO)
ms:assetid: 02c95c10-4032-14e1-e506-f334a8787142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248792(v=office.15)
ms:contentKeyID: 48542966
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bfc9ef5229fe230ad0c83ebde7a887e0fac0c233
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308494"
---
# <a name="stayinsync-property-ado"></a>StayInSync (propiedad, ADO)


**Se aplica a:** Access 2013, Office 2013

En un objeto [Recordset](recordset-object-ado.md) jerárquico, indica si la referencia a los registros secundarios subyacentes (es decir, el *capítulo*) cambia cuando la posición de la fila superior en la jerarquía (elemento principal) cambia.

## <a name="settings-and-return-values"></a>Valores de configuración y devueltos

Establece o devuelve un valor de tipo **Boolean**. El valor predeterminado es **True**. Si es **True**, el capítulo se actualizará si el objeto **Recordset** primario cambia la posición de la fila; si es **False**, seguirá haciendo referencia a los datos del capítulo anterior, aun cuando el objeto **Recordset** primario haya cambiado la posición de la fila.

## <a name="remarks"></a>Comentarios

Esta propiedad se aplica a objetos Recordset jerárquicos, como los admitidos por el [Servicio de forma de datos de Microsoft para OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), y debe establecerse en el objeto **Recordset** primario antes de que el objeto **Recordset** secundario sea recuperado. Esta propiedad simplifica el desplazamiento por los conjuntos de registros jerárquicos.

