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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280428"
---
# <a name="add-user-statement-microsoft-access-sql"></a><span data-ttu-id="05f55-102">Instrucción ADD USER (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="05f55-102">ADD USER statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="05f55-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="05f55-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="05f55-104">Agrega uno o varios *usuarios* existentes a un *grupo* existente.</span><span class="sxs-lookup"><span data-stu-id="05f55-104">Adds one or more existing *user* s to an existing *group*.</span></span>

## <a name="syntax"></a><span data-ttu-id="05f55-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="05f55-105">Syntax</span></span>

<span data-ttu-id="05f55-106">AGREGAR *usuario,* \[ *usuario,*... \] Grupo *PARA*</span><span class="sxs-lookup"><span data-stu-id="05f55-106">ADD USER *user*\[, *user*, …\] TO *group*</span></span>

<span data-ttu-id="05f55-107">La instrucción ADD USER consta de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="05f55-107">The ADD USER statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="05f55-108">Parte</span><span class="sxs-lookup"><span data-stu-id="05f55-108">Part</span></span></p></th>
<th><p><span data-ttu-id="05f55-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="05f55-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="05f55-110"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="05f55-110"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="05f55-111">Nombre de un usuario que se agregará al archivo de información de grupo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="05f55-111">The name of a user to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05f55-112"><em>group</em></span><span class="sxs-lookup"><span data-stu-id="05f55-112"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="05f55-113">Nombre de un grupo que se agregará al archivo de información de grupo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="05f55-113">The name of a group to be added to the workgroup information file.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="05f55-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="05f55-114">Remarks</span></span>

<span data-ttu-id="05f55-115">Después de *agregar* un usuario a  un *grupo,* el usuario tiene todos los permisos que se han concedido al *grupo.*</span><span class="sxs-lookup"><span data-stu-id="05f55-115">After a *user* had been added to a *group*, the *user* has all the permissions that have been granted to the *group*.</span></span>

