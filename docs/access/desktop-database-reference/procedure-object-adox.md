---
title: Procedure (objeto) (ADOX)
TOCTitle: Procedure Object (ADOX)
ms:assetid: d5fcf0fe-f59f-e114-dc11-515f11c2a2c1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250076(v=office.15)
ms:contentKeyID: 48547972
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5363bd435a4950b833e110fdda4f14a9c1bc2bc2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486567"
---
# <a name="procedure-object-adox"></a>Procedure (objeto) (ADOX)


**Se aplica a**: Access 2013 | Office 2013

Representa un procedimiento almacenado. Cuando se usa junto con el objeto [Command](command-object-ado.md) de ADO, se puede usar el objeto **Procedure** para agregar, eliminar o modificar procedimientos almacenados.

## <a name="remarks"></a>Comentarios

El objeto **Procedure** permite crear un procedimiento almacenado sin necesidad de conocer ni utilizar la sintaxis "CREATE PROCEDURE" del proveedor.

Con las propiedades de un objeto **Procedure**, se puede:

  - Identificar el procedimiento con la propiedad [Name](name-property-adox.md).

  - Especificar el objeto **Command** de ADO que se puede utilizar para crear o ejecutar el procedimiento con la propiedad [Command](command-property-adox.md).

  - Devolver información de fecha con las propiedades [DateCreated](datecreated-property-adox.md) y [DateModified](datemodified-property-adox.md).

