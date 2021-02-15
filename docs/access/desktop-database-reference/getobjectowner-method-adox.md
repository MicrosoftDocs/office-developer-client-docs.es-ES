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
# <a name="getobjectowner-method-adox"></a>Método GetObjectOwner (ADOX)

**Se aplica a:** Access 2013, Office 2013

Devuelve el propietario de un objeto de un [catálogo](catalog-object-adox.md).

## <a name="syntax"></a>Sintaxis

*Propietario*  =  *Catálogo*. GetObjectOwner(*ObjectName*, *ObjectType* \[ ,*ObjectTypeId* \] )

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **String** que especifica el [nombre](name-property-adox.md) del [usuario](user-object-adox.md) o el [grupo](group-object-adox.md) propietario del objeto.

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*ObjectName* |Un valor **String** que especifica el nombre del objeto cuyo propietario se va a devolver.|
|*ObjectType* |Un valor **Long** que puede ser una de las constantes [ObjectTypeEnum](objecttypeenum.md), que especifica el tipo de objeto cuyo propietario se va a obtener.|
|*ObjectTypeId* |Opcional. Un valor **Variant** que especifica el GUID correspondiente a un tipo de objeto de proveedor no definido en la especificación de OLE DB. Este parámetro es necesario si *ObjectType* se ha establecido en **adPermObjProviderSpecific**; de lo contrario, no se utiliza.|

## <a name="remarks"></a>Comentarios

Si el proveedor no admite la devolución de propietarios de objetos, se producirá un error.

