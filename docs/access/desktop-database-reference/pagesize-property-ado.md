---
title: PageSize (propiedad, ADO)
TOCTitle: PageSize Property (ADO)
ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15)
ms:contentKeyID: 48548079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 89b28e382f1597ff6466aa323565eaf2ff068605
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483728"
---
# <a name="pagesize-property-ado"></a><span data-ttu-id="56615-102">PageSize (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="56615-102">PageSize Property (ADO)</span></span>


<span data-ttu-id="56615-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="56615-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="56615-104">Indica cuántos registros constituyen una página en el objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="56615-104">Indicates how many records constitute one page in the [Recordset](recordset-object-ado.md).</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="56615-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="56615-105">Settings and Return Values</span></span>

<span data-ttu-id="56615-p101">Establece o devuelve un valor de tipo **Long** que indica cuántos registros hay en una página. El valor predeterminado es 10.</span><span class="sxs-lookup"><span data-stu-id="56615-p101">Sets or returns a **Long** value that indicates how many records are on a page. The default is 10.</span></span>

## <a name="remarks"></a><span data-ttu-id="56615-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="56615-108">Remarks</span></span>

<span data-ttu-id="56615-p102">Use la propiedad **PageSize** para determinar cuántos registros componen una página lógica de datos. El establecimiento de un tamaño de página permite utilizar la propiedad [AbsolutePage](absolutepage-property-ado.md) para moverse al primer registro de una página determinada. Esto es útil en escenarios de servidor web cuando se desea permitir al usuario que se desplace por los datos de las páginas para ver un número determinado de registros a la vez.</span><span class="sxs-lookup"><span data-stu-id="56615-p102">Use the **PageSize** property to determine how many records make up a logical page of data. Establishing a page size allows you to use the [AbsolutePage](absolutepage-property-ado.md) property to move to the first record of a particular page. This is useful in Web server scenarios when you want to allow the user to page through data, viewing a certain number of records at a time.</span></span>

<span data-ttu-id="56615-112">Esta propiedad se puede establecer en cualquier momento y su valor se utilizará para calcular la ubicación del primer registro de una página determinada.</span><span class="sxs-lookup"><span data-stu-id="56615-112">This property can be set at any time, and its value will be used for calculating the location of the first record of a particular page.</span></span>

