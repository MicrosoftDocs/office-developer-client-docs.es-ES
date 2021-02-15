---
title: Método GetPermissions (ADOX)
TOCTitle: GetPermissions method (ADOX)
ms:assetid: 98a2b2b6-a8af-15ee-b052-622a6f0661b9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249683(v=office.15)
ms:contentKeyID: 48546496
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa5dda3c8e2ee8251fc54f4ff3bc12be0aca5002
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292247"
---
# <a name="getpermissions-method-adox"></a><span data-ttu-id="4c1ae-102">Método GetPermissions (ADOX)</span><span class="sxs-lookup"><span data-stu-id="4c1ae-102">GetPermissions method (ADOX)</span></span>

<span data-ttu-id="4c1ae-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4c1ae-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4c1ae-104">Devuelve los permisos para un grupo o un usuario en un objeto o un contenedor de objeto.</span><span class="sxs-lookup"><span data-stu-id="4c1ae-104">Returns the permissions for a group or user on an object or object container.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c1ae-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4c1ae-105">Syntax</span></span>

<span data-ttu-id="4c1ae-106">*ReturnValue*  =  *GroupOrUser*. GetPermissions(*Name*, *ObjectType* \[ ,*ObjectTypeId* \] )</span><span class="sxs-lookup"><span data-stu-id="4c1ae-106">*ReturnValue* = *GroupOrUser*.GetPermissions(*Name*, *ObjectType* \[,*ObjectTypeId*\])</span></span>

## <a name="return-value"></a><span data-ttu-id="4c1ae-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4c1ae-107">Return value</span></span>

<span data-ttu-id="4c1ae-p101">Devuelve un valor **Long** que especifica una máscara de bits que contiene los permisos del grupo o del usuario en el objeto. Este valor puede ser una o varias de las constantes [RightsEnum](rightsenum.md).</span><span class="sxs-lookup"><span data-stu-id="4c1ae-p101">Returns a **Long** value that specifies a bitmask containing the permissions that the group or user has on the object. This value can be one or more of the [RightsEnum](rightsenum.md) constants.</span></span>

## <a name="parameters"></a><span data-ttu-id="4c1ae-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4c1ae-110">Parameters</span></span>

|<span data-ttu-id="4c1ae-111">Parámetro</span><span class="sxs-lookup"><span data-stu-id="4c1ae-111">Parameter</span></span>|<span data-ttu-id="4c1ae-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c1ae-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="4c1ae-113">*Name*</span><span class="sxs-lookup"><span data-stu-id="4c1ae-113">*Name*</span></span> |<span data-ttu-id="4c1ae-p102">Un valor **Variant** que especifica el nombre del objeto para el que se van a establecer permisos. Establezca *Name* en un valor nulo si desea obtener los permisos para el contenedor de objeto.</span><span class="sxs-lookup"><span data-stu-id="4c1ae-p102">A **Variant** value that specifies the name of the object for which to set permissions. Set *Name* to a null value if you want to get the permissions for the object container.</span></span>|
|<span data-ttu-id="4c1ae-116">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="4c1ae-116">*ObjectType*</span></span> |<span data-ttu-id="4c1ae-117">Un valor **Long** que puede ser una de las constantes [ObjectTypeEnum](objecttypeenum.md), que especifica el tipo de objeto para el que se van a obtener permisos.</span><span class="sxs-lookup"><span data-stu-id="4c1ae-117">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get permissions.</span></span>|
|<span data-ttu-id="4c1ae-118">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="4c1ae-118">*ObjectTypeId*</span></span> |<span data-ttu-id="4c1ae-p103">Opcional. Un valor **Variant** que especifica el GUID correspondiente a un tipo de objeto de proveedor no definido en la especificación de OLE DB. Este parámetro es necesario si *ObjectType* se ha establecido en **adPermObjProviderSpecific**; de lo contrario, no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4c1ae-p103">Optional. A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification. This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>|

