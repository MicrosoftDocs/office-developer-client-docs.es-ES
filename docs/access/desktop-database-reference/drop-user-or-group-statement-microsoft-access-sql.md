---
title: DROP USER o GROUP (instrucción de Microsoft Access SQL)
TOCTitle: DROP USER or GROUP Statement (Microsoft Access SQL)
ms:assetid: 46bc5916-556b-17df-2f4c-8fd7bbd21ef7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193192(v=office.15)
ms:contentKeyID: 48544575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3a5cf75de06c13e2452e5f33b8355b7fb480d8a3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483848"
---
# <a name="drop-user-or-group-statement-microsoft-access-sql"></a><span data-ttu-id="e8e24-102">DROP USER o GROUP (instrucción de Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="e8e24-102">DROP USER or GROUP Statement (Microsoft Access SQL)</span></span>


<span data-ttu-id="e8e24-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e8e24-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e8e24-104">Elimina uno o varios *usuarios* o *grupos* existentes, o elimina uno o varios *usuarios* en un *grupo* existente.</span><span class="sxs-lookup"><span data-stu-id="e8e24-104">Deletes one or more existing *user*s or *group*s, or removes one or more existing *user*s from an existing *group*.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8e24-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e8e24-105">Syntax</span></span>

<span data-ttu-id="e8e24-106">Para eliminar uno o varios *usuarios*, o eliminar uno o varios *usuarios* en un *grupo*:</span><span class="sxs-lookup"><span data-stu-id="e8e24-106">Delete one or more *user*s or remove one or more *user*s from a *group*:</span></span>

<span data-ttu-id="e8e24-107">DROP USER *usuario*\[, *usuario*,... \] \[De *grupo*\]</span><span class="sxs-lookup"><span data-stu-id="e8e24-107">DROP USER *user*\[, *user*, …\] \[FROM *group*\]</span></span>

<span data-ttu-id="e8e24-108">Para eliminar uno o varios *grupos*:</span><span class="sxs-lookup"><span data-stu-id="e8e24-108">Delete one or more *group*s:</span></span>

<span data-ttu-id="e8e24-109">DROP GROUP *grupo*\[, *grupo*,...\]</span><span class="sxs-lookup"><span data-stu-id="e8e24-109">DROP GROUP *group*\[, *group*, …\]</span></span>

<span data-ttu-id="e8e24-110">La instrucción DROP USER o GROUP consta de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="e8e24-110">The DROP USER or GROUP statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e8e24-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="e8e24-111">Part</span></span></p></th>
<th><p><span data-ttu-id="e8e24-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8e24-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8e24-113"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="e8e24-113"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="e8e24-114">Nombre de un usuario que se va a eliminar del archivo de información de grupo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="e8e24-114">The name of a user to be removed from the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8e24-115"><em>group</em></span><span class="sxs-lookup"><span data-stu-id="e8e24-115"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="e8e24-116">Nombre de un grupo que se va a eliminar del archivo de información de grupo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="e8e24-116">The name of a group to be removed from the workgroup information file.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e8e24-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e8e24-117">Remarks</span></span>

<span data-ttu-id="e8e24-p101">Si se usa la palabra clave FROM en la instrucción DROP USER, cada uno de los *usuarios* enumerados en la instrucción se eliminará del *grupo* especificado a continuación de la palabra clave FROM. Sin embargo, los *usuarios* en sí no se eliminarán.</span><span class="sxs-lookup"><span data-stu-id="e8e24-p101">If the FROM keyword is used in the DROP USER statement, then each of the *user*s listed in the statement will be removed from the *group* specified following the FROM keyword. However, the *user*s themselves will not be deleted.</span></span>

<span data-ttu-id="e8e24-p102">La instrucción DROP GROUP eliminará el *grupo* o los grupos especificados. Los *usuarios* que sean miembros del *grupo* o grupos no se verán afectados, pero ya no serán miembros del *grupo* eliminado.</span><span class="sxs-lookup"><span data-stu-id="e8e24-p102">The DROP GROUP statement will delete the specified *group*(s). The *user*s who are members of the *group*(s) will not be affected, but they will no longer be members of the deleted *group*(s).</span></span>

