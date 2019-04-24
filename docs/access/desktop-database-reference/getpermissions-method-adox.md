---
title: GetPermissions (método, ADOX)
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
# <a name="getpermissions-method-adox"></a>GetPermissions (método, ADOX)

**Se aplica a:** Access 2013, Office 2013

Devuelve los permisos para un grupo o un usuario en un objeto o un contenedor de objeto.

## <a name="syntax"></a>Sintaxis

*ReturnValue* = *GroupOrUser*. GetPermissions (*Name*, *objecttype* \[,*ObjectTypeId*\])

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **Long** que especifica una máscara de bits que contiene los permisos del grupo o del usuario en el objeto. Este valor puede ser una o varias de las constantes [RightsEnum](rightsenum.md).

## <a name="parameters"></a>Parámetros

|Parameter|Descripción|
|:--------|:----------|
|*Name* |Un valor **Variant** que especifica el nombre del objeto para el que se van a establecer permisos. Establezca *Name* en un valor nulo si desea obtener los permisos para el contenedor de objeto.|
|*ObjectType* |Un valor **Long** que puede ser una de las constantes [ObjectTypeEnum](objecttypeenum.md), que especifica el tipo de objeto para el que se van a obtener permisos.|
|*ObjectTypeId* |Opcional. Un valor **Variant** que especifica el GUID correspondiente a un tipo de objeto de proveedor no definido en la especificación de OLE DB. Este parámetro es necesario si *ObjectType* se ha establecido en **adPermObjProviderSpecific**; de lo contrario, no se utiliza.|

