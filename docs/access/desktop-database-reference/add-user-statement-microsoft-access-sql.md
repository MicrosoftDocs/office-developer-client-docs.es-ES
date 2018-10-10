---
title: ADD USER (instrucción de Microsoft Access SQL)
TOCTitle: ADD USER Statement (Microsoft Access SQL)
ms:assetid: 1feb631f-cb8c-14ae-6214-276f1faf1a55
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845862(v=office.15)
ms:contentKeyID: 48543652
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ba08ab3104fa08780e8affa310b52a65f67d8831
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485127"
---
# <a name="add-user-statement-microsoft-access-sql"></a><span data-ttu-id="9c513-102">ADD USER (instrucción de Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="9c513-102">ADD USER Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="9c513-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9c513-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9c513-104">Agrega uno o varios *usuarios* existentes a un *grupo* existente.</span><span class="sxs-lookup"><span data-stu-id="9c513-104">Adds one or more existing *user*s to an existing *group*.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c513-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9c513-105">Syntax</span></span>

<span data-ttu-id="9c513-106">ADD USER *usuario*\[, *usuario*,... \] Al *grupo*</span><span class="sxs-lookup"><span data-stu-id="9c513-106">ADD USER *user*\[, *user*, …\] TO *group*</span></span>

<span data-ttu-id="9c513-107">La instrucción ADD USER consta de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="9c513-107">The ADD USER statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9c513-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="9c513-108">Part</span></span></p></th>
<th><p><span data-ttu-id="9c513-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c513-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9c513-110"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="9c513-110"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="9c513-111">Nombre de un usuario que se agregará al archivo de información de grupo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="9c513-111">The name of a user to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c513-112"><em>group</em></span><span class="sxs-lookup"><span data-stu-id="9c513-112"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="9c513-113">Nombre de un grupo que se agregará al archivo de información de grupo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="9c513-113">The name of a group to be added to the workgroup information file.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="9c513-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9c513-114">Remarks</span></span>

<span data-ttu-id="9c513-115">Una vez que un *usuario* se haya agregado a un *grupo*, el *usuario* tendrá todos los permisos concedidos a dicho *grupo*.</span><span class="sxs-lookup"><span data-stu-id="9c513-115">Once a *user* had been added to a *group,* the *user* has all the permissions that have been granted to the *group*.</span></span>

