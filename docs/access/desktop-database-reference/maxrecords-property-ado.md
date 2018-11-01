---
title: MaxRecords (propiedad, ADO)
TOCTitle: MaxRecords property (ADO)
ms:assetid: 424b2d41-073a-3fbe-30aa-99fac94f9a81
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249195(v=office.15)
ms:contentKeyID: 48544475
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7d66a26cffb14220670643c5b6b5aafe94e8fcb5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870089"
---
# <a name="maxrecords-property-ado"></a><span data-ttu-id="7a39a-102">MaxRecords (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="7a39a-102">MaxRecords property (ADO)</span></span>


<span data-ttu-id="7a39a-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7a39a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7a39a-104">Indica el número máximo de registros que se va a devolver a un objeto [Recordset](recordset-object-ado.md) desde una consulta.</span><span class="sxs-lookup"><span data-stu-id="7a39a-104">Indicates the maximum number of records to return to a [Recordset](recordset-object-ado.md) from a query.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="7a39a-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="7a39a-105">Settings and return values</span></span>

<span data-ttu-id="7a39a-p101">Establece o devuelve un valor de tipo **Long** que indica el número máximo de registros que se va a devolver. El valor predeterminado es cero (sin límite).</span><span class="sxs-lookup"><span data-stu-id="7a39a-p101">Sets or returns a **Long** value that indicates the maximum number of records to return. Default is zero (no limit).</span></span>

## <a name="remarks"></a><span data-ttu-id="7a39a-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7a39a-108">Remarks</span></span>

<span data-ttu-id="7a39a-p102">Use la propiedad **MaxRecords** para limitar el número de registros que devuelve el proveedor desde el origen de datos. El valor predeterminado de esta propiedad es cero, lo que significa que el proveedor devuelve todos los registros solicitados.</span><span class="sxs-lookup"><span data-stu-id="7a39a-p102">Use the **MaxRecords** property to limit the number of records that the provider returns from the data source. The default setting of this property is zero, which means the provider returns all requested records.</span></span>

<span data-ttu-id="7a39a-111">La propiedad **MaxRecords** es de lectura y escritura cuando el objeto **Recordset** está cerrado, y es de solo lectura cuando está abierto.</span><span class="sxs-lookup"><span data-stu-id="7a39a-111">The **MaxRecords** property is read/write when the **Recordset** is closed and read-only when it is open.</span></span>

