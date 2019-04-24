---
title: MaxRecords (propiedad, ADO)
TOCTitle: MaxRecords property (ADO)
ms:assetid: 424b2d41-073a-3fbe-30aa-99fac94f9a81
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249195(v=office.15)
ms:contentKeyID: 48544475
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8ed643ca3b1341d7f933901e15c20c84acb025f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289724"
---
# <a name="maxrecords-property-ado"></a><span data-ttu-id="2956e-102">MaxRecords (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="2956e-102">MaxRecords property (ADO)</span></span>


<span data-ttu-id="2956e-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2956e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2956e-104">Indica el número máximo de registros que se va a devolver a un objeto [Recordset](recordset-object-ado.md) desde una consulta.</span><span class="sxs-lookup"><span data-stu-id="2956e-104">Indicates the maximum number of records to return to a [Recordset](recordset-object-ado.md) from a query.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="2956e-105">Valores de configuración y devueltos</span><span class="sxs-lookup"><span data-stu-id="2956e-105">Settings and return values</span></span>

<span data-ttu-id="2956e-106">Establece o devuelve un valor de tipo **Long** que indica el número máximo de registros que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="2956e-106">Sets or returns a **Long** value that indicates the maximum number of records to return.</span></span> <span data-ttu-id="2956e-107">El valor predeterminado es cero (sin límite).</span><span class="sxs-lookup"><span data-stu-id="2956e-107">Default is zero (no limit).</span></span>

## <a name="remarks"></a><span data-ttu-id="2956e-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2956e-108">Remarks</span></span>

<span data-ttu-id="2956e-p102">Use la propiedad **MaxRecords** para limitar el número de registros que devuelve el proveedor desde el origen de datos. El valor predeterminado de esta propiedad es cero, lo que significa que el proveedor devuelve todos los registros solicitados.</span><span class="sxs-lookup"><span data-stu-id="2956e-p102">Use the **MaxRecords** property to limit the number of records that the provider returns from the data source. The default setting of this property is zero, which means the provider returns all requested records.</span></span>

<span data-ttu-id="2956e-111">La propiedad **MaxRecords** es de lectura y escritura cuando el objeto **Recordset** está cerrado, y es de solo lectura cuando está abierto.</span><span class="sxs-lookup"><span data-stu-id="2956e-111">The **MaxRecords** property is read/write when the **Recordset** is closed and read-only when it is open.</span></span>

