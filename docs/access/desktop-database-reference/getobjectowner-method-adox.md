---
title: Método GetObjectOwner (ADOX)
TOCTitle: GetObjectOwner method (ADOX)
ms:assetid: 716dd49a-8663-3f7a-32a3-0be353aea506
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249451(v=office.15)
ms:contentKeyID: 48545585
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 948464534f9bbfbea50c8eba2c926dea9cb9bcac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292261"
---
# <a name="getobjectowner-method-adox"></a><span data-ttu-id="3b74d-102">Método GetObjectOwner (ADOX)</span><span class="sxs-lookup"><span data-stu-id="3b74d-102">GetObjectOwner method (ADOX)</span></span>

<span data-ttu-id="3b74d-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3b74d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3b74d-104">Devuelve el propietario de un objeto de un [catálogo](catalog-object-adox.md).</span><span class="sxs-lookup"><span data-stu-id="3b74d-104">Returns the owner of an object in a [Catalog](catalog-object-adox.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3b74d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b74d-105">Syntax</span></span>

<span data-ttu-id="3b74d-106">*Propietario*  =  *Catálogo*. GetObjectOwner(*ObjectName*, *ObjectType* \[ ,*ObjectTypeId* \] )</span><span class="sxs-lookup"><span data-stu-id="3b74d-106">*Owner* = *Catalog*.GetObjectOwner(*ObjectName*, *ObjectType* \[,*ObjectTypeId*\])</span></span>

## <a name="return-value"></a><span data-ttu-id="3b74d-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b74d-107">Return value</span></span>

<span data-ttu-id="3b74d-108">Devuelve un valor **String** que especifica el [nombre](name-property-adox.md) del [usuario](user-object-adox.md) o el [grupo](group-object-adox.md) propietario del objeto.</span><span class="sxs-lookup"><span data-stu-id="3b74d-108">Returns a **String** value that specifies the [Name](name-property-adox.md) of the [User](user-object-adox.md) or [Group](group-object-adox.md) that owns the object.</span></span>

## <a name="parameters"></a><span data-ttu-id="3b74d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3b74d-109">Parameters</span></span>

|<span data-ttu-id="3b74d-110">Parámetro</span><span class="sxs-lookup"><span data-stu-id="3b74d-110">Parameter</span></span>|<span data-ttu-id="3b74d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="3b74d-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="3b74d-112">*ObjectName*</span><span class="sxs-lookup"><span data-stu-id="3b74d-112">*ObjectName*</span></span> |<span data-ttu-id="3b74d-113">Un valor **String** que especifica el nombre del objeto cuyo propietario se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="3b74d-113">A **String** value that specifies the name of the object for which to return the owner.</span></span>|
|<span data-ttu-id="3b74d-114">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="3b74d-114">*ObjectType*</span></span> |<span data-ttu-id="3b74d-115">Un valor **Long** que puede ser una de las constantes [ObjectTypeEnum](objecttypeenum.md), que especifica el tipo de objeto cuyo propietario se va a obtener.</span><span class="sxs-lookup"><span data-stu-id="3b74d-115">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get the owner.</span></span>|
|<span data-ttu-id="3b74d-116">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="3b74d-116">*ObjectTypeId*</span></span> |<span data-ttu-id="3b74d-p101">Opcional. Un valor **Variant** que especifica el GUID correspondiente a un tipo de objeto de proveedor no definido en la especificación de OLE DB. Este parámetro es necesario si *ObjectType* se ha establecido en **adPermObjProviderSpecific**; de lo contrario, no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="3b74d-p101">Optional. A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification. This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>|

## <a name="remarks"></a><span data-ttu-id="3b74d-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3b74d-120">Remarks</span></span>

<span data-ttu-id="3b74d-121">Si el proveedor no admite la devolución de propietarios de objetos, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="3b74d-121">An error will occur if the provider does not support returning object owners.</span></span>

