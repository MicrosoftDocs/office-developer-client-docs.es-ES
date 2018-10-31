---
title: Instrucción DROP USER o GROUP (Microsoft Access SQL)
TOCTitle: DROP USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 46bc5916-556b-17df-2f4c-8fd7bbd21ef7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193192(v=office.15)
ms:contentKeyID: 48544575
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: a7988a2124af13dc84cefe678342da969e349a06
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25864035"
---
# <a name="drop-user-or-group-statement-microsoft-access-sql"></a><span data-ttu-id="de2e7-102">Instrucción DROP USER o GROUP (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="de2e7-102">DROP USER or GROUP statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="de2e7-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="de2e7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="de2e7-104">Elimina uno o más existentes *a los usuarios* o *grupos*, o quita uno o varios existentes *a los usuarios* de un *grupo*de existente.</span><span class="sxs-lookup"><span data-stu-id="de2e7-104">Deletes one or more existing *users* or *groups*, or removes one or more existing *users* from an existing *group*.</span></span>

## <a name="syntax"></a><span data-ttu-id="de2e7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="de2e7-105">Syntax</span></span>

<span data-ttu-id="de2e7-106">**Eliminar uno o varios _usuarios_ o quitar uno o varios _usuarios_ de un _grupo_**:</span><span class="sxs-lookup"><span data-stu-id="de2e7-106">**Delete one or more _users_ or remove one or more _users_ from a _group_**:</span></span>

<span data-ttu-id="de2e7-107">DROP USER *usuario*\[, *usuario*,... \] \[De *grupo*\]</span><span class="sxs-lookup"><span data-stu-id="de2e7-107">DROP USER *user*\[, *user*, …\] \[FROM *group*\]</span></span>

<span data-ttu-id="de2e7-108">**Eliminar uno o varios _grupos_**:</span><span class="sxs-lookup"><span data-stu-id="de2e7-108">**Delete one or more _groups_**:</span></span>

<span data-ttu-id="de2e7-109">DROP GROUP *grupo*\[, *grupo*,...\]</span><span class="sxs-lookup"><span data-stu-id="de2e7-109">DROP GROUP *group*\[, *group*, …\]</span></span>

<span data-ttu-id="de2e7-110">La instrucción DROP USER o GROUP consta de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="de2e7-110">The DROP USER or GROUP statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="de2e7-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="de2e7-111">Part</span></span></p></th>
<th><p><span data-ttu-id="de2e7-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="de2e7-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="de2e7-113"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="de2e7-113"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="de2e7-114">Nombre de un usuario que se va a eliminar del archivo de información de grupo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="de2e7-114">The name of a user to be removed from the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de2e7-115"><em>group</em></span><span class="sxs-lookup"><span data-stu-id="de2e7-115"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="de2e7-116">Nombre de un grupo que se va a eliminar del archivo de información de grupo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="de2e7-116">The name of a group to be removed from the workgroup information file.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="de2e7-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="de2e7-117">Remarks</span></span>

<span data-ttu-id="de2e7-118">Si se utiliza la palabra clave FROM en la instrucción DROP USER, cada uno de los *usuarios* enumerados en la instrucción se quitarán del *grupo* especificado a continuación de la palabra clave FROM.</span><span class="sxs-lookup"><span data-stu-id="de2e7-118">If the FROM keyword is used in the DROP USER statement, each of the *users* listed in the statement will be removed from the *group* specified following the FROM keyword.</span></span> <span data-ttu-id="de2e7-119">Sin embargo, los *usuarios* no se eliminarán ellos mismos.</span><span class="sxs-lookup"><span data-stu-id="de2e7-119">However, the *users* themselves will not be deleted.</span></span>

<span data-ttu-id="de2e7-120">La instrucción DROP GROUP eliminará el *grupo*especificado (s).</span><span class="sxs-lookup"><span data-stu-id="de2e7-120">The DROP GROUP statement will delete the specified *group*(s).</span></span> <span data-ttu-id="de2e7-121">No se verán afectados los *usuarios* que son miembros del *grupo*(s), pero ya no serán miembros del *grupo*eliminado (s).</span><span class="sxs-lookup"><span data-stu-id="de2e7-121">The *users* who are members of the *group*(s) will not be affected, but they will no longer be members of the deleted *group*(s).</span></span>

