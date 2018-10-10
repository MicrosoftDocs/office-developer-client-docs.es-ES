---
title: Mover el método - ActiveX Data Objects (ADO)
TOCTitle: Move Method (ADO)
ms:assetid: 1f858654-5fa3-273d-7cdc-574c5f09a420
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248982(v=office.15)
ms:contentKeyID: 48543645
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 88787d1f76f84db13feea4bac0e8febd2db1e473
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484215"
---
# <a name="move-method-ado"></a>Move (método, ADO)


**Se aplica a**: Access 2013 | Office 2013



Mueve la posición del actual registro en un objeto [Recordset](recordset-object-ado.md).

## <a name="syntax"></a>Sintaxis

*conjunto de registros*. Mover *NumRecords*, *Iniciar*

## <a name="parameters"></a>Parámetros

  - *NumRecords*

  - Expresión de tipo **Long** con signo que especifica, en número de registros, el desplazamiento de la posición de registro actual.

  - *Start*

  - Es opcional. Valor de tipo **String** o **Variant** que da como resultado un marcador. También se puede utilizar un valor de [BookmarkEnum](bookmarkenum.md).

## <a name="remarks"></a>Comentarios

El método **Move** se admite en todos los objetos **Recordset**.

Si el argumento *NumRecords* es mayor que cero, la posición de registro activo avanza (hacia el final del **conjunto de registros**). Si *NumRecords* es menor que cero, la posición de registro activo retrocede (hacia el principio del **conjunto de registros**).

Si la llamada a **Move** mueve la posición de registro actual hasta un punto delante del primer registro, ADO establece el registro actual a la posición antes del primer registro del objeto Recordset (el[valor de BOF](bof-eof-properties-ado.md) es **True**). Si el valor de la propiedad **BOF** ya es **True**, cualquier intento de retroceder genera un error.

Si la llamada a **Move** mueve la posición de registro actual hasta un punto después del último registro, ADO establece el registro actual a la posición después del último registro del objeto Recordset ([EOF](bof-eof-properties-ado.md) es **True**). Si el valor de la propiedad **EOF** ya es **True**, cualquier intento de avanzar genera un error.

Si se llama a **Move** desde un objeto **Recordset** vacío, se genera un error.

Si se pasa el argumento *Start* , el movimiento es respecto al registro con este marcador, suponiendo que el objeto **Recordset** admite marcadores. Si no se especifica, el desplazamiento se realiza con respecto al registro actual.

Si se utiliza la propiedad [CacheSize](cachesize-property-ado.md) para localmente en caché registros del proveedor, pasando un argumento *NumRecords* que mueve la posición de registro actual fuera del actual grupo de registros almacenados en caché obliga a ADO para recuperar un nuevo grupo de registros, empezando por el registro de destino. La propiedad **CacheSize** determina el tamaño del nuevo grupo recuperado y el registro de destino es el primer registro recuperado.

Si el objeto **Recordset** es de sólo avance, un usuario puede pasar aún un argumento *NumRecords cuyo valor sea* menor que cero, siempre que el destino es dentro del conjunto actual de registros almacenados en caché. Si la llamada a **Move** desplaza la posición de registro actual hacia un registro situado delante del primer registro almacenado en caché, se producirá un error. Por consiguiente, puede utilizar una memoria caché de registros que admita desplazamientos tanto hacia adelante como hacia atrás en lugar de un proveedor que sólo admite desplazamientos hacia adelante. Dado que los registros almacenados en caché se cargan en la memoria, deberá evitar almacenar en caché un número excesivo de registros. Incluso si un objeto **Recordset** de sólo avance admite de esta forma desplazamientos hacia atrás, las llamadas al método [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) en los objetos **Recordset** de sólo avance generarán un error.


> [!NOTE]
> [!NOTA] La compatibilidad con los desplazamientos hacia atrás en un objeto **Recordset** de sólo avance no es previsible, según el proveedor. Si la posición del actual registro se ha establecido en un punto situado después del último registro del objeto **Recordset**, un **desplazamiento** hacia atrás puede no tener la posición actual correcta como resultado.


