---
title: DrilledDown (propiedad, ADO MD)
TOCTitle: DrilledDown Property (ADO MD)
ms:assetid: 1dfe728f-8da2-1d2b-7361-8689a0b088b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248972(v=office.15)
ms:contentKeyID: 48543610
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f7e53eb2a6d1735e07fa73e38adad8a59522fddf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871503"
---
# <a name="drilleddown-property-ado-md"></a><span data-ttu-id="ecdf2-102">DrilledDown (propiedad, ADO MD)</span><span class="sxs-lookup"><span data-stu-id="ecdf2-102">DrilledDown Property (ADO MD)</span></span>


<span data-ttu-id="ecdf2-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ecdf2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ecdf2-104">Indica si no hay ningún elemento secundario que siga inmediatamente al elemento en el eje.</span><span class="sxs-lookup"><span data-stu-id="ecdf2-104">Indicates whether no children immediately follow the member on the axis.</span></span>

## <a name="return-values"></a><span data-ttu-id="ecdf2-105">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="ecdf2-105">Return values</span></span>

<span data-ttu-id="ecdf2-p101">Devuelve un valor **Boolean** y es de solo lectura. **DrilledDown** devuelve **True** si no hay ningún elemento secundario del elemento activo en el eje. **DrilledDown** devuelve **False** si hay al menos un elemento secundario del elemento activo en el eje.</span><span class="sxs-lookup"><span data-stu-id="ecdf2-p101">Returns a **Boolean** value and is read-only. **DrilledDown** returns **True** if there are no child members of the current member on the axis. **DrilledDown** returns **False** if there is one or more child members of the current member on the axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecdf2-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ecdf2-109">Remarks</span></span>

<span data-ttu-id="ecdf2-p102">Utilice la propiedad **DrilledDown** para determinar si hay al menos un elemento secundario de este elemento en el eje que siga inmediatamente a este elemento. Esta información es útil cuando se muestra el elemento.</span><span class="sxs-lookup"><span data-stu-id="ecdf2-p102">Use the **DrilledDown** property to determine whether there is at least one child of this member on the axis immediately following this member. This information is useful when displaying the member.</span></span>

<span data-ttu-id="ecdf2-p103">Esta propiedad sólo es compatible con objetos [Member](member-object-ado-md.md) pertenecientes a un objeto [Position](position-object-ado-md.md). Si se hace referencia a esta propiedad desde objetos **Member** pertenecientes a un objeto [Level](level-object-ado-md.md), se produce un error.</span><span class="sxs-lookup"><span data-stu-id="ecdf2-p103">This property is only supported on [Member](member-object-ado-md.md) objects belonging to a [Position](position-object-ado-md.md) object. An error occurs when this property is referenced from **Member** objects belonging to a [Level](level-object-ado-md.md) object.</span></span>

