---
title: Propiedad DrilledDown (ADO MD)
TOCTitle: DrilledDown property (ADO MD)
ms:assetid: 1dfe728f-8da2-1d2b-7361-8689a0b088b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248972(v=office.15)
ms:contentKeyID: 48543610
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 40a97c7f755f681169c77c3a2077ee41d9cdc980
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293689"
---
# <a name="drilleddown-property-ado-md"></a><span data-ttu-id="cd9f9-102">Propiedad DrilledDown (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="cd9f9-102">DrilledDown property (ADO MD)</span></span>


<span data-ttu-id="cd9f9-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cd9f9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cd9f9-104">Indica si no hay ningún elemento secundario que siga inmediatamente al elemento en el eje.</span><span class="sxs-lookup"><span data-stu-id="cd9f9-104">Indicates whether no children immediately follow the member on the axis.</span></span>

## <a name="return-values"></a><span data-ttu-id="cd9f9-105">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="cd9f9-105">Return values</span></span>

<span data-ttu-id="cd9f9-p101">Devuelve un valor **Boolean** y es de solo lectura. **DrilledDown** devuelve **True** si no hay ningún elemento secundario del elemento activo en el eje. **DrilledDown** devuelve **False** si hay al menos un elemento secundario del elemento activo en el eje.</span><span class="sxs-lookup"><span data-stu-id="cd9f9-p101">Returns a **Boolean** value and is read-only. **DrilledDown** returns **True** if there are no child members of the current member on the axis. **DrilledDown** returns **False** if there is one or more child members of the current member on the axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd9f9-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cd9f9-109">Remarks</span></span>

<span data-ttu-id="cd9f9-p102">Utilice la propiedad **DrilledDown** para determinar si hay al menos un elemento secundario de este elemento en el eje que siga inmediatamente a este elemento. Esta información es útil cuando se muestra el elemento.</span><span class="sxs-lookup"><span data-stu-id="cd9f9-p102">Use the **DrilledDown** property to determine whether there is at least one child of this member on the axis immediately following this member. This information is useful when displaying the member.</span></span>

<span data-ttu-id="cd9f9-p103">Esta propiedad sólo es compatible con objetos [Member](member-object-ado-md.md) pertenecientes a un objeto [Position](position-object-ado-md.md). Si se hace referencia a esta propiedad desde objetos **Member** pertenecientes a un objeto [Level](level-object-ado-md.md), se produce un error.</span><span class="sxs-lookup"><span data-stu-id="cd9f9-p103">This property is only supported on [Member](member-object-ado-md.md) objects belonging to a [Position](position-object-ado-md.md) object. An error occurs when this property is referenced from **Member** objects belonging to a [Level](level-object-ado-md.md) object.</span></span>

