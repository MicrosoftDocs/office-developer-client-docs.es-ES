---
title: InheritTypeEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: InheritTypeEnum
ms:assetid: aa505c66-5871-10a8-35a7-cb30bb5dc21a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249787(v=office.15)
ms:contentKeyID: 48546944
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 031c47aff666bf10f0e2aa597ccd0143ed3d6209
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483849"
---
# <a name="inherittypeenum"></a><span data-ttu-id="406df-102">InheritTypeEnum</span><span class="sxs-lookup"><span data-stu-id="406df-102">InheritTypeEnum</span></span>


<span data-ttu-id="406df-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="406df-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="406df-104">Especifica cómo heredan permisos establecidos con [SetPermissions](setpermissions-method-adox.md) los objetos.</span><span class="sxs-lookup"><span data-stu-id="406df-104">Specifies how objects will inherit permissions set with [SetPermissions](setpermissions-method-adox.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="406df-105">Constante</span><span class="sxs-lookup"><span data-stu-id="406df-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="406df-106">Valor</span><span class="sxs-lookup"><span data-stu-id="406df-106">Value</span></span></p></th>
<th><p><span data-ttu-id="406df-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="406df-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="406df-108"><strong>adInheritBoth</strong></span><span class="sxs-lookup"><span data-stu-id="406df-108"><strong>adInheritBoth</strong></span></span></p></td>
<td><p><span data-ttu-id="406df-109">3</span><span class="sxs-lookup"><span data-stu-id="406df-109">3</span></span></p></td>
<td><p><span data-ttu-id="406df-110">Los objetos y otros contenedores contenidos en el objeto principal heredan la entrada.</span><span class="sxs-lookup"><span data-stu-id="406df-110">Both objects and other containers contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="406df-111"><strong>adInheritContainers</strong></span><span class="sxs-lookup"><span data-stu-id="406df-111"><strong>adInheritContainers</strong></span></span></p></td>
<td><p><span data-ttu-id="406df-112">2</span><span class="sxs-lookup"><span data-stu-id="406df-112">2</span></span></p></td>
<td><p><span data-ttu-id="406df-113">Otros contenedores que están contenidos en el objeto principal heredan la entrada.</span><span class="sxs-lookup"><span data-stu-id="406df-113">Other containers that are contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="406df-114"><strong>adInheritNone</strong></span><span class="sxs-lookup"><span data-stu-id="406df-114"><strong>adInheritNone</strong></span></span></p></td>
<td><p><span data-ttu-id="406df-115">0</span><span class="sxs-lookup"><span data-stu-id="406df-115">0</span></span></p></td>
<td><p><span data-ttu-id="406df-p101">Valor predeterminado.

No se produce ninguna herencia.</span><span class="sxs-lookup"><span data-stu-id="406df-p101">Default. No inheritance occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="406df-118"><strong>adInheritNoPropagate</strong></span><span class="sxs-lookup"><span data-stu-id="406df-118"><strong>adInheritNoPropagate</strong></span></span></p></td>
<td><p><span data-ttu-id="406df-119">4</span><span class="sxs-lookup"><span data-stu-id="406df-119">4</span></span></p></td>
<td><p><span data-ttu-id="406df-120">Las marcas <strong>adInheritObjects</strong> y <strong>adInheritContainers</strong> no se propagan a una entrada heredada.</span><span class="sxs-lookup"><span data-stu-id="406df-120">The <strong>adInheritObjects</strong> and <strong>adInheritContainers</strong> flags are not propagated to an inherited entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="406df-121"><strong>marcas adInheritObjects</strong></span><span class="sxs-lookup"><span data-stu-id="406df-121"><strong>adInheritObjects</strong></span></span></p></td>
<td><p><span data-ttu-id="406df-122">1</span><span class="sxs-lookup"><span data-stu-id="406df-122">1</span></span></p></td>
<td><p><span data-ttu-id="406df-123">Los objetos que nos son contenedores y están incluidos en el contenedor heredan los permisos.</span><span class="sxs-lookup"><span data-stu-id="406df-123">Non-container objects in the container inherit the permissions.</span></span></p></td>
</tr>
</tbody>
</table>

