---
title: Cláusulas COMPUTE de Shape intermedias
TOCTitle: Intervening Shape COMPUTE clauses
ms:assetid: 3e9dcef2-776c-0365-4a92-68e325f7dbb5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249174(v=office.15)
ms:contentKeyID: 48544380
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1f8edc3b1e873234b04eca0feb7a4e9c36e71e9c
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945883"
---
# <a name="intervening-shape-compute-clauses"></a><span data-ttu-id="ffdf3-102">Cláusulas COMPUTE de Shape intermedias</span><span class="sxs-lookup"><span data-stu-id="ffdf3-102">Intervening Shape COMPUTE clauses</span></span>


<span data-ttu-id="ffdf3-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ffdf3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ffdf3-104">Es posible incrustar cláusulas COMPUTE entre el elemento principal y el secundario de un comando Shape parametrizado, como en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="ffdf3-104">It is valid to embed one or more COMPUTE clauses between the parent and child in a parameterized shape command, as in the following example:</span></span>

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

