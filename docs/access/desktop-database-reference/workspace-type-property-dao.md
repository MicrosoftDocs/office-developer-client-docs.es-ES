---
title: Propiedad Workspace.Type (DAO)
TOCTitle: Type Property
ms:assetid: 89e59280-d2cd-b6a2-16c5-9f14f42fdd99
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197086(v=office.15)
ms:contentKeyID: 48546177
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e698963d60809e8d88c4ff87532fb7b74cff275c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311308"
---
# <a name="workspacetype-property-dao"></a><span data-ttu-id="dc1fd-102">Propiedad Workspace.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="dc1fd-102">Workspace.Type property (DAO)</span></span>


<span data-ttu-id="dc1fd-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dc1fd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dc1fd-104">Establece o devuelve un valor que indica el tipo operativo o el tipo de datos de un objeto.</span><span class="sxs-lookup"><span data-stu-id="dc1fd-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="dc1fd-105">**Integer** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="dc1fd-105">Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc1fd-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc1fd-106">Syntax</span></span>

<span data-ttu-id="dc1fd-107">*expression* .Type</span><span class="sxs-lookup"><span data-stu-id="dc1fd-107">*expression* .Type</span></span>

<span data-ttu-id="dc1fd-108">*expression* Variable que representa un objeto **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="dc1fd-108">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc1fd-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dc1fd-109">Remarks</span></span>

<span data-ttu-id="dc1fd-110">Para un objeto **Workspace**, los posibles valores de configuración y devueltos son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="dc1fd-110">For a **Workspace** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dc1fd-111">Constante</span><span class="sxs-lookup"><span data-stu-id="dc1fd-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="dc1fd-112">Tipo de área de trabajo</span><span class="sxs-lookup"><span data-stu-id="dc1fd-112">Workspace type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc1fd-113"><strong>dbUseJet</strong></span><span class="sxs-lookup"><span data-stu-id="dc1fd-113"><strong>dbUseJet</strong></span></span></p></td>
<td><p><span data-ttu-id="dc1fd-114">El objeto <strong>Workspace</strong> está conectado al motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="dc1fd-114">The <strong>Workspace</strong> is connected to the Microsoft Access database engine.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc1fd-115"><strong>dbUseODBC</strong></span><span class="sxs-lookup"><span data-stu-id="dc1fd-115"><strong>dbUseODBC</strong></span></span></p></td>
<td><p><span data-ttu-id="dc1fd-116">El objeto <strong>Workspace</strong> está conectado a un origen de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="dc1fd-116">The <strong>Workspace</strong> is connected to an ODBC data source.</span></span></p></td>
</tr>
</tbody>
</table>

