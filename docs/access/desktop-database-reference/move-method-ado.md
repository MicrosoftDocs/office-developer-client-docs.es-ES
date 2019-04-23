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
# <a name="move-method-ado"></a><span data-ttu-id="3fa60-102">Move (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="3fa60-102">Move method (ADO)</span></span>

<span data-ttu-id="3fa60-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3fa60-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3fa60-104">Mueve la posición del actual registro en un objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="3fa60-104">Moves the position of the current record in a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fa60-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3fa60-105">Syntax</span></span>

<span data-ttu-id="3fa60-106">*objeto Recordset*. Move *NumRecords*, *Start*</span><span class="sxs-lookup"><span data-stu-id="3fa60-106">*recordset*.Move *NumRecords*, *Start*</span></span>

## <a name="parameters"></a><span data-ttu-id="3fa60-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3fa60-107">Parameters</span></span>

|<span data-ttu-id="3fa60-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3fa60-108">Parameter</span></span>|<span data-ttu-id="3fa60-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="3fa60-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="3fa60-110">*NumRecords*</span><span class="sxs-lookup"><span data-stu-id="3fa60-110">*NumRecords*</span></span> |<span data-ttu-id="3fa60-111">Expresión de tipo **Long** con signo que especifica, en número de registros, el desplazamiento de la posición de registro actual.</span><span class="sxs-lookup"><span data-stu-id="3fa60-111">A signed **Long** expression that specifies the number of records that the current record position moves.</span></span>|
|<span data-ttu-id="3fa60-112">*Start*</span><span class="sxs-lookup"><span data-stu-id="3fa60-112">*Start*</span></span> |<span data-ttu-id="3fa60-p101">Es opcional. Valor de tipo **String** o **Variant** que da como resultado un marcador. También se puede utilizar un valor de [BookmarkEnum](bookmarkenum.md).</span><span class="sxs-lookup"><span data-stu-id="3fa60-p101">Optional. A **String** value or **Variant** that evaluates to a bookmark. You can also use a [BookmarkEnum](bookmarkenum.md) value.</span></span>|

## <a name="remarks"></a><span data-ttu-id="3fa60-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3fa60-116">Remarks</span></span>

<span data-ttu-id="3fa60-117">El método **Move** se admite en todos los objetos **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="3fa60-117">The **Move** method is supported on all **Recordset** objects.</span></span>

<span data-ttu-id="3fa60-p102">Si el argumento *NumRecords* es mayor que cero, la posición de registro activo avanza (hacia el final del **conjunto de registros**). Si *NumRecords* es menor que cero, la posición de registro activo retrocede (hacia el principio del **conjunto de registros**).</span><span class="sxs-lookup"><span data-stu-id="3fa60-p102">If the *NumRecords* argument is greater than zero, the current record position moves forward (toward the end of the **Recordset**). If *NumRecords* is less than zero, the current record position moves backward (toward the beginning of the **Recordset**).</span></span>

<span data-ttu-id="3fa60-120">Si la llamada a **Move** mueve la posición del registro activo a un punto anterior al primer registro, ADO establece el registro actual en la posición anterior al primer registro del conjunto de registros ([BOF](bof-eof-properties-ado.md) es **true**).</span><span class="sxs-lookup"><span data-stu-id="3fa60-120">If the **Move** call would move the current record position to a point before the first record, ADO sets the current record to the position before the first record in the recordset ([BOF](bof-eof-properties-ado.md) is **True**).</span></span> <span data-ttu-id="3fa60-121">Si el valor de la propiedad **BOF** ya es **True**, cualquier intento de retroceder genera un error.</span><span class="sxs-lookup"><span data-stu-id="3fa60-121">An attempt to move backward when the **BOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="3fa60-p104">Si la llamada a **Move** mueve la posición de registro actual hasta un punto situado después del último registro, ADO establece el registro actual en la posición situada después del último registro del conjunto de registros (el valor de [EOF](bof-eof-properties-ado.md) es **True**). Si el valor de la propiedad **EOF** ya es **True**, cualquier intento de avanzar genera un error.</span><span class="sxs-lookup"><span data-stu-id="3fa60-p104">If the **Move** call would move the current record position to a point after the last record, ADO sets the current record to the position after the last record in the recordset ([EOF](bof-eof-properties-ado.md) is **True**). An attempt to move forward when the **EOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="3fa60-124">Si se llama a **Move** desde un objeto **Recordset** vacío, se genera un error.</span><span class="sxs-lookup"><span data-stu-id="3fa60-124">Calling the **Move** method from an empty **Recordset** object generates an error.</span></span>

<span data-ttu-id="3fa60-p105">Si pasa el argumento *Start*, el desplazamiento se realiza con respecto al registro con este marcador, suponiendo que el objeto **Recordset** admite marcadores. Si no se especifica, el desplazamiento se realiza con respecto al registro actual.</span><span class="sxs-lookup"><span data-stu-id="3fa60-p105">If you pass the *Start* argument, the move is relative to the record with this bookmark, assuming the **Recordset** object supports bookmarks. If not specified, the move is relative to the current record.</span></span>

<span data-ttu-id="3fa60-p106">Si se utiliza la propiedad [CacheSize](cachesize-property-ado.md) para almacenar localmente en caché registros del proveedor, el paso de un argumento *NumRecords* que mueve la posición del registro activo fuera del grupo actual de registros almacenados en caché provoca que ADO recupere un nuevo grupo de registros, a partir del registro de destino. La propiedad **CacheSize** determina el tamaño del grupo recién recuperado y el registro de destino es el primer registro recuperado.</span><span class="sxs-lookup"><span data-stu-id="3fa60-p106">If you are using the [CacheSize](cachesize-property-ado.md) property to locally cache records from the provider, passing a *NumRecords* argument that moves the current record position outside the current group of cached records forces ADO to retrieve a new group of records, starting from the destination record. The **CacheSize** property determines the size of the newly retrieved group, and the destination record is the first record retrieved.</span></span>

<span data-ttu-id="3fa60-p107">Si el objeto **Recordset** es de sólo avance, el usuario puede seguir pasando un argumento *NumRecords* cuyo valor sea menor que cero, a condición de que el destino se encuentre dentro del actual conjunto de registros almacenados en caché. Si la llamada a **Move** desplaza la posición de registro actual hacia un registro situado delante del primer registro almacenado en caché, se producirá un error. Por consiguiente, puede utilizar una memoria caché de registros que admita desplazamientos tanto hacia adelante como hacia atrás en lugar de un proveedor que sólo admite desplazamientos hacia adelante. Dado que los registros almacenados en caché se cargan en la memoria, deberá evitar almacenar en caché un número excesivo de registros. Incluso si un objeto **Recordset** de sólo avance admite de esta forma desplazamientos hacia atrás, las llamadas al método [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) en los objetos **Recordset** de sólo avance generarán un error.</span><span class="sxs-lookup"><span data-stu-id="3fa60-p107">If the **Recordset** object is forward only, a user can still pass a *NumRecords* argument less than zero, provided the destination is within the current set of cached records. If the **Move** call would move the current record position to a record before the first cached record, an error will occur. Thus, you can use a record cache that supports full scrolling over a provider that supports only forward scrolling. Because cached records are loaded into memory, you should avoid caching more records than is necessary. Even if a forward-only **Recordset** object supports backward moves in this way, calling the [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) method on any forward-only **Recordset** object will still generate an error.</span></span>


> [!NOTE]
> <span data-ttu-id="3fa60-p108">[!NOTA] La compatibilidad con los desplazamientos hacia atrás en un objeto **Recordset** de sólo avance no es previsible, según el proveedor. Si la posición del actual registro se ha establecido en un punto situado después del último registro del objeto **Recordset**, un **desplazamiento** hacia atrás puede no tener la posición actual correcta como resultado.</span><span class="sxs-lookup"><span data-stu-id="3fa60-p108">Support for moving backwards in a forward-only **Recordset** is not predictable, depending upon your provider. If the current record has been postioned after the last record in the **Recordset**, **Move** backwards may not result in the correct current position.</span></span>


