---
title: Append (método, grupos ADOX)
TOCTitle: Append Method (ADOX Groups)
ms:assetid: c3245a24-55b8-3f3f-1c4a-43a119d84dc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249954(v=office.15)
ms:contentKeyID: 48547567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f08b1bdbde8cc276e94947c2bd62250320f646c5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888590"
---
# <a name="append-method-adox-groups"></a>Append (método, grupos ADOX)


**Se aplica a**: Access 2013, Office 2013



Agrega un nuevo objeto [Group](group-object-adox.md) a la colección [Groups](groups-collection-adox.md).

## <a name="syntax"></a>Sintaxis

*Grupos*. Anexe el*grupo*

## <a name="parameters"></a>Parámetros

  - *Group*

  - El objeto **Group** que se anexará o el nombre del grupo que se creará y anexará.

## <a name="remarks"></a>Comentarios

La colección **Groups** de un [catálogo](catalog-object-adox.md) representa todas las cuentas de grupo del catálogo. La colección **Groups** para un [usuario](user-object-adox.md) representa sólo el grupo al que pertenece el usuario.

Si el proveedor no admite la creación de grupos, se producirá un error.


> [!NOTE]
> [!NOTA] Para poder anexar un objeto **Group** a la colección **Groups** de un objeto **User**, debe existir previamente un objeto **Group** con el mismo [nombre](name-property-adox.md) que el que se va a anexar en la colección **Groups** del **catálogo**.


