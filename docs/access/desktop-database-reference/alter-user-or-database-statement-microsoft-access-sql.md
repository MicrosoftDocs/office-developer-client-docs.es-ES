---
title: Instrucción ALTER USER o DATABASE (Microsoft Access SQL)
TOCTitle: ALTER USER or DATABASE statement (Microsoft Access SQL)
ms:assetid: 86ccd296-5171-97e7-683f-cdaab4bde9ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197012(v=office.15)
ms:contentKeyID: 48546093
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2514ca6403ce70acae9e344d610fbd7b9ba7d73b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297182"
---
# <a name="alter-user-or-database-statement-microsoft-access-sql"></a><span data-ttu-id="46e37-102">Instrucción ALTER USER o DATABASE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="46e37-102">ALTER USER or DATABASE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="46e37-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="46e37-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="46e37-104">Cambia la contraseña de un usuario existente o de una base de datos.</span><span class="sxs-lookup"><span data-stu-id="46e37-104">Changes the password for an existing user or for a database.</span></span>

## <a name="syntax"></a><span data-ttu-id="46e37-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46e37-105">Syntax</span></span>

<span data-ttu-id="46e37-106">ALTER DATABASE PASSWORD *contraseñaNueva contraseñaAntigua*</span><span class="sxs-lookup"><span data-stu-id="46e37-106">ALTER DATABASE PASSWORD *newpassword oldpassword*</span></span>

<span data-ttu-id="46e37-107">ALTER USER *usuario* PASSWORD *contraseñaNueva contraseñaAntigua*</span><span class="sxs-lookup"><span data-stu-id="46e37-107">ALTER USER *user* PASSWORD *newpassword oldpassword*</span></span>

<span data-ttu-id="46e37-108">La instrucción ALTER USER o DATABASE consta de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="46e37-108">The ALTER USER or DATABASE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="46e37-109">Parte</span><span class="sxs-lookup"><span data-stu-id="46e37-109">Part</span></span></p></th>
<th><p><span data-ttu-id="46e37-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="46e37-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="46e37-111"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="46e37-111"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="46e37-112">Nombre de un usuario que se agregará al archivo de información de grupo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="46e37-112">The name of a user to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46e37-113"><em>newpassword</em></span><span class="sxs-lookup"><span data-stu-id="46e37-113"><em>newpassword</em></span></span></p></td>
<td><p><span data-ttu-id="46e37-114">Nueva contraseña que se asociará con el nombre del <em>usuario</em> o la <em>base de datos</em> especificados.</span><span class="sxs-lookup"><span data-stu-id="46e37-114">The new password to be associated with the specified <em>user</em> or <em>database</em> name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46e37-115"><em>oldpassword</em></span><span class="sxs-lookup"><span data-stu-id="46e37-115"><em>oldpassword</em></span></span></p></td>
<td><p><span data-ttu-id="46e37-116">Contraseña existente que se asociará con el nombre del <em>usuario</em> o <em>grupo</em> especificados.</span><span class="sxs-lookup"><span data-stu-id="46e37-116">The existing password to be associated with the specified <em>user</em> or <em>group</em> name.</span></span></p></td>
</tr>
</tbody>
</table>

