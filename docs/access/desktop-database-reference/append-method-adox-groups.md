---
title: Append (método, Groups de ADOX)
TOCTitle: Append method (ADOX Groups)
ms:assetid: c3245a24-55b8-3f3f-1c4a-43a119d84dc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249954(v=office.15)
ms:contentKeyID: 48547567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dfc2da5490cf5c148d39670dedfb2551cedd31f2
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923591"
---
# <a name="append-method-adox-groups"></a>Append (método, Groups de ADOX)


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


