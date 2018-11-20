---
title: CursorLocation (propiedad, ADO)
TOCTitle: CursorLocation property (ADO)
ms:assetid: 8a048bd4-ae25-a555-1c07-14364b7e6560
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249606(v=office.15)
ms:contentKeyID: 48546182
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 874662585292b9d9a9b2bc53f5b6fe5178e3517b
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025850"
---
# <a name="cursorlocation-property-ado"></a><span data-ttu-id="24249-102">CursorLocation (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="24249-102">CursorLocation property (ADO)</span></span>


<span data-ttu-id="24249-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="24249-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="24249-104">Indica la ubicación del servicio de cursores.</span><span class="sxs-lookup"><span data-stu-id="24249-104">Indicates the location of the cursor service.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="24249-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="24249-105">Settings And Return Values</span></span>

<span data-ttu-id="24249-106">Establece o devuelve un valor de tipo **Long** que puede establecerse en uno de los valores de [CursorLocationEnum](cursorlocationenum.md).</span><span class="sxs-lookup"><span data-stu-id="24249-106">Sets or returns a **Long** value that can be set to one of the [CursorLocationEnum](cursorlocationenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="24249-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="24249-107">Remarks</span></span>

<span data-ttu-id="24249-p101">Esta propiedad permite elegir entre varias bibliotecas de cursores accesibles para el proveedor. Normalmente, se puede elegir entre una biblioteca de cursores de cliente y otra ubicada en el servidor.</span><span class="sxs-lookup"><span data-stu-id="24249-p101">This property allows you to choose between various cursor libraries accessible to the provider. Usually, you can choose between using a client-side cursor library or one that is located on the server.</span></span>

<span data-ttu-id="24249-p102">El valor de esta propiedad afecta sólo a las conexiones establecidas después de la configuración de la propiedad. Si se modifica la propiedad **CursorLocation**, no se verán afectadas las conexiones existentes.</span><span class="sxs-lookup"><span data-stu-id="24249-p102">This property setting affects connections established only after the property has been set. Changing the **CursorLocation** property has no effect on existing connections.</span></span>

<span data-ttu-id="24249-p103">Los cursores devueltos por el método [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) heredan este valor de configuración. Los objetos **Recordset** heredarán automáticamente este valor de sus conexiones asociadas.</span><span class="sxs-lookup"><span data-stu-id="24249-p103">Cursors returned by the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) method inherit this setting. **Recordset** objects will automatically inherit this setting from their associated connections.</span></span>

<span data-ttu-id="24249-114">Esta propiedad es de lectura y escritura en un objeto [Connection](connection-object-ado.md) o un objeto [Recordset](recordset-object-ado.md) cerrado, y es de sólo lectura en un objeto **Recordset** abierto.</span><span class="sxs-lookup"><span data-stu-id="24249-114">This property is read/write on a [Connection](connection-object-ado.md) or a closed [Recordset](recordset-object-ado.md), and read-only on an open **Recordset**.</span></span>

<span data-ttu-id="24249-115">**Uso de servicio de datos remotos** Cuando se usa en un objeto de **conexión** o un **conjunto de registros** del lado cliente, sólo puede establecerse la propiedad **CursorLocation** en **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="24249-115">**Remote Data Service Usage**When used on a client-side **Recordset** or **Connection** object, the **CursorLocation** property can only be set to **adUseClient**.</span></span>

