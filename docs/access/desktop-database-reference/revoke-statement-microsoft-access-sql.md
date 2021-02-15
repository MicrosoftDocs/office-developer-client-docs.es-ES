---
title: Instrucción REVOKE (Microsoft Access SQL)
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
localization_priority: Normal
ms.openlocfilehash: 20122fee617597987940766a076d5f968a87c2d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306534"
---
# <a name="revoke-statement-microsoft-access-sql"></a><span data-ttu-id="b0463-102">Instrucción REVOKE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="b0463-102">REVOKE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="b0463-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b0463-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b0463-104">Revoca privilegios específicos a un usuario o grupo existente.</span><span class="sxs-lookup"><span data-stu-id="b0463-104">Revokes specific privileges from an existing user or group.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0463-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b0463-105">Syntax</span></span>

<span data-ttu-id="b0463-106">REVOKE {*privilege* \[ , *privilege*, ... \] } ON {TABLE *table |* Object *(objeto)*|</span><span class="sxs-lookup"><span data-stu-id="b0463-106">REVOKE {*privilege*\[, *privilege*, …\]} ON {TABLE *table* | OBJECT *object*|</span></span>

<span data-ttu-id="b0463-107">CONTENEDOR *CONTENEDOR*} FROM {*nombreDeAutorización* \[ , *nombreDeAutorización*, ... \] }</span><span class="sxs-lookup"><span data-stu-id="b0463-107">CONTAINTER *container*} FROM {*authorizationname*\[, *authorizationname*, …\]}</span></span>

<span data-ttu-id="b0463-108">La instrucción REVOKE consta de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="b0463-108">The REVOKE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b0463-109">Parte</span><span class="sxs-lookup"><span data-stu-id="b0463-109">Part</span></span></p></th>
<th><p><span data-ttu-id="b0463-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b0463-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b0463-111"><em>privilegio</em></span><span class="sxs-lookup"><span data-stu-id="b0463-111"><em>privilege</em></span></span></p></td>
<td><p><span data-ttu-id="b0463-112">Privilegio o privilegios que se van a revocar.</span><span class="sxs-lookup"><span data-stu-id="b0463-112">The privilege or privileges to be revoked.</span></span> <span data-ttu-id="b0463-113">Los privilegios se especifican mediante las siguientes palabras clave: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA y UPDATEOWNER.</span><span class="sxs-lookup"><span data-stu-id="b0463-113">Privileges are specified using the following keywords: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA, and UPDATEOWNER.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0463-114"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="b0463-114"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="b0463-115">Cualquier nombre de tabla válido.</span><span class="sxs-lookup"><span data-stu-id="b0463-115">Any valid table name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0463-116"><em>object</em></span><span class="sxs-lookup"><span data-stu-id="b0463-116"><em>object</em></span></span></p></td>
<td><p><span data-ttu-id="b0463-117">Puede incluir cualquier objeto que no sea tabla.</span><span class="sxs-lookup"><span data-stu-id="b0463-117">This can encompass any non-table object.</span></span> <span data-ttu-id="b0463-118">Por ejemplo, una consulta (vista o procedimiento) almacenada.</span><span class="sxs-lookup"><span data-stu-id="b0463-118">A stored query (view or procedure) is one example.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0463-119"><em>contenedor</em></span><span class="sxs-lookup"><span data-stu-id="b0463-119"><em>container</em></span></span></p></td>
<td><p><span data-ttu-id="b0463-120">Nombre de un contenedor válido.</span><span class="sxs-lookup"><span data-stu-id="b0463-120">The name of a valid container.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0463-121"><em>authorizationname</em></span><span class="sxs-lookup"><span data-stu-id="b0463-121"><em>authorizationname</em></span></span></p></td>
<td><p><span data-ttu-id="b0463-122">Nombre de usuario o grupo.</span><span class="sxs-lookup"><span data-stu-id="b0463-122">A user or group name.</span></span></p></td>
</tr>
</tbody>
</table>

