---
title: GetObjectOwner (método, ADOX)
TOCTitle: GetObjectOwner method (ADOX)
ms:assetid: 716dd49a-8663-3f7a-32a3-0be353aea506
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249451(v=office.15)
ms:contentKeyID: 48545585
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b1a37b0f341c849358b649c2222df2955fd88f5d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927824"
---
# <a name="getobjectowner-method-adox"></a>GetObjectOwner (método, ADOX)


**Se aplica a**: Access 2013, Office 2013


Devuelve el propietario de un objeto de un [catálogo](catalog-object-adox.md).

## <a name="syntax"></a>Sintaxis

*Propietario* = *catálogo*. GetObjectOwner (*ObjectName*, *ObjectType* \[,*valor de ObjectTypeId*\])

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **String** que especifica el [nombre](name-property-adox.md) del [usuario](user-object-adox.md) o el [grupo](group-object-adox.md) propietario del objeto.

## <a name="parameters"></a>Parámetros

  - *ObjectName*

  - Un valor **String** que especifica el nombre del objeto cuyo propietario se va a devolver.

  - *ObjectType*

  - Un valor **Long** que puede ser una de las constantes [ObjectTypeEnum](objecttypeenum.md), que especifica el tipo de objeto cuyo propietario se va a obtener.

  - *Valor de ObjectTypeId*

  - Opcional. Un valor **Variant** que especifica el GUID correspondiente a un tipo de objeto de proveedor no definido en la especificación de OLE DB. Este parámetro es necesario si *ObjectType* se ha establecido en **adPermObjProviderSpecific**; de lo contrario, no se usa.

## <a name="remarks"></a>Comentarios

Si el proveedor no admite la devolución de propietarios de objetos, se producirá un error.

