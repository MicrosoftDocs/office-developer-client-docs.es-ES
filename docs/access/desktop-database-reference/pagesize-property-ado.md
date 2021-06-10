---
title: Propiedad PageSize (ADO)
TOCTitle: PageSize property (ADO)
ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15)
ms:contentKeyID: 48548079
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9365acb13820f898c053d4c90fc252bfd3b228c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288136"
---
# <a name="pagesize-property-ado"></a><span data-ttu-id="81c9c-102">Propiedad PageSize (ADO)</span><span class="sxs-lookup"><span data-stu-id="81c9c-102">PageSize property (ADO)</span></span>


<span data-ttu-id="81c9c-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="81c9c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="81c9c-104">Indica cuántos registros constituyen una página en el objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="81c9c-104">Indicates how many records constitute one page in the [Recordset](recordset-object-ado.md).</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="81c9c-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="81c9c-105">Settings and return values</span></span>

<span data-ttu-id="81c9c-p101">Establece o devuelve un valor de tipo **Long** que indica cuántos registros hay en una página. El valor predeterminado es 10.</span><span class="sxs-lookup"><span data-stu-id="81c9c-p101">Sets or returns a **Long** value that indicates how many records are on a page. The default is 10.</span></span>

## <a name="remarks"></a><span data-ttu-id="81c9c-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="81c9c-108">Remarks</span></span>

<span data-ttu-id="81c9c-109">Use la propiedad **PageSize** para determinar cuántos registros componen una página lógica de datos.</span><span class="sxs-lookup"><span data-stu-id="81c9c-109">Use the **PageSize** property to determine how many records make up a logical page of data.</span></span> <span data-ttu-id="81c9c-110">El establecimiento de un tamaño de página permite utilizar la propiedad [AbsolutePage](absolutepage-property-ado.md) para moverse al primer registro de una página determinada.</span><span class="sxs-lookup"><span data-stu-id="81c9c-110">Establishing a page size allows you to use the [AbsolutePage](absolutepage-property-ado.md) property to move to the first record of a particular page.</span></span> <span data-ttu-id="81c9c-111">Esto resulta útil en escenarios de servidor web cuando se desea permitir que el usuario pueda paginar los datos y ver un número determinado de registros a la vez.</span><span class="sxs-lookup"><span data-stu-id="81c9c-111">This is useful in web server scenarios when you want to allow the user to page through data, viewing a certain number of records at a time.</span></span>

<span data-ttu-id="81c9c-112">Esta propiedad se puede establecer en cualquier momento y su valor se utilizará para calcular la ubicación del primer registro de una página determinada.</span><span class="sxs-lookup"><span data-stu-id="81c9c-112">This property can be set at any time, and its value will be used for calculating the location of the first record of a particular page.</span></span>

