---
title: Adición de varios campos
TOCTitle: Adding multiple fields
ms:assetid: 81b2f9de-4805-4494-9990-09ffda1b2068
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249560(v=office.15)
ms:contentKeyID: 48545961
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bc9822f2055e7cdfd9a2ef5fe9d2312fc5622ac7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280591"
---
# <a name="adding-multiple-fields"></a><span data-ttu-id="6723f-102">Adición de varios campos</span><span class="sxs-lookup"><span data-stu-id="6723f-102">Adding multiple fields</span></span>

<span data-ttu-id="6723f-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6723f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6723f-p101">En ocasiones, podría resultar más eficaz pasar una matriz de campos y sus correspondientes valores al método **AddNew** que establecer **Value** varias veces para cada nuevo campo. Si *FieldList* es una matriz, *Values* también debe ser una matriz con el mismo número de elementos; de lo contrario, se produce un error. El orden de los nombres de campo debe coincidir con el orden de los valores de campo en cada matriz. El código siguiente pasa una matriz de campos y una matriz de valores al método **AddNew**.</span><span class="sxs-lookup"><span data-stu-id="6723f-p101">Occasionally, it might be more efficient to pass in an array of fields and their corresponding values to the **AddNew** method, rather than setting **Value** multiple times for each new field. If *FieldList* is an array, *Values* must also be an array with the same number of members; otherwise, an error occurs. The order of field names must match the order of field values in each array. The following code passes an array of fields and an array of values to the **AddNew** method.</span></span>

```vb 
 
'BeginAddNew2 
 Dim avarFldNames As Variant 
 Dim avarFldValues As Variant 
 
 avarFldNames = Array("CompanyName", "Phone") 
 avarFldValues = Array("Sample Shipper 2", "(931) 555-6334") 
 
 If objRs1.Supports(adAddNew) Then 
 objRs1.AddNew avarFldNames, avarFldValues 
 End If 
 
 'Re-establish a Connection and update 
 Set objRs1.ActiveConnection = GetNewConnection 
 objRs1.UpdateBatch 
'EndAddNew2 
```

