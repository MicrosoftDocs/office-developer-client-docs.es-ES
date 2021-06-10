---
title: Instrucción DROP USER o GROUP (Microsoft Access SQL)
TOCTitle: DROP USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 46bc5916-556b-17df-2f4c-8fd7bbd21ef7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193192(v=office.15)
ms:contentKeyID: 48544575
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 995f935ceea5af3b740215c5a4137e02e7ebb1b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293647"
---
# <a name="drop-user-or-group-statement-microsoft-access-sql"></a><span data-ttu-id="4818d-102">Instrucción DROP USER o GROUP (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="4818d-102">DROP USER or GROUP statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="4818d-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4818d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4818d-104">Elimina uno o varios *usuarios* o grupos existentes *o* quita uno o más usuarios *existentes* de un grupo *existente.*</span><span class="sxs-lookup"><span data-stu-id="4818d-104">Deletes one or more existing *users* or *groups*, or removes one or more existing *users* from an existing *group*.</span></span>

## <a name="syntax"></a><span data-ttu-id="4818d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4818d-105">Syntax</span></span>

### <a name="delete-one-or-more-users-or-remove-one-or-more-users-from-a-group"></a><span data-ttu-id="4818d-106">Eliminar uno o más usuarios o quitar uno o más usuarios de un grupo</span><span class="sxs-lookup"><span data-stu-id="4818d-106">Delete one or more users or remove one or more users from a group</span></span>

<span data-ttu-id="4818d-107">DROP USER *user* \[ , *user*, ... \] \[ Grupo *FROM*\]</span><span class="sxs-lookup"><span data-stu-id="4818d-107">DROP USER *user*\[, *user*, …\] \[FROM *group*\]</span></span>

### <a name="delete-one-or-more-groups"></a><span data-ttu-id="4818d-108">Eliminar uno o varios grupos</span><span class="sxs-lookup"><span data-stu-id="4818d-108">Delete one or more groups</span></span>

<span data-ttu-id="4818d-109">Grupo DE *DROP,* \[ *grupo*, ...\]</span><span class="sxs-lookup"><span data-stu-id="4818d-109">DROP GROUP *group*\[, *group*, …\]</span></span>

<span data-ttu-id="4818d-110">La instrucción DROP USER o GROUP consta de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="4818d-110">The DROP USER or GROUP statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4818d-111">Parte</span><span class="sxs-lookup"><span data-stu-id="4818d-111">Part</span></span></p></th>
<th><p><span data-ttu-id="4818d-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="4818d-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4818d-113"><em>usuario</em></span><span class="sxs-lookup"><span data-stu-id="4818d-113"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="4818d-114">Nombre de un usuario que se va a eliminar del archivo de información de grupo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="4818d-114">The name of a user to be removed from the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4818d-115"><em>group</em></span><span class="sxs-lookup"><span data-stu-id="4818d-115"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="4818d-116">Nombre de un grupo que se va a eliminar del archivo de información de grupo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="4818d-116">The name of a group to be removed from the workgroup information file.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4818d-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4818d-117">Remarks</span></span>

<span data-ttu-id="4818d-118">Si la palabra clave FROM se usa en  la instrucción DROP USER,  cada uno de los usuarios enumerados en la instrucción se quitará del grupo especificado después de la palabra clave FROM.</span><span class="sxs-lookup"><span data-stu-id="4818d-118">If the FROM keyword is used in the DROP USER statement, each of the *users* listed in the statement will be removed from the *group* specified following the FROM keyword.</span></span> <span data-ttu-id="4818d-119">Sin embargo, *los propios* usuarios no se eliminarán.</span><span class="sxs-lookup"><span data-stu-id="4818d-119">However, the *users* themselves will not be deleted.</span></span>

<span data-ttu-id="4818d-120">La instrucción DROP GROUP eliminará el *grupo* o los grupos especificados.</span><span class="sxs-lookup"><span data-stu-id="4818d-120">The DROP GROUP statement will delete the specified *group*(s).</span></span> <span data-ttu-id="4818d-121">Los *usuarios* que son miembros del grupo *(s)* no se verán afectados, pero ya no serán miembros de los grupos *eliminados.*</span><span class="sxs-lookup"><span data-stu-id="4818d-121">The *users* who are members of the *group*(s) will not be affected, but they will no longer be members of the deleted *group*(s).</span></span>

