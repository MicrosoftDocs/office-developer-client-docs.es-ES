---
title: ActionEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: ActionEnum
ms:assetid: 225024c1-9088-b532-2a23-04c1aaaaa892
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248998(v=office.15)
ms:contentKeyID: 48543704
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: af0e5fd734c03b88990383b99815d6e35f2c1290
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483771"
---
# <a name="actionenum"></a><span data-ttu-id="afbbf-102">ActionEnum</span><span class="sxs-lookup"><span data-stu-id="afbbf-102">ActionEnum</span></span>


<span data-ttu-id="afbbf-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="afbbf-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="afbbf-104">Especifica el tipo de acción que se debe realizar cuando se llama a [SetPermissions](setpermissions-method-adox.md).</span><span class="sxs-lookup"><span data-stu-id="afbbf-104">Specifies the type of action to be performed when [SetPermissions](setpermissions-method-adox.md) is called.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="afbbf-105">Constante</span><span class="sxs-lookup"><span data-stu-id="afbbf-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="afbbf-106">Valor</span><span class="sxs-lookup"><span data-stu-id="afbbf-106">Value</span></span></p></th>
<th><p><span data-ttu-id="afbbf-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="afbbf-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="afbbf-108"><strong>adAccessDeny</strong></span><span class="sxs-lookup"><span data-stu-id="afbbf-108"><strong>adAccessDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="afbbf-109">3</span><span class="sxs-lookup"><span data-stu-id="afbbf-109">3</span></span></p></td>
<td><p><span data-ttu-id="afbbf-110">Se denegarán los permisos especificados al grupo o al usuario.</span><span class="sxs-lookup"><span data-stu-id="afbbf-110">The group or user will be denied the specified permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afbbf-111"><strong>adAccessGrant</strong></span><span class="sxs-lookup"><span data-stu-id="afbbf-111"><strong>adAccessGrant</strong></span></span></p></td>
<td><p><span data-ttu-id="afbbf-112">1</span><span class="sxs-lookup"><span data-stu-id="afbbf-112">1</span></span></p></td>
<td><p><span data-ttu-id="afbbf-113">El grupo o el usuario tendrá al menos los permisos solicitados.</span><span class="sxs-lookup"><span data-stu-id="afbbf-113">The group or user will have at least the requested permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afbbf-114"><strong>adAccessRevoke</strong></span><span class="sxs-lookup"><span data-stu-id="afbbf-114"><strong>adAccessRevoke</strong></span></span></p></td>
<td><p><span data-ttu-id="afbbf-115">4</span><span class="sxs-lookup"><span data-stu-id="afbbf-115">4</span></span></p></td>
<td><p><span data-ttu-id="afbbf-116">Se revocará todo derecho de acceso explícito que tenga el grupo o el usuario.</span><span class="sxs-lookup"><span data-stu-id="afbbf-116">Any explicit access rights the group or user has will be revoked.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afbbf-117"><strong>adAccessSet</strong></span><span class="sxs-lookup"><span data-stu-id="afbbf-117"><strong>adAccessSet</strong></span></span></p></td>
<td><p><span data-ttu-id="afbbf-118">2</span><span class="sxs-lookup"><span data-stu-id="afbbf-118">2</span></span></p></td>
<td><p><span data-ttu-id="afbbf-119">El grupo o el usuario tendrá exactamente los permisos solicitados.</span><span class="sxs-lookup"><span data-stu-id="afbbf-119">The group or user will have exactly the requested permissions.</span></span></p></td>
</tr>
</tbody>
</table>

