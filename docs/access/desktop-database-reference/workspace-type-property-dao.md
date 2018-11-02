---
title: Propiedad Workspace.Type (DAO)
TOCTitle: Type Property
ms:assetid: 89e59280-d2cd-b6a2-16c5-9f14f42fdd99
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197086(v=office.15)
ms:contentKeyID: 48546177
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6c715da6ec535d90397b49e47be6ca76a72e5685
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926776"
---
# <a name="workspacetype-property-dao"></a><span data-ttu-id="0844a-102">Propiedad Workspace.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="0844a-102">Workspace.Type property (DAO)</span></span>


<span data-ttu-id="0844a-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0844a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0844a-p101">Establece o devuelve un valor que indica el tipo operativo o el tipo de datos de un objeto. **Integer** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="0844a-p101">Sets or returns a value that indicates the operational type or data type of an object. Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0844a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0844a-106">Syntax</span></span>

<span data-ttu-id="0844a-107">*expresión* . Tipo de</span><span class="sxs-lookup"><span data-stu-id="0844a-107">*expression* .Type</span></span>

<span data-ttu-id="0844a-108">*expresión* Variable que representa un objeto **Workspace** .</span><span class="sxs-lookup"><span data-stu-id="0844a-108">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0844a-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0844a-109">Remarks</span></span>

<span data-ttu-id="0844a-110">Para un objeto **Workspace**, los posibles valores de configuración y devueltos son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="0844a-110">For a **Workspace** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0844a-111">Constante</span><span class="sxs-lookup"><span data-stu-id="0844a-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="0844a-112">Tipo de área de trabajo</span><span class="sxs-lookup"><span data-stu-id="0844a-112">Workspace type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0844a-113"><strong>dbUseJet</strong></span><span class="sxs-lookup"><span data-stu-id="0844a-113"><strong>dbUseJet</strong></span></span></p></td>
<td><p><span data-ttu-id="0844a-114">El objeto <strong>Workspace</strong> está conectado al motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="0844a-114">The <strong>Workspace</strong> is connected to the Microsoft Access database engine.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0844a-115"><strong>dbUseODBC</strong></span><span class="sxs-lookup"><span data-stu-id="0844a-115"><strong>dbUseODBC</strong></span></span></p></td>
<td><p><span data-ttu-id="0844a-116">El objeto <strong>Workspace</strong> está conectado a un origen de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="0844a-116">The <strong>Workspace</strong> is connected to an ODBC data source.</span></span></p></td>
</tr>
</tbody>
</table>

