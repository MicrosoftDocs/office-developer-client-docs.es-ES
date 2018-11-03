---
title: Tutorial de RDS (Visual J ++)
TOCTitle: RDS tutorial (Visual J++)
ms:assetid: b5679bfe-e830-05df-8a1c-0744c96abe90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249870(v=office.15)
ms:contentKeyID: 48547248
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e23af46ac7aab267eb5788aa4790d5c568f23609
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946128"
---
# <a name="rds-tutorial-visual-j"></a><span data-ttu-id="21c50-102">Tutorial de RDS (Visual J ++)</span><span class="sxs-lookup"><span data-stu-id="21c50-102">RDS tutorial (Visual J++)</span></span>


<span data-ttu-id="21c50-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="21c50-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="21c50-p101">ADO/WFC no sigue completamente el modelo de objetos RDS, ya que no implementa el objeto [RDS.DataControl](datacontrol-object-rds.md). ADO/WFC sólo implementa la clase de la parte cliente, [RDS.DataSpace](dataspace-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="21c50-p101">ADO/WFC does not completely follow the RDS object model in that it does not implement the [RDS.DataControl](datacontrol-object-rds.md) object. ADO/WFC only implements the client-side class, [RDS.DataSpace](dataspace-object-rds.md).</span></span>

<span data-ttu-id="21c50-p102">La clase **DataSpace** implementa un método, [CreateObject](createobject-method-rds.md), que devuelve un objeto [ObjectProxy](https://msdn.microsoft.com/library/jj249624\(v=office.15\)). La clase **DataSpace** también implementa la propiedad [InternetTimeout](internettimeout-property-rds.md).</span><span class="sxs-lookup"><span data-stu-id="21c50-p102">The **DataSpace** class implements one method, [CreateObject](createobject-method-rds.md), which returns an [ObjectProxy](https://msdn.microsoft.com/library/jj249624\(v=office.15\)) object. The **DataSpace** class also implements the [InternetTimeout](internettimeout-property-rds.md) property.</span></span>

<span data-ttu-id="21c50-108">La clase **ObjectProxy** implementa un método, call, que puede llamar a cualquier objeto de negocio de servidor.</span><span class="sxs-lookup"><span data-stu-id="21c50-108">The **ObjectProxy** class implements one method, call, which can invoke any server-side business object.</span></span>

<span data-ttu-id="21c50-109">**Éste es el principio del tutorial.**</span><span class="sxs-lookup"><span data-stu-id="21c50-109">**This is the beginning of the tutorial.**</span></span>

```java 
 
import com.ms.wfc.data.*; 
public class RDSTutorial 
{ 
 public void tutorial() 
 { 
// Step 1: Specify a server program. 
 ObjectProxy obj = 
 DataSpace.createObject( 
 "RDSServer.DataFactory", 
 "https://YourServer"); 
 
// Step 2: Server returns a Recordset. 
 Recordset rs = (Recordset) obj.call( 
 "Query", 
 new Object[] {"DSN=Pubs;", "SELECT * FROM Authors"}); 
 
// Step 3: Changes are sent to the server. 
 ... // Edit Recordset. 
 obj.call( 
 "SubmitChanges", 
 new Object[] {"DSN=Pubs;", rs}); 
 return; 
 } 
} 
```

<span data-ttu-id="21c50-110">**Éste es el final del tutorial.**</span><span class="sxs-lookup"><span data-stu-id="21c50-110">**This is the end of the tutorial.**</span></span>

