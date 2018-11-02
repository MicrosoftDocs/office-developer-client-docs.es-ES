---
title: SetPermissions (método, ADOX)
TOCTitle: SetPermissions method (ADOX)
ms:assetid: 63d1053d-fb32-456b-ae67-3a4e45aa01af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249382(v=office.15)
ms:contentKeyID: 48545274
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6d99608a938598135d713375875da9073c8f9f3c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927518"
---
# <a name="setpermissions-method-adox"></a>SetPermissions (método, ADOX)


**Se aplica a**: Access 2013, Office 2013



Especifica los permisos para un grupo o un usuario en un objeto.

## <a name="syntax"></a>Sintaxis

*Grupo_o_usuario*. SetPermissions*nombre*, *ObjectType*, *acción*, *derechos* \[,*heredar* \] \[,*valor de ObjectTypeId*\]

## <a name="parameters"></a>Parámetros

  - *Name*

  - Un valor **String** que especifica el nombre del objeto para el que se van a establecer permisos.

  - *ObjectType*

  - Un valor **Long** que puede ser una de las constantes [ObjectTypeEnum](objecttypeenum.md), que especifica el tipo de objeto para el que se van a obtener permisos.

  - *Action*

  - Un valor **Long** que puede ser una de las constantes [ActionEnum](actionenum.md), que especifica el tipo de acción que se realizará cuando se establezcan permisos.

  - *Rights*

  - Un valor **Long** que puede ser una máscara de bits de una o varias de las constantes [RightsEnum](rightsenum.md), que indica los derechos a establecer.

  - *Inherit*

  - Opcional. Un valor **Long** que puede ser una de las constantes [InheritTypeEnum](inherittypeenum.md), que especifica cómo heredarán estos permisos los objetos. El valor predeterminado es **adInheritNone**.

  - *Valor de ObjectTypeId*

  - Opcional. Un valor **Variant** que especifica el GUID correspondiente a un tipo de objeto de proveedor no definido en la especificación de OLE DB. Este parámetro es necesario si *ObjectType* se ha establecido en **adPermObjProviderSpecific**; de lo contrario, no se usa.

## <a name="remarks"></a>Comentarios

Si el proveedor no admite el establecimiento de derechos de acceso para grupos o usuarios, se producirá un error.


> [!NOTE]
> <P>Cuando se llama a <STRONG>SetPermissions</STRONG>, establecimiento de Action en <STRONG>adAccessRevoke</STRONG> anula los valores del parámetro <EM>Rights</EM> . No establezca <EM>acciones</EM> en <STRONG>adAccessRevoke</STRONG> si desea que los derechos especificados en el parámetro <EM>Rights</EM> surta efecto.</P>


