---
title: Resumen del modelo de objetos de RDS
TOCTitle: RDS Object Model Summary
ms:assetid: 0355d62a-dabb-8643-5c43-1e98ccf7f3b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248800(v=office.15)
ms:contentKeyID: 48542981
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4afb0309018b12267f29c23bcde740fdb5a9664e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485231"
---
# <a name="rds-object-model-summary"></a><span data-ttu-id="69cff-102">Resumen del modelo de objetos de RDS</span><span class="sxs-lookup"><span data-stu-id="69cff-102">RDS Object Model Summary</span></span>


<span data-ttu-id="69cff-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="69cff-103">**Applies to**: Access 2013 | Office 2013</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="69cff-104">Objeto</span><span class="sxs-lookup"><span data-stu-id="69cff-104">Object</span></span></p></th>
<th><p><span data-ttu-id="69cff-105">Descripción</span><span class="sxs-lookup"><span data-stu-id="69cff-105">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="69cff-106"><a href="dataspace-object-rds.md">RDS. DataSpace</a></span><span class="sxs-lookup"><span data-stu-id="69cff-106"><a href="dataspace-object-rds.md">RDS.DataSpace</a></span></span></p></td>
<td><p><span data-ttu-id="69cff-p101">Este objeto contiene un método para obtener un proxy de servidor. El proxy puede ser el programa de servidor predeterminado o un programa de servidor personalizado (objeto de negocio). El programa de servidor puede invocarse en Internet, una intranet, una red de área local, o puede ser una biblioteca de vínculos dinámicos local.</span><span class="sxs-lookup"><span data-stu-id="69cff-p101">This object contains a method to obtain a server proxy. The proxy may be the default or a custom server program (business object). The server program may be invoked on the Internet, an intranet, a local area network, or be a local dynamic-link library.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69cff-110"><a href="datafactory-object-rdsserver.md">RDSServer.DataFactory</a></span><span class="sxs-lookup"><span data-stu-id="69cff-110"><a href="datafactory-object-rdsserver.md">RDSServer.DataFactory</a></span></span></p></td>
<td><p><span data-ttu-id="69cff-p102">Este objeto representa el programa de servidor predeterminado.

Ejecuta el comportamiento predeterminado de recuperación y actualización de datos de RDS.</span><span class="sxs-lookup"><span data-stu-id="69cff-p102">This object represents the default server program. It executes the default RDS data retrieval and update behavior.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69cff-113"><a href="datacontrol-object-rds.md">RDS. DataControl</a></span><span class="sxs-lookup"><span data-stu-id="69cff-113"><a href="datacontrol-object-rds.md">RDS.DataControl</a></span></span></p></td>
<td><p><span data-ttu-id="69cff-114">Este objeto puede invocar automáticamente los objetos <strong>RDS.DataSpace</strong> y <strong>RDSServer.DataFactory</strong>.
</span><span class="sxs-lookup"><span data-stu-id="69cff-114">This object can automatically invoke the <strong>RDS.DataSpace</strong> and <strong>RDSServer.DataFactory</strong> objects.</span></span> <span data-ttu-id="69cff-115">Utilice este objeto para invocar el comportamiento predeterminado de recuperación y actualización de datos de RDS.</span><span class="sxs-lookup"><span data-stu-id="69cff-115">Use this object to invoke the default RDS data retrieval or update behavior.</span></span> <span data-ttu-id="69cff-116">Este objeto también permite a los controles visuales obtener acceso al objeto <strong>Recordset</strong> devuelto.</span><span class="sxs-lookup"><span data-stu-id="69cff-116">This object also provides the means for visual controls to access the returned <strong>Recordset</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>
