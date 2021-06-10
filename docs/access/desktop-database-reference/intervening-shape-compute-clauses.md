---
title: Cláusulas COMPUTE de formas que intervienen
TOCTitle: Intervening Shape COMPUTE clauses
ms:assetid: 3e9dcef2-776c-0365-4a92-68e325f7dbb5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249174(v=office.15)
ms:contentKeyID: 48544380
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 456729bb93d6cfaf2844d71123cd850d7f719844
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291251"
---
# <a name="intervening-shape-compute-clauses"></a><span data-ttu-id="945b1-102">Cláusulas COMPUTE de formas que intervienen</span><span class="sxs-lookup"><span data-stu-id="945b1-102">Intervening Shape COMPUTE clauses</span></span>


<span data-ttu-id="945b1-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="945b1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="945b1-104">Es posible incrustar cláusulas COMPUTE entre el elemento principal y el secundario de un comando Shape parametrizado, como en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="945b1-104">It is valid to embed one or more COMPUTE clauses between the parent and child in a parameterized shape command, as in the following example:</span></span>

```vb 
 
SHAPE {select au_lname, state from authors} APPEND 
 ((SHAPE 
 (SHAPE 
 {select * from authors where state = ?} rs 
 COMPUTE rs, ANY(rs.state) state, ANY(rs.au_lname) au_lname 
 BY au_id) rs2 
 COMPUTE rs2, ANY(rs2.state) BY au_lname) 
RELATE state TO PARAMETER 0) 
```

