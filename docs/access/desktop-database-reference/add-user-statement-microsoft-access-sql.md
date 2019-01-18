---
title: Instrucción ADD USER (Microsoft Access SQL)
TOCTitle: ADD USER statement (Microsoft Access SQL)
ms:assetid: 1feb631f-cb8c-14ae-6214-276f1faf1a55
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845862(v=office.15)
ms:contentKeyID: 48543652
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8ba60a646fd234748bcc39b9a5604a33675caee5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705396"
---
# <a name="add-user-statement-microsoft-access-sql"></a><span data-ttu-id="0d0c6-102">Instrucción ADD USER (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="0d0c6-102">ADD USER statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="0d0c6-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0d0c6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0d0c6-104">Agrega uno o varios *usuarios* existentes a un *grupo* existente.</span><span class="sxs-lookup"><span data-stu-id="0d0c6-104">Adds one or more existing *user*s to an existing *group*.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d0c6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0d0c6-105">Syntax</span></span>

<span data-ttu-id="0d0c6-106">ADD USER *usuario*\[, *usuario*,... \] Al *grupo*</span><span class="sxs-lookup"><span data-stu-id="0d0c6-106">ADD USER *user*\[, *user*, …\] TO *group*</span></span>

<span data-ttu-id="0d0c6-107">La instrucción ADD USER consta de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="0d0c6-107">The ADD USER statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0d0c6-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="0d0c6-108">Part</span></span></p></th>
<th><p><span data-ttu-id="0d0c6-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d0c6-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0d0c6-110"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="0d0c6-110"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="0d0c6-111">Nombre de un usuario que se agregará al archivo de información de grupo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="0d0c6-111">The name of a user to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d0c6-112"><em>grupo</em></span><span class="sxs-lookup"><span data-stu-id="0d0c6-112"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="0d0c6-113">Nombre de un grupo que se agregará al archivo de información de grupo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="0d0c6-113">The name of a group to be added to the workgroup information file.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="0d0c6-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0d0c6-114">Remarks</span></span>

<span data-ttu-id="0d0c6-115">Después de que un *usuario* se haya agregado a un *grupo*, el *usuario* tiene todos los permisos que se han concedido al *grupo*.</span><span class="sxs-lookup"><span data-stu-id="0d0c6-115">After a *user* had been added to a *group*, the *user* has all the permissions that have been granted to the *group*.</span></span>

