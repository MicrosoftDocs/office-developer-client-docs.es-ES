---
title: Instrucción CREATE USER o GROUP (Microsoft Access SQL)
TOCTitle: CREATE USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 62148ce2-0f81-944e-a1ab-edef990fff9f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194914(v=office.15)
ms:contentKeyID: 48545229
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5b294af16498778eae94b38a7a31b93fd029585e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295383"
---
# <a name="create-user-or-group-statement-microsoft-access-sql"></a><span data-ttu-id="67d37-102">Instrucción CREATE USER o GROUP (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="67d37-102">CREATE USER or GROUP statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="67d37-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="67d37-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="67d37-104">Crea uno o varios usuarios o grupos nuevos.</span><span class="sxs-lookup"><span data-stu-id="67d37-104">Creates one or more new users or groups.</span></span>

## <a name="syntax"></a><span data-ttu-id="67d37-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="67d37-105">Syntax</span></span>

### <a name="create-a-user"></a><span data-ttu-id="67d37-106">Crear un usuario</span><span class="sxs-lookup"><span data-stu-id="67d37-106">Create a user</span></span>

<span data-ttu-id="67d37-107">CREATE USER *password* *pid* \[ , *user* *password pid*, ...\]</span><span class="sxs-lookup"><span data-stu-id="67d37-107">CREATE USER *user* *password pid* \[, *user* *password pid*, …\]</span></span>

### <a name="create-a-group"></a><span data-ttu-id="67d37-108">Crear un grupo</span><span class="sxs-lookup"><span data-stu-id="67d37-108">Create a group</span></span>

<span data-ttu-id="67d37-109">CREATE GROUP *group* *pid,* \[ *group* *pid*, ...\]</span><span class="sxs-lookup"><span data-stu-id="67d37-109">CREATE GROUP *group* *pid*\[, *group* *pid*, …\]</span></span>

<span data-ttu-id="67d37-110">La instrucción CREATE USER o GROUP consta de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="67d37-110">The CREATE USER or GROUP statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="67d37-111">Parte</span><span class="sxs-lookup"><span data-stu-id="67d37-111">Part</span></span></p></th>
<th><p><span data-ttu-id="67d37-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="67d37-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="67d37-113"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="67d37-113"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="67d37-114">Nombre de un usuario que se agregará al archivo de información de grupo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="67d37-114">The name of a user to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67d37-115"><em>group</em></span><span class="sxs-lookup"><span data-stu-id="67d37-115"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="67d37-116">Nombre de un grupo que se agregará al archivo de información de grupo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="67d37-116">The name of a group to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67d37-117"><em>password</em></span><span class="sxs-lookup"><span data-stu-id="67d37-117"><em>password</em></span></span></p></td>
<td><p><span data-ttu-id="67d37-118">Contraseña que se asociará con el nombre de <em>usuario</em> especificado.</span><span class="sxs-lookup"><span data-stu-id="67d37-118">The password to be associated with the specified <em>user</em> name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67d37-119"><em>pid</em></span><span class="sxs-lookup"><span data-stu-id="67d37-119"><em>pid</em></span></span></p></td>
<td><p><span data-ttu-id="67d37-120">Id. personal.</span><span class="sxs-lookup"><span data-stu-id="67d37-120">The personal id.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="67d37-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="67d37-121">Remarks</span></span>

<span data-ttu-id="67d37-122">Un *usuario* y un *grupo* no pueden tener el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="67d37-122">A *user* and a *group* cannot have the same name.</span></span>

<span data-ttu-id="67d37-123">Es necesaria una *contraseña* para cada *usuario* o *grupo* que se cree.</span><span class="sxs-lookup"><span data-stu-id="67d37-123">A *password* is required for each *user* or *group* that is created.</span></span>

