---
title: Instrucción GRANT (Microsoft Access SQL)
TOCTitle: GRANT Statement (Microsoft Access SQL)
ms:assetid: 50ae97ae-d5be-57e5-d9da-f3fc42f01d83
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193820(v=office.15)
ms:contentKeyID: 48544800
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277478
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d4fffc9ac40586be899de0dd4054ba39dd3a6489
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483351"
---
# <a name="grant-statement-microsoft-access-sql"></a><span data-ttu-id="ba895-102">Instrucción GRANT (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="ba895-102">GRANT Statement (Microsoft Access SQL)</span></span>


<span data-ttu-id="ba895-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ba895-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ba895-104">Concede privilegios específicos a un usuario o grupo existente.</span><span class="sxs-lookup"><span data-stu-id="ba895-104">Grants specific privileges to an existing user or group.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba895-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ba895-105">Syntax</span></span>

<span data-ttu-id="ba895-106">GRANT {*privilegio*\[, *privilegio*,... \]} ON {tabla *tabla* | OBJETO *objeto*|</span><span class="sxs-lookup"><span data-stu-id="ba895-106">GRANT {*privilege*\[, *privilege*, …\]} ON{TABLE *table* | OBJECT *object*|</span></span>

<span data-ttu-id="ba895-107">*Contenedor* de contenedor} TO {*nombredeautorización*\[, *nombredeautorización*,... \]}</span><span class="sxs-lookup"><span data-stu-id="ba895-107">CONTAINER *container* } TO {*authorizationname*\[, *authorizationname*, …\]}</span></span>

<span data-ttu-id="ba895-108">La instrucción GRANT consta de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="ba895-108">The GRANT statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ba895-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="ba895-109">Part</span></span></p></th>
<th><p><span data-ttu-id="ba895-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ba895-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ba895-111"><em>privilegio</em></span><span class="sxs-lookup"><span data-stu-id="ba895-111"><em>privilege</em></span></span></p></td>
<td><p><span data-ttu-id="ba895-112">El privilegio o privilegios que se conceden.</span><span class="sxs-lookup"><span data-stu-id="ba895-112">The privilege or privileges to be granted.</span></span> <span data-ttu-id="ba895-113">Los privilegios se especifican mediante las siguientes palabras clave: seleccionar, eliminar, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA y UPDATEOWNER.</span><span class="sxs-lookup"><span data-stu-id="ba895-113">Privileges are specified using the following keywords: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA and UPDATEOWNER.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba895-114"><em>nombretabla</em></span><span class="sxs-lookup"><span data-stu-id="ba895-114"><em>tablename</em></span></span></p></td>
<td><p><span data-ttu-id="ba895-115">Cualquier nombre de tabla válido.</span><span class="sxs-lookup"><span data-stu-id="ba895-115">Any valid table name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba895-116"><em>object</em></span><span class="sxs-lookup"><span data-stu-id="ba895-116"><em>object</em></span></span></p></td>
<td><p><span data-ttu-id="ba895-p102">Puede incluir cualquier objeto que no sea tabla. Por ejemplo, una consulta (vista o procedimiento) almacenada.</span><span class="sxs-lookup"><span data-stu-id="ba895-p102">This can encompass any non-table object. A stored query (view or procedure) is one example.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba895-119"><em>contenedor</em></span><span class="sxs-lookup"><span data-stu-id="ba895-119"><em>container</em></span></span></p></td>
<td><p><span data-ttu-id="ba895-120">Nombre de un contenedor válido.</span><span class="sxs-lookup"><span data-stu-id="ba895-120">The name of a valid container.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba895-121"><em>nombreDeAutorización</em></span><span class="sxs-lookup"><span data-stu-id="ba895-121"><em>authorizationname</em></span></span></p></td>
<td><p><span data-ttu-id="ba895-122">Nombre de usuario o grupo.</span><span class="sxs-lookup"><span data-stu-id="ba895-122">A user or group name.</span></span></p></td>
</tr>
</tbody>
</table>

