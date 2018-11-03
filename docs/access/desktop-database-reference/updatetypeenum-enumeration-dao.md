---
title: UpdateTypeEnum (enumeración) (DAO)
TOCTitle: UpdateTypeEnum Enumeration
ms:assetid: 7ac38bae-27fc-f3d0-5b75-569bce547954
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196186(v=office.15)
ms:contentKeyID: 48545800
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d38cf4554837c9c6434b7607746f2c40836ac950
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944623"
---
# <a name="updatetypeenum-enumeration-dao"></a><span data-ttu-id="ef8d8-102">UpdateTypeEnum (enumeración) (DAO)</span><span class="sxs-lookup"><span data-stu-id="ef8d8-102">UpdateTypeEnum enumeration (DAO)</span></span>


<span data-ttu-id="ef8d8-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ef8d8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ef8d8-104">Se utiliza con el método **Update** para especificar qué actualizaciones se han de escribir en el disco.</span><span class="sxs-lookup"><span data-stu-id="ef8d8-104">Used with the **Update** method to specify which updates to write to disk.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ef8d8-105">Nombre</span><span class="sxs-lookup"><span data-stu-id="ef8d8-105">Name</span></span></p></th>
<th><p><span data-ttu-id="ef8d8-106">Valor</span><span class="sxs-lookup"><span data-stu-id="ef8d8-106">Value</span></span></p></th>
<th><p><span data-ttu-id="ef8d8-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="ef8d8-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef8d8-108">dbUpdateBatch</span><span class="sxs-lookup"><span data-stu-id="ef8d8-108">dbUpdateBatch</span></span></p></td>
<td><p><span data-ttu-id="ef8d8-109">4</span><span class="sxs-lookup"><span data-stu-id="ef8d8-109">4</span></span></p></td>
<td><p><span data-ttu-id="ef8d8-110">Todos los cambios pendientes de la caché de actualizaciones se escriben en el disco.</span><span class="sxs-lookup"><span data-stu-id="ef8d8-110">All pending changes in the update cache are written to disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef8d8-111">dbUpdateCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="ef8d8-111">dbUpdateCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="ef8d8-112">2</span><span class="sxs-lookup"><span data-stu-id="ef8d8-112">2</span></span></p></td>
<td><p><span data-ttu-id="ef8d8-113">Sólo los cambios pendientes del registro actual se escriben en el disco.</span><span class="sxs-lookup"><span data-stu-id="ef8d8-113">Only the current record's pending changes are written to disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef8d8-114">valores dbUpdateRegular</span><span class="sxs-lookup"><span data-stu-id="ef8d8-114">dbUpdateRegular</span></span></p></td>
<td><p><span data-ttu-id="ef8d8-115">1</span><span class="sxs-lookup"><span data-stu-id="ef8d8-115">1</span></span></p></td>
<td><p><span data-ttu-id="ef8d8-116">(Valor predeterminado) Los cambios pendientes no se almacenan en caché y se escriben en el disco inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="ef8d8-116">(Default) Pending changes are not cached and are written to disk immediately.</span></span></p></td>
</tr>
</tbody>
</table>

