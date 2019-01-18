---
title: ActionEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: ActionEnum
ms:assetid: 225024c1-9088-b532-2a23-04c1aaaaa892
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248998(v=office.15)
ms:contentKeyID: 48543704
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f098adb42df39d1509a6d22decd8d2cead684f11
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702433"
---
# <a name="actionenum"></a><span data-ttu-id="6b78d-102">ActionEnum</span><span class="sxs-lookup"><span data-stu-id="6b78d-102">ActionEnum</span></span>

<span data-ttu-id="6b78d-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6b78d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6b78d-104">Especifica el tipo de acción que se debe realizar cuando se llama a [SetPermissions](setpermissions-method-adox.md).</span><span class="sxs-lookup"><span data-stu-id="6b78d-104">Specifies the type of action to be performed when [SetPermissions](setpermissions-method-adox.md) is called.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6b78d-105">Constante</span><span class="sxs-lookup"><span data-stu-id="6b78d-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="6b78d-106">Valor</span><span class="sxs-lookup"><span data-stu-id="6b78d-106">Value</span></span></p></th>
<th><p><span data-ttu-id="6b78d-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b78d-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6b78d-108"><strong>adAccessDeny</strong></span><span class="sxs-lookup"><span data-stu-id="6b78d-108"><strong>adAccessDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="6b78d-109">3</span><span class="sxs-lookup"><span data-stu-id="6b78d-109">3</span></span></p></td>
<td><p><span data-ttu-id="6b78d-110">Se denegarán los permisos especificados al grupo o al usuario.</span><span class="sxs-lookup"><span data-stu-id="6b78d-110">The group or user will be denied the specified permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b78d-111"><strong>adAccessGrant</strong></span><span class="sxs-lookup"><span data-stu-id="6b78d-111"><strong>adAccessGrant</strong></span></span></p></td>
<td><p><span data-ttu-id="6b78d-112">1</span><span class="sxs-lookup"><span data-stu-id="6b78d-112">1</span></span></p></td>
<td><p><span data-ttu-id="6b78d-113">El grupo o el usuario tendrá al menos los permisos solicitados.</span><span class="sxs-lookup"><span data-stu-id="6b78d-113">The group or user will have at least the requested permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b78d-114"><strong>adAccessRevoke</strong></span><span class="sxs-lookup"><span data-stu-id="6b78d-114"><strong>adAccessRevoke</strong></span></span></p></td>
<td><p><span data-ttu-id="6b78d-115">4</span><span class="sxs-lookup"><span data-stu-id="6b78d-115">4</span></span></p></td>
<td><p><span data-ttu-id="6b78d-116">Se revocará todo derecho de acceso explícito que tenga el grupo o el usuario.</span><span class="sxs-lookup"><span data-stu-id="6b78d-116">Any explicit access rights the group or user has will be revoked.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b78d-117"><strong>adAccessSet</strong></span><span class="sxs-lookup"><span data-stu-id="6b78d-117"><strong>adAccessSet</strong></span></span></p></td>
<td><p><span data-ttu-id="6b78d-118">2</span><span class="sxs-lookup"><span data-stu-id="6b78d-118">2</span></span></p></td>
<td><p><span data-ttu-id="6b78d-119">El grupo o el usuario tendrá exactamente los permisos solicitados.</span><span class="sxs-lookup"><span data-stu-id="6b78d-119">The group or user will have exactly the requested permissions.</span></span></p></td>
</tr>
</tbody>
</table>

