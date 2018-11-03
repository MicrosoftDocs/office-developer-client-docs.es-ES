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
ms.openlocfilehash: ca75e1b21e017dfbbbc5028d06a4799a9afd50f3
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936598"
---
# <a name="recordset2type-property-dao"></a><span data-ttu-id="bfe5e-102">Propiedad Recordset2.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="bfe5e-102">Recordset2.Type property (DAO)</span></span>


<span data-ttu-id="bfe5e-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bfe5e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bfe5e-p101">Establece o devuelve un valor que indica el tipo operativo o el tipo de datos de un objeto. **Integer** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="bfe5e-p101">Sets or returns a value that indicates the operational type or data type of an object. Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfe5e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bfe5e-106">Syntax</span></span>

<span data-ttu-id="bfe5e-107">*expresión* . Tipo de</span><span class="sxs-lookup"><span data-stu-id="bfe5e-107">*expression* .Type</span></span>

<span data-ttu-id="bfe5e-108">*expresión* Variable que representa un objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="bfe5e-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfe5e-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bfe5e-109">Remarks</span></span>

<span data-ttu-id="bfe5e-110">Para un objeto **Recordset**, los valores posibles y valores devueltos son los que se muestran a continuación.</span><span class="sxs-lookup"><span data-stu-id="bfe5e-110">For a **Recordset** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bfe5e-111">Constante</span><span class="sxs-lookup"><span data-stu-id="bfe5e-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="bfe5e-112">Tipo Recordset</span><span class="sxs-lookup"><span data-stu-id="bfe5e-112">Recordset type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bfe5e-113"><strong>dbOpenTable</strong></span><span class="sxs-lookup"><span data-stu-id="bfe5e-113"><strong>dbOpenTable</strong></span></span></p></td>
<td><p><span data-ttu-id="bfe5e-114">Tabla (sólo para áreas de trabajo de Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="bfe5e-114">Table (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfe5e-115"><strong>dbOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="bfe5e-115"><strong>dbOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="bfe5e-116">Dinámico (sólo áreas de trabajo de ODBCDirect)</span><span class="sxs-lookup"><span data-stu-id="bfe5e-116">Dynamic (ODBCDirect workspaces only)</span></span></p>
<p><span data-ttu-id="bfe5e-117"><strong>Nota</strong>: las áreas de trabajo de ODBCDirect no son compatibles con Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="bfe5e-117"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="bfe5e-118">Use ADO si desea obtener acceso a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="bfe5e-118">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bfe5e-119"><strong>dbOpenDynaset</strong></span><span class="sxs-lookup"><span data-stu-id="bfe5e-119"><strong>dbOpenDynaset</strong></span></span></p></td>
<td><p><span data-ttu-id="bfe5e-120">Dynaset</span><span class="sxs-lookup"><span data-stu-id="bfe5e-120">Dynaset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfe5e-121"><strong>dbOpenSnapshot</strong></span><span class="sxs-lookup"><span data-stu-id="bfe5e-121"><strong>dbOpenSnapshot</strong></span></span></p></td>
<td><p><span data-ttu-id="bfe5e-122">Snapshot</span><span class="sxs-lookup"><span data-stu-id="bfe5e-122">Snapshot</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bfe5e-123"><strong>dbOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="bfe5e-123"><strong>dbOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="bfe5e-124">Forward-only</span><span class="sxs-lookup"><span data-stu-id="bfe5e-124">Forward-only</span></span></p></td>
</tr>
</tbody>
</table>

