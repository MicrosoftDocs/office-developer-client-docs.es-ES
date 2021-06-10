---
title: Propiedad Recordset2.Type (DAO)
TOCTitle: Type Property
ms:assetid: 9bec543e-7f59-ea59-dc79-41d0e08b5ab6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198080(v=office.15)
ms:contentKeyID: 48546583
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052880
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 6646658daf482373ef8b62f6d3420b1d11152cac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307178"
---
# <a name="recordset2type-property-dao"></a><span data-ttu-id="a283e-102">Propiedad Recordset2.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="a283e-102">Recordset2.Type property (DAO)</span></span>


<span data-ttu-id="a283e-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a283e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a283e-p101">Establece o devuelve un valor que indica el tipo operativo o el tipo de datos de un objeto. **Integer** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="a283e-p101">Sets or returns a value that indicates the operational type or data type of an object. Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a283e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a283e-106">Syntax</span></span>

<span data-ttu-id="a283e-107">*expression* .Type</span><span class="sxs-lookup"><span data-stu-id="a283e-107">*expression* .Type</span></span>

<span data-ttu-id="a283e-108">*expresión* Variable que representa un **objeto Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="a283e-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a283e-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a283e-109">Remarks</span></span>

<span data-ttu-id="a283e-110">Para un objeto **Recordset**, los valores posibles y valores devueltos son los que se muestran a continuación.</span><span class="sxs-lookup"><span data-stu-id="a283e-110">For a **Recordset** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a283e-111">Constante</span><span class="sxs-lookup"><span data-stu-id="a283e-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="a283e-112">Tipo Recordset</span><span class="sxs-lookup"><span data-stu-id="a283e-112">Recordset type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a283e-113"><strong>dbOpenTable</strong></span><span class="sxs-lookup"><span data-stu-id="a283e-113"><strong>dbOpenTable</strong></span></span></p></td>
<td><p><span data-ttu-id="a283e-114">Tabla (sólo para áreas de trabajo de Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="a283e-114">Table (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a283e-115"><strong>dbOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="a283e-115"><strong>dbOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="a283e-116">Dinámico (sólo áreas de trabajo de ODBCDirect)</span><span class="sxs-lookup"><span data-stu-id="a283e-116">Dynamic (ODBCDirect workspaces only)</span></span></p>
<p><span data-ttu-id="a283e-117"><strong>NOTA</strong>: las áreas de trabajo de ODBCDirect no se admiten en Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="a283e-117"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="a283e-118">Use ADO si desea obtener acceso a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="a283e-118">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a283e-119"><strong>dbOpenDynaset</strong></span><span class="sxs-lookup"><span data-stu-id="a283e-119"><strong>dbOpenDynaset</strong></span></span></p></td>
<td><p><span data-ttu-id="a283e-120">Dynaset</span><span class="sxs-lookup"><span data-stu-id="a283e-120">Dynaset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a283e-121"><strong>dbOpenSnapshot</strong></span><span class="sxs-lookup"><span data-stu-id="a283e-121"><strong>dbOpenSnapshot</strong></span></span></p></td>
<td><p><span data-ttu-id="a283e-122">Instantánea</span><span class="sxs-lookup"><span data-stu-id="a283e-122">Snapshot</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a283e-123"><strong>dbOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="a283e-123"><strong>dbOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="a283e-124">Solo avance</span><span class="sxs-lookup"><span data-stu-id="a283e-124">Forward-only</span></span></p></td>
</tr>
</tbody>
</table>

