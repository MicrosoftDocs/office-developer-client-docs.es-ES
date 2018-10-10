---
title: UpdateTypeEnum Enumeration (DAO)
TOCTitle: UpdateTypeEnum Enumeration
ms:assetid: 7ac38bae-27fc-f3d0-5b75-569bce547954
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196186(v=office.15)
ms:contentKeyID: 48545800
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4ee8638d6fdade7e6955613964f619270574ce4b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484565"
---
# <a name="updatetypeenum-enumeration-dao"></a><span data-ttu-id="fb48b-102">UpdateTypeEnum Enumeration (DAO)</span><span class="sxs-lookup"><span data-stu-id="fb48b-102">UpdateTypeEnum Enumeration (DAO)</span></span>


<span data-ttu-id="fb48b-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="fb48b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fb48b-104">Se utiliza con el método **Update** para especificar qué actualizaciones se han de escribir en el disco.</span><span class="sxs-lookup"><span data-stu-id="fb48b-104">Used with the **Update** method to specify which updates to write to disk.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fb48b-105">Nombre</span><span class="sxs-lookup"><span data-stu-id="fb48b-105">Name</span></span></p></th>
<th><p><span data-ttu-id="fb48b-106">Valor</span><span class="sxs-lookup"><span data-stu-id="fb48b-106">Value</span></span></p></th>
<th><p><span data-ttu-id="fb48b-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb48b-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fb48b-108">dbUpdateBatch</span><span class="sxs-lookup"><span data-stu-id="fb48b-108">dbUpdateBatch</span></span></p></td>
<td><p><span data-ttu-id="fb48b-109">4</span><span class="sxs-lookup"><span data-stu-id="fb48b-109">4</span></span></p></td>
<td><p><span data-ttu-id="fb48b-110">Todos los cambios pendientes de la caché de actualizaciones se escriben en el disco.</span><span class="sxs-lookup"><span data-stu-id="fb48b-110">All pending changes in the update cache are written to disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb48b-111">dbUpdateCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="fb48b-111">dbUpdateCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="fb48b-112">2</span><span class="sxs-lookup"><span data-stu-id="fb48b-112">2</span></span></p></td>
<td><p><span data-ttu-id="fb48b-113">Sólo los cambios pendientes del registro actual se escriben en el disco.</span><span class="sxs-lookup"><span data-stu-id="fb48b-113">Only the current record's pending changes are written to disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb48b-114">valores dbUpdateRegular</span><span class="sxs-lookup"><span data-stu-id="fb48b-114">dbUpdateRegular</span></span></p></td>
<td><p><span data-ttu-id="fb48b-115">1</span><span class="sxs-lookup"><span data-stu-id="fb48b-115">1</span></span></p></td>
<td><p><span data-ttu-id="fb48b-116">(Valor predeterminado) Los cambios pendientes no se almacenan en caché y se escriben en el disco inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="fb48b-116">(Default) Pending changes are not cached and are written to disk immediately.</span></span></p></td>
</tr>
</tbody>
</table>

