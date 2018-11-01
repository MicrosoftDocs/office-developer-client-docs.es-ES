---
title: GetPermissions (método, ADOX)
TOCTitle: GetPermissions Method (ADOX)
ms:assetid: 98a2b2b6-a8af-15ee-b052-622a6f0661b9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249683(v=office.15)
ms:contentKeyID: 48546496
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f53298d56f09b3df94c1b9e20158b3549317af6b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886539"
---
# <a name="getpermissions-method-adox"></a><span data-ttu-id="14dac-102">GetPermissions (método, ADOX)</span><span class="sxs-lookup"><span data-stu-id="14dac-102">GetPermissions Method (ADOX)</span></span>


<span data-ttu-id="14dac-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="14dac-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="14dac-104">Devuelve los permisos para un grupo o un usuario en un objeto o un contenedor de objeto.</span><span class="sxs-lookup"><span data-stu-id="14dac-104">Returns the permissions for a group or user on an object or object container.</span></span>

## <a name="syntax"></a><span data-ttu-id="14dac-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="14dac-105">Syntax</span></span>

<span data-ttu-id="14dac-106">*ReturnValue* = *Grupo_o_usuario*. GetPermissions (*nombre*, *ObjectType* \[,*valor de ObjectTypeId*\])</span><span class="sxs-lookup"><span data-stu-id="14dac-106">*ReturnValue* = *GroupOrUser*.GetPermissions(*Name*, *ObjectType* \[,*ObjectTypeId*\])</span></span>

## <a name="return-value"></a><span data-ttu-id="14dac-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="14dac-107">Return value</span></span>

<span data-ttu-id="14dac-p101">Devuelve un valor **Long** que especifica una máscara de bits que contiene los permisos del grupo o del usuario en el objeto. Este valor puede ser una o varias de las constantes [RightsEnum](rightsenum.md).</span><span class="sxs-lookup"><span data-stu-id="14dac-p101">Returns a **Long** value that specifies a bitmask containing the permissions that the group or user has on the object. This value can be one or more of the [RightsEnum](rightsenum.md) constants.</span></span>

## <a name="parameters"></a><span data-ttu-id="14dac-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="14dac-110">Parameters</span></span>

  - <span data-ttu-id="14dac-111">*Name*</span><span class="sxs-lookup"><span data-stu-id="14dac-111">*Name*</span></span>

  - <span data-ttu-id="14dac-112">Un valor **Variant** que especifica el nombre del objeto para el que se van a establecer permisos.</span><span class="sxs-lookup"><span data-stu-id="14dac-112">A **Variant** value that specifies the name of the object for which to set permissions.</span></span> <span data-ttu-id="14dac-113">*Nombre* del conjunto en un valor nulo si desea obtener los permisos para el contenedor de objetos.</span><span class="sxs-lookup"><span data-stu-id="14dac-113">Set *Name* to a null value if you want to get the permissions for the object container.</span></span>

  - <span data-ttu-id="14dac-114">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="14dac-114">*ObjectType*</span></span>

  - <span data-ttu-id="14dac-115">Un valor **Long** que puede ser una de las constantes [ObjectTypeEnum](objecttypeenum.md), que especifica el tipo de objeto para el que se van a obtener permisos.</span><span class="sxs-lookup"><span data-stu-id="14dac-115">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get permissions.</span></span>

  - <span data-ttu-id="14dac-116">*Valor de ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="14dac-116">*ObjectTypeId*</span></span>

  - <span data-ttu-id="14dac-117">Opcional.</span><span class="sxs-lookup"><span data-stu-id="14dac-117">Optional.</span></span> <span data-ttu-id="14dac-118">Un valor **Variant** que especifica el GUID correspondiente a un tipo de objeto de proveedor no definido en la especificación de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="14dac-118">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="14dac-119">Este parámetro es necesario si *ObjectType* se ha establecido en **adPermObjProviderSpecific**; de lo contrario, no se usa.</span><span class="sxs-lookup"><span data-stu-id="14dac-119">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>

