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
# <a name="getpermissions-method-adox"></a>GetPermissions (método, ADOX)


**Se aplica a**: Access 2013, Office 2013


Devuelve los permisos para un grupo o un usuario en un objeto o un contenedor de objeto.

## <a name="syntax"></a>Sintaxis

*ReturnValue* = *Grupo_o_usuario*. GetPermissions (*nombre*, *ObjectType* \[,*valor de ObjectTypeId*\])

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **Long** que especifica una máscara de bits que contiene los permisos del grupo o del usuario en el objeto. Este valor puede ser una o varias de las constantes [RightsEnum](rightsenum.md).

## <a name="parameters"></a>Parámetros

  - *Name*

  - Un valor **Variant** que especifica el nombre del objeto para el que se van a establecer permisos. *Nombre* del conjunto en un valor nulo si desea obtener los permisos para el contenedor de objetos.

  - *ObjectType*

  - Un valor **Long** que puede ser una de las constantes [ObjectTypeEnum](objecttypeenum.md), que especifica el tipo de objeto para el que se van a obtener permisos.

  - *Valor de ObjectTypeId*

  - Opcional. Un valor **Variant** que especifica el GUID correspondiente a un tipo de objeto de proveedor no definido en la especificación de OLE DB. Este parámetro es necesario si *ObjectType* se ha establecido en **adPermObjProviderSpecific**; de lo contrario, no se usa.

