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
# <a name="setpermissions-method-adox"></a>Método SetPermissions (ADOX)

**Se aplica a:** Access 2013, Office 2013

Especifica los permisos para un grupo o un usuario en un objeto.

## <a name="syntax"></a>Sintaxis

*GroupOrUser*. SetPermissions *Name*, *ObjectType*, *Action*, *Rights* \[ ,*Inherit* \] \[ ,*ObjectTypeId*\]

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*Name* |Un valor **String** que especifica el nombre del objeto para el que se van a establecer permisos.|
|*ObjectType* |Un valor **Long** que puede ser una de las constantes [ObjectTypeEnum](objecttypeenum.md), que especifica el tipo de objeto para el que se van a obtener permisos.|
|*Action* |Un valor **Long** que puede ser una de las constantes [ActionEnum](actionenum.md), que especifica el tipo de acción que se realizará cuando se establezcan permisos.|
|*Rights* |Un valor **Long** que puede ser una máscara de bits de una o varias de las constantes [RightsEnum](rightsenum.md), que indica los derechos a establecer.|
|*Inherit* |Opcional. Un valor **Long** que puede ser una de las constantes [InheritTypeEnum](inherittypeenum.md), que especifica cómo heredarán estos permisos los objetos. El valor predeterminado es **adInheritNone**.|
|*ObjectTypeId* |Opcional. Un valor **Variant** que especifica el GUID correspondiente a un tipo de objeto de proveedor no definido en la especificación de OLE DB. Este parámetro es necesario si *ObjectType* se ha establecido en **adPermObjProviderSpecific**; de lo contrario, no se utiliza.|

## <a name="remarks"></a>Comentarios

Si el proveedor no admite el establecimiento de derechos de acceso para grupos o usuarios, se producirá un error.

> [!NOTE]
> Cuando se llama a **SetPermissions**, el establecimiento de Action en **adAccessRevoke** anula los valores del parámetro *Rights*. No establezca *Action* en **adAccessRevoke** si desea que los derechos especificados en el parámetro *Rights* sean efectivos.


