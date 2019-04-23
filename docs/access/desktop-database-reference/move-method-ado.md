---
title: Move Method-ActiveX Data Objects (ADO)
TOCTitle: Move method (ADO)
ms:assetid: 1f858654-5fa3-273d-7cdc-574c5f09a420
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248982(v=office.15)
ms:contentKeyID: 48543645
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6c7db661e590bc21605d9c289b1de6d4ae9f46e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288837"
---
# <a name="move-method-ado"></a>Move (método, ADO)

**Se aplica a:** Access 2013, Office 2013

Mueve la posición del actual registro en un objeto [Recordset](recordset-object-ado.md).

## <a name="syntax"></a>Sintaxis

*objeto Recordset*. Move *NumRecords*, *Start*

## <a name="parameters"></a>Parámetros

|Parameter|Descripción|
|:--------|:----------|
|*NumRecords* |Expresión de tipo **Long** con signo que especifica, en número de registros, el desplazamiento de la posición de registro actual.|
|*Start* |Es opcional. Valor de tipo **String** o **Variant** que da como resultado un marcador. También se puede utilizar un valor de [BookmarkEnum](bookmarkenum.md).|

## <a name="remarks"></a>Comentarios

El método **Move** se admite en todos los objetos **Recordset**.

Si el argumento *NumRecords* es mayor que cero, la posición de registro activo avanza (hacia el final del **conjunto de registros**). Si *NumRecords* es menor que cero, la posición de registro activo retrocede (hacia el principio del **conjunto de registros**).

Si la llamada a **Move** mueve la posición del registro activo a un punto anterior al primer registro, ADO establece el registro actual en la posición anterior al primer registro del conjunto de registros ([BOF](bof-eof-properties-ado.md) es **true**). Si el valor de la propiedad **BOF** ya es **True**, cualquier intento de retroceder genera un error.

Si la llamada a **Move** mueve la posición de registro actual hasta un punto situado después del último registro, ADO establece el registro actual en la posición situada después del último registro del conjunto de registros (el valor de [EOF](bof-eof-properties-ado.md) es **True**). Si el valor de la propiedad **EOF** ya es **True**, cualquier intento de avanzar genera un error.

Si se llama a **Move** desde un objeto **Recordset** vacío, se genera un error.

Si pasa el argumento *Start*, el desplazamiento se realiza con respecto al registro con este marcador, suponiendo que el objeto **Recordset** admite marcadores. Si no se especifica, el desplazamiento se realiza con respecto al registro actual.

Si se utiliza la propiedad [CacheSize](cachesize-property-ado.md) para almacenar localmente en caché registros del proveedor, el paso de un argumento *NumRecords* que mueve la posición del registro activo fuera del grupo actual de registros almacenados en caché provoca que ADO recupere un nuevo grupo de registros, a partir del registro de destino. La propiedad **CacheSize** determina el tamaño del grupo recién recuperado y el registro de destino es el primer registro recuperado.

Si el objeto **Recordset** es de sólo avance, el usuario puede seguir pasando un argumento *NumRecords* cuyo valor sea menor que cero, a condición de que el destino se encuentre dentro del actual conjunto de registros almacenados en caché. Si la llamada a **Move** desplaza la posición de registro actual hacia un registro situado delante del primer registro almacenado en caché, se producirá un error. Por consiguiente, puede utilizar una memoria caché de registros que admita desplazamientos tanto hacia adelante como hacia atrás en lugar de un proveedor que sólo admite desplazamientos hacia adelante. Dado que los registros almacenados en caché se cargan en la memoria, deberá evitar almacenar en caché un número excesivo de registros. Incluso si un objeto **Recordset** de sólo avance admite de esta forma desplazamientos hacia atrás, las llamadas al método [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) en los objetos **Recordset** de sólo avance generarán un error.


> [!NOTE]
> [!NOTA] La compatibilidad con los desplazamientos hacia atrás en un objeto **Recordset** de sólo avance no es previsible, según el proveedor. Si la posición del actual registro se ha establecido en un punto situado después del último registro del objeto **Recordset**, un **desplazamiento** hacia atrás puede no tener la posición actual correcta como resultado.


