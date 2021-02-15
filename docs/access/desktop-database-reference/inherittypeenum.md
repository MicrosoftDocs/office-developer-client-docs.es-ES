---
title: InheritTypeEnum (referencia de base de datos de escritorio de Access)
TOCTitle: InheritTypeEnum
ms:assetid: aa505c66-5871-10a8-35a7-cb30bb5dc21a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249787(v=office.15)
ms:contentKeyID: 48546944
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ba1a78e49d44bce0c489e4f5259ec9699543e231
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291417"
---
# <a name="inherittypeenum"></a><span data-ttu-id="cadc8-102">InheritTypeEnum</span><span class="sxs-lookup"><span data-stu-id="cadc8-102">InheritTypeEnum</span></span>

<span data-ttu-id="cadc8-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cadc8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cadc8-104">Especifica cómo heredan permisos establecidos con [SetPermissions](setpermissions-method-adox.md) los objetos.</span><span class="sxs-lookup"><span data-stu-id="cadc8-104">Specifies how objects will inherit permissions set with [SetPermissions](setpermissions-method-adox.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cadc8-105">Constante</span><span class="sxs-lookup"><span data-stu-id="cadc8-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="cadc8-106">Valor</span><span class="sxs-lookup"><span data-stu-id="cadc8-106">Value</span></span></p></th>
<th><p><span data-ttu-id="cadc8-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="cadc8-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cadc8-108"><strong>adInheritBoth</strong></span><span class="sxs-lookup"><span data-stu-id="cadc8-108"><strong>adInheritBoth</strong></span></span></p></td>
<td><p><span data-ttu-id="cadc8-109">3 </span><span class="sxs-lookup"><span data-stu-id="cadc8-109">3</span></span></p></td>
<td><p><span data-ttu-id="cadc8-110">Los objetos y otros contenedores contenidos en el objeto principal heredan la entrada.</span><span class="sxs-lookup"><span data-stu-id="cadc8-110">Both objects and other containers contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cadc8-111"><strong>adInheritContainers</strong></span><span class="sxs-lookup"><span data-stu-id="cadc8-111"><strong>adInheritContainers</strong></span></span></p></td>
<td><p><span data-ttu-id="cadc8-112">2 </span><span class="sxs-lookup"><span data-stu-id="cadc8-112">2</span></span></p></td>
<td><p><span data-ttu-id="cadc8-113">Otros contenedores que están contenidos en el objeto principal heredan la entrada.</span><span class="sxs-lookup"><span data-stu-id="cadc8-113">Other containers that are contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cadc8-114"><strong>adInheritNone</strong></span><span class="sxs-lookup"><span data-stu-id="cadc8-114"><strong>adInheritNone</strong></span></span></p></td>
<td><p><span data-ttu-id="cadc8-115">0</span><span class="sxs-lookup"><span data-stu-id="cadc8-115">0</span></span></p></td>
<td><p><span data-ttu-id="cadc8-p101">Valor predeterminado.

No se produce ninguna herencia.</span><span class="sxs-lookup"><span data-stu-id="cadc8-p101">Default. No inheritance occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cadc8-118"><strong>adInheritNoPropcoherencia</strong></span><span class="sxs-lookup"><span data-stu-id="cadc8-118"><strong>adInheritNoPropagate</strong></span></span></p></td>
<td><p><span data-ttu-id="cadc8-119">4 </span><span class="sxs-lookup"><span data-stu-id="cadc8-119">4</span></span></p></td>
<td><p><span data-ttu-id="cadc8-120">Las marcas <strong>adInheritObjects</strong> y <strong>adInheritContainers</strong> no se propagan a una entrada heredada.</span><span class="sxs-lookup"><span data-stu-id="cadc8-120">The <strong>adInheritObjects</strong> and <strong>adInheritContainers</strong> flags are not propagated to an inherited entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cadc8-121"><strong>adInheritObjects</strong></span><span class="sxs-lookup"><span data-stu-id="cadc8-121"><strong>adInheritObjects</strong></span></span></p></td>
<td><p><span data-ttu-id="cadc8-122">1 </span><span class="sxs-lookup"><span data-stu-id="cadc8-122">1</span></span></p></td>
<td><p><span data-ttu-id="cadc8-123">Los objetos que nos son contenedores y están incluidos en el contenedor heredan los permisos.</span><span class="sxs-lookup"><span data-stu-id="cadc8-123">Non-container objects in the container inherit the permissions.</span></span></p></td>
</tr>
</tbody>
</table>

