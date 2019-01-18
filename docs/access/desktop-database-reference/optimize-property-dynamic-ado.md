---
title: Optimizar dinámico (propiedad, ADO)
TOCTitle: Optimize dynamic property (ADO)
ms:assetid: 2253b052-2d8a-f6f0-f8b8-f56e79d243de
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249001(v=office.15)
ms:contentKeyID: 48543705
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 11bb7872514a828fdd97fb404f5366c35ff9a883
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709414"
---
# <a name="optimize-dynamic-property-ado"></a><span data-ttu-id="b2fd5-102">Optimizar dinámico (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="b2fd5-102">Optimize dynamic property (ADO)</span></span>


<span data-ttu-id="b2fd5-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b2fd5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b2fd5-104">Especifica si se debe crear un índice en un campo.</span><span class="sxs-lookup"><span data-stu-id="b2fd5-104">Specifies whether an index should be created on a field.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="b2fd5-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="b2fd5-105">Settings and return values</span></span>

<span data-ttu-id="b2fd5-106">Establece o devuelve un valor de tipo **Boolean** que indica si se debe crear un índice.</span><span class="sxs-lookup"><span data-stu-id="b2fd5-106">Sets or returns a **Boolean** value that indicates whether an index should be created.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2fd5-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b2fd5-107">Remarks</span></span>

<span data-ttu-id="b2fd5-p101">Un índice puede mejorar el rendimiento de operaciones que buscan u ordenan valores de un objeto [Recordset](recordset-object-ado.md). El índice es interno a ADO: no es posible obtener acceso a él de forma explícita ni usarlo en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b2fd5-p101">An index can improve the performance of operations that find or sort values in a [Recordset](recordset-object-ado.md). The index is internal to ADO — you cannot explicitly access or use it in your application.</span></span>

<span data-ttu-id="b2fd5-p102">Para crear un índice en un campo, establezca la propiedad **Optimize** en **True**. Para eliminar el índice, establezca esta propiedad en **False**.</span><span class="sxs-lookup"><span data-stu-id="b2fd5-p102">To create an index on a field, set the **Optimize** property to **True**. To delete the index, set this property to **False**.</span></span>

<span data-ttu-id="b2fd5-112">**Optimize** es una propiedad dinámica que se anexa a la colección [Properties](field-object-ado.md) del objeto [Field](properties-collection-ado.md) cuando la propiedad [CursorLocation](cursorlocation-property-ado.md) está establecida en **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="b2fd5-112">**Optimize** is a dynamic property appended to the [Field](field-object-ado.md) object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

<span data-ttu-id="b2fd5-113">**Uso**</span><span class="sxs-lookup"><span data-stu-id="b2fd5-113">**Usage**</span></span>

```vb
    Dim rs As New Recordset
    Dim fld As Field
    rs.CursorLocation = adUseClient      'Enable index creation
    rs.Fields.Append "Field1", adChar, 35, adFldIsNullable
    rs.Open
    Set fld = rs.Fields(0)
    fld.Properties("Optimize") = True    'Create an index
    fld.Properties("Optimize") = False   'Delete an index
```
