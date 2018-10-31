---
title: REVOCAR declaración (Microsoft Access SQL)
TOCTitle: REVOKE statement (Microsoft Access SQL)
ms:assetid: 69399fd6-c4e8-f2e2-e5f4-48ae779323f5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195272(v=office.15)
ms:contentKeyID: 48545409
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277479
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4bcdd7aa77823a53ba2a2c0cde4badbac571611a
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860549"
---
# <a name="revoke-statement-microsoft-access-sql"></a><span data-ttu-id="056ba-102">REVOCAR declaración (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="056ba-102">REVOKE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="056ba-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="056ba-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="056ba-104">Revoca privilegios específicos a un usuario o grupo existente.</span><span class="sxs-lookup"><span data-stu-id="056ba-104">Revokes specific privileges from an existing user or group.</span></span>

## <a name="syntax"></a><span data-ttu-id="056ba-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="056ba-105">Syntax</span></span>

<span data-ttu-id="056ba-106">REVOKE {*privilegio*\[, *privilegio*,... \]} ON {tabla *tabla* | OBJETO *objeto*|</span><span class="sxs-lookup"><span data-stu-id="056ba-106">REVOKE {*privilege*\[, *privilege*, …\]} ON {TABLE *table* | OBJECT *object*|</span></span>

<span data-ttu-id="056ba-107">CONTAINTER *contenedor*} FROM {*nombredeautorización*\[, *nombredeautorización*,... \]}</span><span class="sxs-lookup"><span data-stu-id="056ba-107">CONTAINTER *container*} FROM {*authorizationname*\[, *authorizationname*, …\]}</span></span>

<span data-ttu-id="056ba-108">La instrucción REVOKE consta de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="056ba-108">The REVOKE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="056ba-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="056ba-109">Part</span></span></p></th>
<th><p><span data-ttu-id="056ba-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="056ba-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="056ba-111"><em>privilegio</em></span><span class="sxs-lookup"><span data-stu-id="056ba-111"><em>privilege</em></span></span></p></td>
<td><p><span data-ttu-id="056ba-112">Privilegio o privilegios que se va a revocar.</span><span class="sxs-lookup"><span data-stu-id="056ba-112">The privilege or privileges to be revoked.</span></span> <span data-ttu-id="056ba-113">Los privilegios se especifican mediante las siguientes palabras clave: seleccionar, eliminar, insertar, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, esquema y UPDATEOWNER.</span><span class="sxs-lookup"><span data-stu-id="056ba-113">Privileges are specified using the following keywords: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA, and UPDATEOWNER.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="056ba-114"><em>tabla</em></span><span class="sxs-lookup"><span data-stu-id="056ba-114"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="056ba-115">Cualquier nombre de tabla válido.</span><span class="sxs-lookup"><span data-stu-id="056ba-115">Any valid table name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="056ba-116"><em>object</em></span><span class="sxs-lookup"><span data-stu-id="056ba-116"><em>object</em></span></span></p></td>
<td><p><span data-ttu-id="056ba-p102">Puede incluir cualquier objeto que no sea tabla. Por ejemplo, una consulta (vista o procedimiento) almacenada.</span><span class="sxs-lookup"><span data-stu-id="056ba-p102">This can encompass any non-table object. A stored query (view or procedure) is one example.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="056ba-119"><em>contenedor</em></span><span class="sxs-lookup"><span data-stu-id="056ba-119"><em>container</em></span></span></p></td>
<td><p><span data-ttu-id="056ba-120">Nombre de un contenedor válido.</span><span class="sxs-lookup"><span data-stu-id="056ba-120">The name of a valid container.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="056ba-121"><em>nombreDeAutorización</em></span><span class="sxs-lookup"><span data-stu-id="056ba-121"><em>authorizationname</em></span></span></p></td>
<td><p><span data-ttu-id="056ba-122">Nombre de usuario o grupo.</span><span class="sxs-lookup"><span data-stu-id="056ba-122">A user or group name.</span></span></p></td>
</tr>
</tbody>
</table>

