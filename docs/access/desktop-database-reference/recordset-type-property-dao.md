---
title: Propiedad Recordset. Type (DAO)
TOCTitle: Type Property
ms:assetid: d841b088-50bf-16d9-33e0-2140050e1ac6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835080(v=office.15)
ms:contentKeyID: 48548030
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4a55af8aaa5cfb3d87e13125871a6ccbe1e7f2dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307556"
---
# <a name="recordsettype-property-dao"></a><span data-ttu-id="357a3-102">Propiedad Recordset. Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="357a3-102">Recordset.Type property (DAO)</span></span>


<span data-ttu-id="357a3-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="357a3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="357a3-104">Establece o devuelve un valor que indica el tipo operativo o el tipo de datos de un objeto.</span><span class="sxs-lookup"><span data-stu-id="357a3-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="357a3-105">**Integer** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="357a3-105">Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="357a3-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="357a3-106">Syntax</span></span>

<span data-ttu-id="357a3-107">*expresión* . Type</span><span class="sxs-lookup"><span data-stu-id="357a3-107">*expression* .Type</span></span>

<span data-ttu-id="357a3-108">*expresión* Variable que representa un objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="357a3-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="357a3-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="357a3-109">Remarks</span></span>

<span data-ttu-id="357a3-110">Para un objeto **Recordset**, los valores posibles y valores devueltos son los que se muestran a continuación.</span><span class="sxs-lookup"><span data-stu-id="357a3-110">For a **Recordset** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="357a3-111">Constante</span><span class="sxs-lookup"><span data-stu-id="357a3-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="357a3-112">Tipo Recordset</span><span class="sxs-lookup"><span data-stu-id="357a3-112">Recordset type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="357a3-113"><strong>dbOpenTable</strong></span><span class="sxs-lookup"><span data-stu-id="357a3-113"><strong>dbOpenTable</strong></span></span></p></td>
<td><p><span data-ttu-id="357a3-114">Tabla (sólo para áreas de trabajo de Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="357a3-114">Table (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="357a3-115"><strong>dbOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="357a3-115"><strong>dbOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="357a3-116">Dinámico (sólo áreas de trabajo de ODBCDirect)</span><span class="sxs-lookup"><span data-stu-id="357a3-116">Dynamic (ODBCDirect workspaces only)</span></span></p>
<p><span data-ttu-id="357a3-117"><strong>Nota</strong>: no se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="357a3-117"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="357a3-118">Use ADO si desea obtener acceso a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="357a3-118">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="357a3-119"><strong>dbOpenDynaset</strong></span><span class="sxs-lookup"><span data-stu-id="357a3-119"><strong>dbOpenDynaset</strong></span></span></p></td>
<td><p><span data-ttu-id="357a3-120">Dinámico</span><span class="sxs-lookup"><span data-stu-id="357a3-120">Dynaset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="357a3-121"><strong>dbOpenSnapshot</strong></span><span class="sxs-lookup"><span data-stu-id="357a3-121"><strong>dbOpenSnapshot</strong></span></span></p></td>
<td><p><span data-ttu-id="357a3-122">Copias</span><span class="sxs-lookup"><span data-stu-id="357a3-122">Snapshot</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="357a3-123"><strong>dbOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="357a3-123"><strong>dbOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="357a3-124">Solo avance</span><span class="sxs-lookup"><span data-stu-id="357a3-124">Forward-only</span></span></p></td>
</tr>
</tbody>
</table>

