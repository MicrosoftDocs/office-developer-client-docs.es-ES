---
title: Instrucción GRANT (Microsoft Access SQL)
TOCTitle: GRANT statement (Microsoft Access SQL)
ms:assetid: 50ae97ae-d5be-57e5-d9da-f3fc42f01d83
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193820(v=office.15)
ms:contentKeyID: 48544800
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277478
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4357099f8bcb9b2308b5cda3543949765b8c3420
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292135"
---
# <a name="grant-statement-microsoft-access-sql"></a><span data-ttu-id="3d84d-102">Instrucción GRANT (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="3d84d-102">GRANT statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="3d84d-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3d84d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3d84d-104">Concede privilegios específicos a un usuario o grupo existente.</span><span class="sxs-lookup"><span data-stu-id="3d84d-104">Grants specific privileges to an existing user or group.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d84d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3d84d-105">Syntax</span></span>

<span data-ttu-id="3d84d-106">Grant {*privilegio*\[, *privilegio*,... \]} On {TABLE *tabla* | Objeto \*\* Object|</span><span class="sxs-lookup"><span data-stu-id="3d84d-106">GRANT {*privilege*\[, *privilege*, …\]} ON{TABLE *table* | OBJECT *object*|</span></span>

<span data-ttu-id="3d84d-107">Contenedor \*\* contenedor} to {*nombredeautorización*\[, *nombredeautorización*,... \]}</span><span class="sxs-lookup"><span data-stu-id="3d84d-107">CONTAINER *container* } TO {*authorizationname*\[, *authorizationname*, …\]}</span></span>

<span data-ttu-id="3d84d-108">La instrucción GRANT consta de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="3d84d-108">The GRANT statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3d84d-109">Parte</span><span class="sxs-lookup"><span data-stu-id="3d84d-109">Part</span></span></p></th>
<th><p><span data-ttu-id="3d84d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="3d84d-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3d84d-111"><em>privilegia</em></span><span class="sxs-lookup"><span data-stu-id="3d84d-111"><em>privilege</em></span></span></p></td>
<td><p><span data-ttu-id="3d84d-112">Privilegio o privilegios que se van a conceder.</span><span class="sxs-lookup"><span data-stu-id="3d84d-112">The privilege or privileges to be granted.</span></span> <span data-ttu-id="3d84d-113">Los privilegios se especifican mediante las siguientes palabras clave: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA y UPDATEOWNER.</span><span class="sxs-lookup"><span data-stu-id="3d84d-113">Privileges are specified using the following keywords: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA, and UPDATEOWNER.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d84d-114"><em>NombreDeTabla</em></span><span class="sxs-lookup"><span data-stu-id="3d84d-114"><em>tablename</em></span></span></p></td>
<td><p><span data-ttu-id="3d84d-115">Cualquier nombre de tabla válido.</span><span class="sxs-lookup"><span data-stu-id="3d84d-115">Any valid table name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d84d-116"><em>object</em></span><span class="sxs-lookup"><span data-stu-id="3d84d-116"><em>object</em></span></span></p></td>
<td><p><span data-ttu-id="3d84d-117">Puede incluir cualquier objeto que no sea tabla.</span><span class="sxs-lookup"><span data-stu-id="3d84d-117">This can encompass any non-table object.</span></span> <span data-ttu-id="3d84d-118">Por ejemplo, una consulta (vista o procedimiento) almacenada.</span><span class="sxs-lookup"><span data-stu-id="3d84d-118">A stored query (view or procedure) is one example.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d84d-119"><em>recipiente</em></span><span class="sxs-lookup"><span data-stu-id="3d84d-119"><em>container</em></span></span></p></td>
<td><p><span data-ttu-id="3d84d-120">Nombre de un contenedor válido.</span><span class="sxs-lookup"><span data-stu-id="3d84d-120">The name of a valid container.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d84d-121"><em>nombredeautorización</em></span><span class="sxs-lookup"><span data-stu-id="3d84d-121"><em>authorizationname</em></span></span></p></td>
<td><p><span data-ttu-id="3d84d-122">Nombre de usuario o grupo.</span><span class="sxs-lookup"><span data-stu-id="3d84d-122">A user or group name.</span></span></p></td>
</tr>
</tbody>
</table>

