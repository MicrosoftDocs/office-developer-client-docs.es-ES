---
title: GetObjectOwner (método, ADOX)
TOCTitle: GetObjectOwner Method (ADOX)
ms:assetid: 716dd49a-8663-3f7a-32a3-0be353aea506
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249451(v=office.15)
ms:contentKeyID: 48545585
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6961cb1de192e480ca68d9688105600ac85c69c9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874220"
---
# <a name="getobjectowner-method-adox"></a><span data-ttu-id="38c4a-102">GetObjectOwner (método, ADOX)</span><span class="sxs-lookup"><span data-stu-id="38c4a-102">GetObjectOwner Method (ADOX)</span></span>


<span data-ttu-id="38c4a-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="38c4a-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="38c4a-104">Devuelve el propietario de un objeto de un [catálogo](catalog-object-adox.md).</span><span class="sxs-lookup"><span data-stu-id="38c4a-104">Returns the owner of an object in a [Catalog](catalog-object-adox.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="38c4a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="38c4a-105">Syntax</span></span>

<span data-ttu-id="38c4a-106">*Propietario* = *catálogo*. GetObjectOwner (*ObjectName*, *ObjectType* \[,*valor de ObjectTypeId*\])</span><span class="sxs-lookup"><span data-stu-id="38c4a-106">*Owner* = *Catalog*.GetObjectOwner(*ObjectName*, *ObjectType* \[,*ObjectTypeId*\])</span></span>

## <a name="return-value"></a><span data-ttu-id="38c4a-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="38c4a-107">Return value</span></span>

<span data-ttu-id="38c4a-108">Devuelve un valor **String** que especifica el [nombre](name-property-adox.md) del [usuario](user-object-adox.md) o el [grupo](group-object-adox.md) propietario del objeto.</span><span class="sxs-lookup"><span data-stu-id="38c4a-108">Returns a **String** value that specifies the [Name](name-property-adox.md) of the [User](user-object-adox.md) or [Group](group-object-adox.md) that owns the object.</span></span>

## <a name="parameters"></a><span data-ttu-id="38c4a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="38c4a-109">Parameters</span></span>

  - <span data-ttu-id="38c4a-110">*ObjectName*</span><span class="sxs-lookup"><span data-stu-id="38c4a-110">*ObjectName*</span></span>

  - <span data-ttu-id="38c4a-111">Un valor **String** que especifica el nombre del objeto cuyo propietario se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="38c4a-111">A **String** value that specifies the name of the object for which to return the owner.</span></span>

  - <span data-ttu-id="38c4a-112">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="38c4a-112">*ObjectType*</span></span>

  - <span data-ttu-id="38c4a-113">Un valor **Long** que puede ser una de las constantes [ObjectTypeEnum](objecttypeenum.md), que especifica el tipo de objeto cuyo propietario se va a obtener.</span><span class="sxs-lookup"><span data-stu-id="38c4a-113">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get the owner.</span></span>

  - <span data-ttu-id="38c4a-114">*Valor de ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="38c4a-114">*ObjectTypeId*</span></span>

  - <span data-ttu-id="38c4a-115">Opcional.</span><span class="sxs-lookup"><span data-stu-id="38c4a-115">Optional.</span></span> <span data-ttu-id="38c4a-116">Un valor **Variant** que especifica el GUID correspondiente a un tipo de objeto de proveedor no definido en la especificación de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="38c4a-116">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="38c4a-117">Este parámetro es necesario si *ObjectType* se ha establecido en **adPermObjProviderSpecific**; de lo contrario, no se usa.</span><span class="sxs-lookup"><span data-stu-id="38c4a-117">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="38c4a-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="38c4a-118">Remarks</span></span>

<span data-ttu-id="38c4a-119">Si el proveedor no admite la devolución de propietarios de objetos, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="38c4a-119">An error will occur if the provider does not support returning object owners.</span></span>

