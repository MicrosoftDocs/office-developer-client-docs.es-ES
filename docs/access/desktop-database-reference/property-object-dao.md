---
title: Objeto Property (DAO)
TOCTitle: Property Object
ms:assetid: a1ecb0db-bb93-a7b5-23c3-0b73f275dfe0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820932(v=office.15)
ms:contentKeyID: 48546744
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e26bc59221b4ff55c943b6a9a0c87ac5c0dd936b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718823"
---
# <a name="property-object-dao"></a>Objeto Property (DAO)

**Se aplica a**: Access 2013, Office 2013

Un objeto **Property** representa una característica integrada o definida por el usuario de un objeto DAO.

## <a name="remarks"></a>Observaciones

Todos los objetos DAO excepto los objetos **Connection** y **Error** contienen una colección **Properties** que tiene objetos **Property** correspondientes a propiedades integradas de dicho objeto DAO. Además, el usuario puede definir objetos **Property** y anexarlos a la colección **Properties** de ciertos objetos DAO. Estos objetos **Property** (que suelen denominarse simplemente propiedades) caracterizan de forma exclusiva dicha instancia del objeto.

Pueden crearse propiedades definidas por el usuario para los objetos siguientes:

- Objetos **Database**, **Index**, **QueryDef** y **TableDef**

- Objetos **Field** de las colecciones **Fields** de los objetos **QueryDef** y **TableDef**

Para agregar una propiedad definida por el usuario, utilice el método **CreateProperty** para crear un objeto **Property** con un valor de la propiedad **Name** único. Establezca las propiedades **Type** y **Value** del nuevo objeto **Property** y, después, anéxelo a la colección **Properties** del objeto correspondiente. El objeto al que se agrega la propiedad definida por el usuario debe estar anexado a una colección. Si se hace referencia a un objeto **Property** definido por el usuario que no esté anexado a una colección **Properties**, se producirá un error, de la misma manera que si se anexa un objeto **Property** definido por el usuario a una colección **Properties** que contenga un objeto **Property** con el mismo nombre.

Se pueden eliminar propiedades definidas por el usuario de la colección **Properties**, pero no se pueden eliminar propiedades integradas.

> [!NOTE]
> [!NOTA] Un objeto **Property** definido por el usuario está asociado sólo con la instancia específica de un objeto. La propiedad no está definida para todas las instancias de objetos del tipo seleccionado.

La colección **Properties** de un objeto se puede usar para enumerar las propiedades integradas y definidas por el usuario del objeto. Para tratarlas, no es necesario saber de antemano qué propiedades existen exactamente o cuáles son sus características (propiedades **Name** y **Type**). Sin embargo, se producirá un error si intenta leer una propiedad de sólo escritura, como la propiedad **Password** de un objeto **Workspace** o si intenta leer o escribir en una propiedad en un contexto inadecuado, por ejemplo el valor de la propiedad **Value** de un objeto **Field** de la colección **Fields** de un objeto **TableDef**.

El objeto **Property** tiene también cuatro propiedades integradas:

- La propiedad **Name**, un valor de tipo **String** que identifica la propiedad de forma única.

- La propiedad **Type**, un valor de tipo **Integer** que especifica el tipo de datos de la propiedad.

- La propiedad **Value**, un valor de tipo **Variant** que contiene el valor de la propiedad.

- La propiedad **Inherited**, un valor de tipo **Boolean** que indica si la propiedad es heredada de otro objeto. Por ejemplo, un objeto **Field** de una colección **Fields** de un objeto **Recordset** puede heredar propiedades del objeto **TableDef** o **QueryDef** subyacentes.

Para hacer referencia a un objeto **Property** integrado de una colección por su número ordinal o por su valor de la propiedad **Name**, utilice uno de los siguientes formatos de sintaxis:

- * objeto ***. Las propiedades**(0)

- *objeto ***. Las propiedades**("* nombre *")

- *objeto ***. Propiedades**\!* nombre *\]

Para una propiedad integrada, también se puede usar la siguiente sintaxis:

- *objeto*. *nombre*

> [!NOTE]
> Para una propiedad definida por el usuario, debe usar el objeto *completa ***. Las propiedades**("* nombre *") sintaxis.

Con los mismos formatos de sintaxis, también se puede hacer referencia a la propiedad **Value** de un objeto **Property**. El contexto de la referencia determinará si se está haciendo referencia al objeto **Property** en sí o a la propiedad **Value** del objeto **Property**.

