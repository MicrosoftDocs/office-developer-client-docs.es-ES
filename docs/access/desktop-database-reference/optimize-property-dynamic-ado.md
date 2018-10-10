---
title: dinámica Optimize (propiedad, ADO)
TOCTitle: Optimize Property--Dynamic (ADO)
ms:assetid: 2253b052-2d8a-f6f0-f8b8-f56e79d243de
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249001(v=office.15)
ms:contentKeyID: 48543705
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6c31950eda813ee4f3f07145d28a83106cf86b3f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484446"
---
# <a name="optimize-property--dynamic-ado"></a><span data-ttu-id="005b4-102">dinámica Optimize (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="005b4-102">Optimize Property--Dynamic (ADO)</span></span>


<span data-ttu-id="005b4-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="005b4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="005b4-104">Especifica si se debe crear un índice en un campo.</span><span class="sxs-lookup"><span data-stu-id="005b4-104">Specifies whether an index should be created on a field.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="005b4-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="005b4-105">Settings and Return Values</span></span>

<span data-ttu-id="005b4-106">Establece o devuelve un valor de tipo **Boolean** que indica si se debe crear un índice.</span><span class="sxs-lookup"><span data-stu-id="005b4-106">Sets or returns a **Boolean** value that indicates whether an index should be created.</span></span>

## <a name="remarks"></a><span data-ttu-id="005b4-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="005b4-107">Remarks</span></span>

<span data-ttu-id="005b4-p101">Un índice puede mejorar el rendimiento de operaciones que buscan u ordenan valores de un objeto [Recordset](recordset-object-ado.md). El índice es interno a ADO: no es posible obtener acceso a él de forma explícita ni usarlo en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="005b4-p101">An index can improve the performance of operations that find or sort values in a [Recordset](recordset-object-ado.md). The index is internal to ADO — you cannot explicitly access or use it in your application.</span></span>

<span data-ttu-id="005b4-p102">Para crear un índice en un campo, establezca la propiedad **Optimize** en **True**. Para eliminar el índice, establezca esta propiedad en **False**.</span><span class="sxs-lookup"><span data-stu-id="005b4-p102">To create an index on a field, set the **Optimize** property to **True**. To delete the index, set this property to **False**.</span></span>

<span data-ttu-id="005b4-112">**Optimize** es una propiedad dinámica que se anexa a la colección [Properties](field-object-ado.md) del objeto [Field](properties-collection-ado.md) cuando la propiedad [CursorLocation](cursorlocation-property-ado.md) está establecida en **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="005b4-112">**Optimize** is a dynamic property appended to the [Field](field-object-ado.md) object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

<span data-ttu-id="005b4-113">**Uso**</span><span class="sxs-lookup"><span data-stu-id="005b4-113">**Usage**</span></span>

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
