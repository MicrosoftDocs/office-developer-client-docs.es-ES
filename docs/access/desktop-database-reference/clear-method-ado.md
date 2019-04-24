---
title: Clear Method-ActiveX Data Objects (ADO)
TOCTitle: Clear method (ADO)
ms:assetid: 5d51f42c-147b-1fcf-d05b-123e5714ecb7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249329(v=office.15)
ms:contentKeyID: 48545110
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b0d76480bdb5d5a3ab258e103a00707af303a4d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296363"
---
# <a name="clear-method-ado"></a><span data-ttu-id="30d43-102">Clear (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="30d43-102">Clear method (ADO)</span></span>


<span data-ttu-id="30d43-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="30d43-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="30d43-104">Quita todos los objetos **Error** de la colección **Errors**.</span><span class="sxs-lookup"><span data-stu-id="30d43-104">Removes all the **Error** objects from the **Errors** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="30d43-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="30d43-105">Syntax</span></span>

<span data-ttu-id="30d43-106">*Errores*. Desactiva</span><span class="sxs-lookup"><span data-stu-id="30d43-106">*Errors*.Clear</span></span>

## <a name="remarks"></a><span data-ttu-id="30d43-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="30d43-107">Remarks</span></span>

<span data-ttu-id="30d43-p101">Utilice el método **Clear** en la colección [Errors](errors-collection-ado.md) para quitar todos los objetos [Error](error-object-ado.md) de la colección. Cuando se produce un error, ADO borra automáticamente la colección **Errors** y la rellena con objetos **Error** basándose en el nuevo error.</span><span class="sxs-lookup"><span data-stu-id="30d43-p101">Use the **Clear** method on the [Errors](errors-collection-ado.md) collection to remove all existing [Error](error-object-ado.md) objects from the collection. When an error occurs, ADO automatically clears the **Errors** collection and fills it with **Error** objects based on the new error.</span></span>

<span data-ttu-id="30d43-p102">Algunos métodos y propiedades devuelven advertencias que aparecen como objetos **Error** en la colección **Errors** pero que no detienen la ejecución de un programa. Antes de llamar a los métodos [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) o [CancelBatch](cancelbatch-method-ado.md) en un objeto [Recordset](recordset-object-ado.md), antes de llamar al método [Open](open-method-ado-connection.md) en un objeto [Connection](connection-object-ado.md), y antes de establecer la propiedad [Filter](filter-property-ado.md) de un objeto **Recordset**, llame al método **Clear** en la colección **Errors**. De este modo, podrá leer la propiedad [Count](count-property-ado.md) de la colección **Errors** y comprobar si hay advertencias devueltas.</span><span class="sxs-lookup"><span data-stu-id="30d43-p102">Some properties and methods return warnings that appear as **Error** objects in the **Errors** collection but do not halt a program's execution. Before you call the [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), or [CancelBatch](cancelbatch-method-ado.md) methods on a [Recordset](recordset-object-ado.md) object; the [Open](open-method-ado-connection.md) method on a [Connection](connection-object-ado.md) object; or set the [Filter](filter-property-ado.md) property on a **Recordset** object, call the **Clear** method on the **Errors** collection. That way, you can read the [Count](count-property-ado.md) property of the **Errors** collection to test for returned warnings.</span></span>

