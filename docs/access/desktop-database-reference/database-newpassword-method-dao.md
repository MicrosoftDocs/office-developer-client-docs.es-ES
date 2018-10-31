---
title: Database.NewPassword Method (DAO)
TOCTitle: NewPassword Method
ms:assetid: 01c1c454-d651-222c-225a-2b02734a1b7a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844754(v=office.15)
ms:contentKeyID: 48542941
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052943
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 892dc16d0422572e83f92316ce2c1c67f9ce5cc0
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860647"
---
# <a name="databasenewpassword-method-dao"></a><span data-ttu-id="7047a-102">Database.NewPassword Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="7047a-102">Database.NewPassword Method (DAO)</span></span>


<span data-ttu-id="7047a-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7047a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7047a-104">Cambia la contraseña de una base de datos existente del motor de base de datos de Microsoft Access (sólo en áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="7047a-104">Changes the password of an existing Microsoft Access database engine database (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="7047a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7047a-105">Syntax</span></span>

<span data-ttu-id="7047a-106">*expresión* . NewPassword (***bstrOld***, ***bstrNew***)</span><span class="sxs-lookup"><span data-stu-id="7047a-106">*expression* .NewPassword(***bstrOld***, ***bstrNew***)</span></span>

<span data-ttu-id="7047a-107">*expresión* Una expresión que devuelve un objeto de **base de datos** .</span><span class="sxs-lookup"><span data-stu-id="7047a-107">*expression* An expression that returns a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="7047a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7047a-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7047a-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="7047a-109">Name</span></span></p></th>
<th><p><span data-ttu-id="7047a-110">Necesario/Opcional</span><span class="sxs-lookup"><span data-stu-id="7047a-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="7047a-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="7047a-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="7047a-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="7047a-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7047a-113">bstrOld</span><span class="sxs-lookup"><span data-stu-id="7047a-113">bstrOld</span></span></p></td>
<td><p><span data-ttu-id="7047a-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="7047a-114">Required</span></span></p></td>
<td><p><span data-ttu-id="7047a-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="7047a-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="7047a-116">Valor actual de la propiedad <strong>Password</strong> del objeto <strong>Database</strong>.</span><span class="sxs-lookup"><span data-stu-id="7047a-116">The current setting of the <strong>Password</strong> property of the <strong>Database</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7047a-117">bstrNew</span><span class="sxs-lookup"><span data-stu-id="7047a-117">bstrNew</span></span></p></td>
<td><p><span data-ttu-id="7047a-118">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="7047a-118">Required</span></span></p></td>
<td><p><span data-ttu-id="7047a-119"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="7047a-119"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="7047a-120">La nueva configuración de la propiedad <strong>Password</strong> del objeto de <strong>base de datos</strong> .</span><span class="sxs-lookup"><span data-stu-id="7047a-120">The new setting of the <strong>Password</strong> property of the <strong>Database</strong> object.</span></span></p>

> [!NOTE]
> <span data-ttu-id="7047a-p101">[!NOTA] Use contraseñas seguras que combinen letras mayúsculas y minúsculas, números y símbolos. Las contraseñas que no son seguras no contienen una combinación de estos elementos. Contraseña segura: Y6dh!et5. Contraseña no segura: House27. Use una contraseña segura que pueda recordar para no tener que anotarla.</span><span class="sxs-lookup"><span data-stu-id="7047a-p101">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span>


</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="7047a-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7047a-126">Remarks</span></span>

<span data-ttu-id="7047a-127">Las cadenas bstrOld y bstrNew pueden tener hasta 20 caracteres y pueden incluir cualquier carácter excepto el carácter ASCII 0 (null).</span><span class="sxs-lookup"><span data-stu-id="7047a-127">The bstrOld and bstrNew strings can be up to 20 characters long and can include any characters except the ASCII character 0 (null).</span></span> <span data-ttu-id="7047a-128">Para borrar la contraseña, utilice una cadena de longitud cero ("") para bstrNew.</span><span class="sxs-lookup"><span data-stu-id="7047a-128">To clear the password, use a zero-length string ("") for bstrNew.</span></span>

<span data-ttu-id="7047a-129">Las contraseñas distinguen entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="7047a-129">Passwords are case-sensitive.</span></span>

<span data-ttu-id="7047a-130">Si una base de datos no tiene contraseña, el motor de base de datos de Microsoft Access creará automáticamente una pasando una cadena de longitud cero ("") para la contraseña antigua.</span><span class="sxs-lookup"><span data-stu-id="7047a-130">If a database has no password, the Microsoft Access database engine will automatically create one by passing a zero-length string ("") for the old password.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="7047a-131">[!IMPORTANTE] Si pierde la contraseña, puede que nunca vuelva a abrir la base de datos.</span><span class="sxs-lookup"><span data-stu-id="7047a-131">If you lose your password, you can never open the database again.</span></span>


