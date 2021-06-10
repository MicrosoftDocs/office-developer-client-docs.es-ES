---
title: Método SetPermissions (ADOX)
TOCTitle: SetPermissions method (ADOX)
ms:assetid: 63d1053d-fb32-456b-ae67-3a4e45aa01af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249382(v=office.15)
ms:contentKeyID: 48545274
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4f9b393e90d579c131865b112263efd0aef3216b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314584"
---
# <a name="setpermissions-method-adox"></a><span data-ttu-id="b7804-102">Método SetPermissions (ADOX)</span><span class="sxs-lookup"><span data-stu-id="b7804-102">SetPermissions method (ADOX)</span></span>

<span data-ttu-id="b7804-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b7804-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b7804-104">Especifica los permisos para un grupo o un usuario en un objeto.</span><span class="sxs-lookup"><span data-stu-id="b7804-104">Specifies the permissions for a group or user on an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7804-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b7804-105">Syntax</span></span>

<span data-ttu-id="b7804-106">*GroupOrUser*. SetPermissions *Name*, *ObjectType*, *Action*, *Rights* \[ ,*Inherit* \] \[ ,*ObjectTypeId*\]</span><span class="sxs-lookup"><span data-stu-id="b7804-106">*GroupOrUser*.SetPermissions *Name*, *ObjectType*, *Action*, *Rights* \[,*Inherit*\] \[,*ObjectTypeId*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="b7804-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b7804-107">Parameters</span></span>

|<span data-ttu-id="b7804-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="b7804-108">Parameter</span></span>|<span data-ttu-id="b7804-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b7804-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="b7804-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="b7804-110">*Name*</span></span> |<span data-ttu-id="b7804-111">Un valor **String** que especifica el nombre del objeto para el que se van a establecer permisos.</span><span class="sxs-lookup"><span data-stu-id="b7804-111">A **String** value that specifies the name of the object for which to set permissions.</span></span>|
|<span data-ttu-id="b7804-112">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="b7804-112">*ObjectType*</span></span> |<span data-ttu-id="b7804-113">Un valor **Long** que puede ser una de las constantes [ObjectTypeEnum](objecttypeenum.md), que especifica el tipo de objeto para el que se van a obtener permisos.</span><span class="sxs-lookup"><span data-stu-id="b7804-113">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get permissions.</span></span>|
|<span data-ttu-id="b7804-114">*Action*</span><span class="sxs-lookup"><span data-stu-id="b7804-114">*Action*</span></span> |<span data-ttu-id="b7804-115">Un valor **Long** que puede ser una de las constantes [ActionEnum](actionenum.md), que especifica el tipo de acción que se realizará cuando se establezcan permisos.</span><span class="sxs-lookup"><span data-stu-id="b7804-115">A **Long** value which can be one of the [ActionEnum](actionenum.md) constants that specifies the type of action to perform when setting permissions.</span></span>|
|<span data-ttu-id="b7804-116">*Rights*</span><span class="sxs-lookup"><span data-stu-id="b7804-116">*Rights*</span></span> |<span data-ttu-id="b7804-117">Un valor **Long** que puede ser una máscara de bits de una o varias de las constantes [RightsEnum](rightsenum.md), que indica los derechos a establecer.</span><span class="sxs-lookup"><span data-stu-id="b7804-117">A **Long** value which can be a bitmask of one or more of the [RightsEnum](rightsenum.md) constants, that indicates the rights to set.</span></span>|
|<span data-ttu-id="b7804-118">*Inherit*</span><span class="sxs-lookup"><span data-stu-id="b7804-118">*Inherit*</span></span> |<span data-ttu-id="b7804-p101">Opcional. Un valor **Long** que puede ser una de las constantes [InheritTypeEnum](inherittypeenum.md), que especifica cómo heredarán estos permisos los objetos. El valor predeterminado es **adInheritNone**.</span><span class="sxs-lookup"><span data-stu-id="b7804-p101">Optional. A **Long** value which can be one of the [InheritTypeEnum](inherittypeenum.md) constants, that specifies how objects will inherit these permissions. The default value is **adInheritNone**.</span></span>|
|<span data-ttu-id="b7804-122">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="b7804-122">*ObjectTypeId*</span></span> |<span data-ttu-id="b7804-p102">Opcional. Un valor **Variant** que especifica el GUID correspondiente a un tipo de objeto de proveedor no definido en la especificación de OLE DB. Este parámetro es necesario si *ObjectType* se ha establecido en **adPermObjProviderSpecific**; de lo contrario, no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="b7804-p102">Optional. A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification. This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>|

## <a name="remarks"></a><span data-ttu-id="b7804-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b7804-126">Remarks</span></span>

<span data-ttu-id="b7804-127">Si el proveedor no admite el establecimiento de derechos de acceso para grupos o usuarios, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="b7804-127">An error will occur if the provider does not support setting access rights for groups or users.</span></span>

> [!NOTE]
> <span data-ttu-id="b7804-p103">Cuando se llama a **SetPermissions**, el establecimiento de Action en **adAccessRevoke** anula los valores del parámetro *Rights*. No establezca *Action* en **adAccessRevoke** si desea que los derechos especificados en el parámetro *Rights* sean efectivos.</span><span class="sxs-lookup"><span data-stu-id="b7804-p103">When calling **SetPermissions**, setting Actions to **adAccessRevoke** overrides any settings of the *Rights* parameter. Do not set *Actions* to **adAccessRevoke** if you want the rights specified in the *Rights* parameter to take effect.</span></span>


