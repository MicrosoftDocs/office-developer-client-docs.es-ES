---
title: InheritTypeEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: InheritTypeEnum
ms:assetid: aa505c66-5871-10a8-35a7-cb30bb5dc21a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249787(v=office.15)
ms:contentKeyID: 48546944
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: bf7d7ceac1e4822344ce4f7ad8a05e09c0429dff
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860570"
---
# <a name="inherittypeenum"></a><span data-ttu-id="b68ba-102">InheritTypeEnum</span><span class="sxs-lookup"><span data-stu-id="b68ba-102">InheritTypeEnum</span></span>

<span data-ttu-id="b68ba-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b68ba-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b68ba-104">Especifica cómo heredan permisos establecidos con [SetPermissions](setpermissions-method-adox.md) los objetos.</span><span class="sxs-lookup"><span data-stu-id="b68ba-104">Specifies how objects will inherit permissions set with [SetPermissions](setpermissions-method-adox.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b68ba-105">Constante</span><span class="sxs-lookup"><span data-stu-id="b68ba-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="b68ba-106">Valor</span><span class="sxs-lookup"><span data-stu-id="b68ba-106">Value</span></span></p></th>
<th><p><span data-ttu-id="b68ba-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="b68ba-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b68ba-108"><strong>adInheritBoth</strong></span><span class="sxs-lookup"><span data-stu-id="b68ba-108"><strong>adInheritBoth</strong></span></span></p></td>
<td><p><span data-ttu-id="b68ba-109">3</span><span class="sxs-lookup"><span data-stu-id="b68ba-109">3</span></span></p></td>
<td><p><span data-ttu-id="b68ba-110">Los objetos y otros contenedores contenidos en el objeto principal heredan la entrada.</span><span class="sxs-lookup"><span data-stu-id="b68ba-110">Both objects and other containers contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b68ba-111"><strong>adInheritContainers</strong></span><span class="sxs-lookup"><span data-stu-id="b68ba-111"><strong>adInheritContainers</strong></span></span></p></td>
<td><p><span data-ttu-id="b68ba-112">2</span><span class="sxs-lookup"><span data-stu-id="b68ba-112">2</span></span></p></td>
<td><p><span data-ttu-id="b68ba-113">Otros contenedores que están contenidos en el objeto principal heredan la entrada.</span><span class="sxs-lookup"><span data-stu-id="b68ba-113">Other containers that are contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b68ba-114"><strong>adInheritNone</strong></span><span class="sxs-lookup"><span data-stu-id="b68ba-114"><strong>adInheritNone</strong></span></span></p></td>
<td><p><span data-ttu-id="b68ba-115">0</span><span class="sxs-lookup"><span data-stu-id="b68ba-115">0</span></span></p></td>
<td><p><span data-ttu-id="b68ba-p101">Valor predeterminado.

No se produce ninguna herencia.</span><span class="sxs-lookup"><span data-stu-id="b68ba-p101">Default. No inheritance occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b68ba-118"><strong>adInheritNoPropagate</strong></span><span class="sxs-lookup"><span data-stu-id="b68ba-118"><strong>adInheritNoPropagate</strong></span></span></p></td>
<td><p><span data-ttu-id="b68ba-119">4</span><span class="sxs-lookup"><span data-stu-id="b68ba-119">4</span></span></p></td>
<td><p><span data-ttu-id="b68ba-120">Las marcas <strong>adInheritObjects</strong> y <strong>adInheritContainers</strong> no se propagan a una entrada heredada.</span><span class="sxs-lookup"><span data-stu-id="b68ba-120">The <strong>adInheritObjects</strong> and <strong>adInheritContainers</strong> flags are not propagated to an inherited entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b68ba-121"><strong>marcas adInheritObjects</strong></span><span class="sxs-lookup"><span data-stu-id="b68ba-121"><strong>adInheritObjects</strong></span></span></p></td>
<td><p><span data-ttu-id="b68ba-122">1</span><span class="sxs-lookup"><span data-stu-id="b68ba-122">1</span></span></p></td>
<td><p><span data-ttu-id="b68ba-123">Los objetos que nos son contenedores y están incluidos en el contenedor heredan los permisos.</span><span class="sxs-lookup"><span data-stu-id="b68ba-123">Non-container objects in the container inherit the permissions.</span></span></p></td>
</tr>
</tbody>
</table>

