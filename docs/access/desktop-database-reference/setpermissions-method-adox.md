---
title: SetPermissions (método, ADOX)
TOCTitle: SetPermissions Method (ADOX)
ms:assetid: 63d1053d-fb32-456b-ae67-3a4e45aa01af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249382(v=office.15)
ms:contentKeyID: 48545274
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 35578de28509e510e9ba5329cfdabc2eff8207b1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485810"
---
# <a name="setpermissions-method-adox"></a><span data-ttu-id="9f88b-102">SetPermissions (método, ADOX)</span><span class="sxs-lookup"><span data-stu-id="9f88b-102">SetPermissions Method (ADOX)</span></span>


<span data-ttu-id="9f88b-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9f88b-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="9f88b-104">Especifica los permisos para un grupo o un usuario en un objeto.</span><span class="sxs-lookup"><span data-stu-id="9f88b-104">Specifies the permissions for a group or user on an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f88b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f88b-105">Syntax</span></span>

<span data-ttu-id="9f88b-106">*Grupo_o_usuario*. SetPermissions*nombre*, *ObjectType*, *acción*, *derechos* \[,*heredar* \] \[,*valor de ObjectTypeId*\]</span><span class="sxs-lookup"><span data-stu-id="9f88b-106">*GroupOrUser*.SetPermissions*Name*, *ObjectType*, *Action*, *Rights* \[,*Inherit*\] \[,*ObjectTypeId*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="9f88b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9f88b-107">Parameters</span></span>

  - <span data-ttu-id="9f88b-108">*Name*</span><span class="sxs-lookup"><span data-stu-id="9f88b-108">*Name*</span></span>

  - <span data-ttu-id="9f88b-109">Un valor **String** que especifica el nombre del objeto para el que se van a establecer permisos.</span><span class="sxs-lookup"><span data-stu-id="9f88b-109">A **String** value that specifies the name of the object for which to set permissions.</span></span>

  - <span data-ttu-id="9f88b-110">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="9f88b-110">*ObjectType*</span></span>

  - <span data-ttu-id="9f88b-111">Un valor **Long** que puede ser una de las constantes [ObjectTypeEnum](objecttypeenum.md), que especifica el tipo de objeto para el que se van a obtener permisos.</span><span class="sxs-lookup"><span data-stu-id="9f88b-111">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get permissions.</span></span>

  - <span data-ttu-id="9f88b-112">*Action*</span><span class="sxs-lookup"><span data-stu-id="9f88b-112">*Action*</span></span>

  - <span data-ttu-id="9f88b-113">Un valor **Long** que puede ser una de las constantes [ActionEnum](actionenum.md), que especifica el tipo de acción que se realizará cuando se establezcan permisos.</span><span class="sxs-lookup"><span data-stu-id="9f88b-113">A **Long** value which can be one of the [ActionEnum](actionenum.md) constants that specifies the type of action to perform when setting permissions.</span></span>

  - <span data-ttu-id="9f88b-114">*Rights*</span><span class="sxs-lookup"><span data-stu-id="9f88b-114">*Rights*</span></span>

  - <span data-ttu-id="9f88b-115">Un valor **Long** que puede ser una máscara de bits de una o varias de las constantes [RightsEnum](rightsenum.md), que indica los derechos a establecer.</span><span class="sxs-lookup"><span data-stu-id="9f88b-115">A **Long** value which can be a bitmask of one or more of the [RightsEnum](rightsenum.md) constants, that indicates the rights to set.</span></span>

  - <span data-ttu-id="9f88b-116">*Inherit*</span><span class="sxs-lookup"><span data-stu-id="9f88b-116">*Inherit*</span></span>

  - <span data-ttu-id="9f88b-p101">Opcional. Un valor **Long** que puede ser una de las constantes [InheritTypeEnum](inherittypeenum.md), que especifica cómo heredarán estos permisos los objetos. El valor predeterminado es **adInheritNone**.</span><span class="sxs-lookup"><span data-stu-id="9f88b-p101">Optional. A **Long** value which can be one of the [InheritTypeEnum](inherittypeenum.md) constants, that specifies how objects will inherit these permissions. The default value is **adInheritNone**.</span></span>

  - <span data-ttu-id="9f88b-120">*Valor de ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="9f88b-120">*ObjectTypeId*</span></span>

  - <span data-ttu-id="9f88b-121">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9f88b-121">Optional.</span></span> <span data-ttu-id="9f88b-122">Un valor **Variant** que especifica el GUID correspondiente a un tipo de objeto de proveedor no definido en la especificación de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="9f88b-122">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="9f88b-123">Este parámetro es necesario si *ObjectType* se ha establecido en **adPermObjProviderSpecific**; de lo contrario, no se usa.</span><span class="sxs-lookup"><span data-stu-id="9f88b-123">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f88b-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9f88b-124">Remarks</span></span>

<span data-ttu-id="9f88b-125">Si el proveedor no admite el establecimiento de derechos de acceso para grupos o usuarios, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="9f88b-125">An error will occur if the provider does not support setting access rights for groups or users.</span></span>


> [!NOTE]
> <P><span data-ttu-id="9f88b-126">Cuando se llama a <STRONG>SetPermissions</STRONG>, establecimiento de Action en <STRONG>adAccessRevoke</STRONG> anula los valores del parámetro <EM>Rights</EM> .</span><span class="sxs-lookup"><span data-stu-id="9f88b-126">When calling <STRONG>SetPermissions</STRONG>, setting Actions to <STRONG>adAccessRevoke</STRONG> overrides any settings of the <EM>Rights</EM> parameter.</span></span> <span data-ttu-id="9f88b-127">No establezca <EM>acciones</EM> en <STRONG>adAccessRevoke</STRONG> si desea que los derechos especificados en el parámetro <EM>Rights</EM> surta efecto.</span><span class="sxs-lookup"><span data-stu-id="9f88b-127">Do not set <EM>Actions</EM> to <STRONG>adAccessRevoke</STRONG> if you want the rights specified in the <EM>Rights</EM> parameter to take effect.</span></span></P>


