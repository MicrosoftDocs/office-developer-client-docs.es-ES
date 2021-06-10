---
title: Propiedad CursorLocation (ADO)
TOCTitle: CursorLocation property (ADO)
ms:assetid: 8a048bd4-ae25-a555-1c07-14364b7e6560
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249606(v=office.15)
ms:contentKeyID: 48546182
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 25fd81acee3c541c8a3f315f96fa69241272a655
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295223"
---
# <a name="cursorlocation-property-ado"></a><span data-ttu-id="51bc6-102">Propiedad CursorLocation (ADO)</span><span class="sxs-lookup"><span data-stu-id="51bc6-102">CursorLocation property (ADO)</span></span>


<span data-ttu-id="51bc6-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="51bc6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="51bc6-104">Indica la ubicación del servicio de cursores.</span><span class="sxs-lookup"><span data-stu-id="51bc6-104">Indicates the location of the cursor service.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="51bc6-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="51bc6-105">Settings And Return Values</span></span>

<span data-ttu-id="51bc6-106">Establece o devuelve un valor de tipo **Long** que puede establecerse en uno de los valores de [CursorLocationEnum](cursorlocationenum.md).</span><span class="sxs-lookup"><span data-stu-id="51bc6-106">Sets or returns a **Long** value that can be set to one of the [CursorLocationEnum](cursorlocationenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="51bc6-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="51bc6-107">Remarks</span></span>

<span data-ttu-id="51bc6-p101">Esta propiedad permite elegir entre varias bibliotecas de cursores accesibles para el proveedor. Normalmente, se puede elegir entre una biblioteca de cursores de cliente y otra ubicada en el servidor.</span><span class="sxs-lookup"><span data-stu-id="51bc6-p101">This property allows you to choose between various cursor libraries accessible to the provider. Usually, you can choose between using a client-side cursor library or one that is located on the server.</span></span>

<span data-ttu-id="51bc6-p102">El valor de esta propiedad afecta sólo a las conexiones establecidas después de la configuración de la propiedad. Si se modifica la propiedad **CursorLocation**, no se verán afectadas las conexiones existentes.</span><span class="sxs-lookup"><span data-stu-id="51bc6-p102">This property setting affects connections established only after the property has been set. Changing the **CursorLocation** property has no effect on existing connections.</span></span>

<span data-ttu-id="51bc6-p103">Los cursores devueltos por el método [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) heredan este valor de configuración. Los objetos **Recordset** heredarán automáticamente este valor de sus conexiones asociadas.</span><span class="sxs-lookup"><span data-stu-id="51bc6-p103">Cursors returned by the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) method inherit this setting. **Recordset** objects will automatically inherit this setting from their associated connections.</span></span>

<span data-ttu-id="51bc6-114">Esta propiedad es de lectura y escritura en un objeto [Connection](connection-object-ado.md) o un objeto [Recordset](recordset-object-ado.md) cerrado, y es de sólo lectura en un objeto **Recordset** abierto.</span><span class="sxs-lookup"><span data-stu-id="51bc6-114">This property is read/write on a [Connection](connection-object-ado.md) or a closed [Recordset](recordset-object-ado.md), and read-only on an open **Recordset**.</span></span>

<span data-ttu-id="51bc6-115">**Uso del servicio de datos remotos** Cuando se usa en un objeto **Recordset** o **Connection** del lado cliente, la **propiedad CursorLocation** solo se puede establecer en **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="51bc6-115">**Remote Data Service Usage** When used on a client-side **Recordset** or **Connection** object, the **CursorLocation** property can only be set to **adUseClient**.</span></span>

