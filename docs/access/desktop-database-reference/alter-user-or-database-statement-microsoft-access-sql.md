---
title: Instrucción ALTER USER o DATABASE (Microsoft Access SQL)
TOCTitle: ALTER USER or DATABASE statement (Microsoft Access SQL)
ms:assetid: 86ccd296-5171-97e7-683f-cdaab4bde9ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197012(v=office.15)
ms:contentKeyID: 48546093
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: f0baf0faab717c35da0313d36e2ec1ac73528255
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879441"
---
# <a name="alter-user-or-database-statement-microsoft-access-sql"></a><span data-ttu-id="518c7-102">Instrucción ALTER USER o DATABASE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="518c7-102">ALTER USER or DATABASE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="518c7-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="518c7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="518c7-104">Cambia la contraseña de un usuario existente o de una base de datos.</span><span class="sxs-lookup"><span data-stu-id="518c7-104">Changes the password for an existing user or for a database.</span></span>

## <a name="syntax"></a><span data-ttu-id="518c7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="518c7-105">Syntax</span></span>

<span data-ttu-id="518c7-106">ALTER DATABASE PASSWORD *contraseñaNueva contraseñaAntigua*</span><span class="sxs-lookup"><span data-stu-id="518c7-106">ALTER DATABASE PASSWORD *newpassword oldpassword*</span></span>

<span data-ttu-id="518c7-107">ALTER USER *usuario* PASSWORD *contraseñaNueva contraseñaAntigua*</span><span class="sxs-lookup"><span data-stu-id="518c7-107">ALTER USER *user* PASSWORD *newpassword oldpassword*</span></span>

<span data-ttu-id="518c7-108">La instrucción ALTER USER o DATABASE consta de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="518c7-108">The ALTER USER or DATABASE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="518c7-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="518c7-109">Part</span></span></p></th>
<th><p><span data-ttu-id="518c7-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="518c7-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="518c7-111"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="518c7-111"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="518c7-112">Nombre de un usuario que se agregará al archivo de información de grupo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="518c7-112">The name of a user to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="518c7-113"><em>contraseñaNueva</em></span><span class="sxs-lookup"><span data-stu-id="518c7-113"><em>newpassword</em></span></span></p></td>
<td><p><span data-ttu-id="518c7-114">Nueva contraseña que se asociará con el nombre del <em>usuario</em> o la <em>base de datos</em> especificados.</span><span class="sxs-lookup"><span data-stu-id="518c7-114">The new password to be associated with the specified <em>user</em> or <em>database</em> name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="518c7-115"><em>contraseñaAntigua</em></span><span class="sxs-lookup"><span data-stu-id="518c7-115"><em>oldpassword</em></span></span></p></td>
<td><p><span data-ttu-id="518c7-116">Contraseña existente que se asociará con el nombre del <em>usuario</em> o <em>grupo</em> especificados.</span><span class="sxs-lookup"><span data-stu-id="518c7-116">The existing password to be associated with the specified <em>user</em> or <em>group</em> name.</span></span></p></td>
</tr>
</tbody>
</table>

