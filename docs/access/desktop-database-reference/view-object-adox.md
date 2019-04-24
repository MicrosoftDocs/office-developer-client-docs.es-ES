---
title: View (objeto) (referencia de base de datos de escritorio de Access de ADOX)
TOCTitle: View object (ADOX)
ms:assetid: 3b2e9972-8a0d-eaa3-1c93-ae0665a47f02
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249149(v=office.15)
ms:contentKeyID: 48544280
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b3b5d25a727233b5fda5627df8dff952003bbfe3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306054"
---
# <a name="view-object-adox"></a>View (objeto) (ADOX)


**Se aplica a:** Access 2013, Office 2013

Representa un conjunto filtrado de registros o una tabla virtual. Cuando se utiliza junto con el objeto [Command](command-object-ado.md) de ADO, se puede usar el objeto **View** para agregar, eliminar o modificar vistas.

## <a name="remarks"></a>Comentarios

Una vista es una tabla virtual creada desde otras tablas de base de datos o vistas. El objeto **View** permite crear una vista sin necesidad de conocer ni utilizar la sintaxis "CREATE VIEW" del proveedor.

Con las propiedades de un objeto **View**, se puede:

  - Identificar la vista con la propiedad [Name](name-property-adox.md).

  - Especificar el objeto **Command** de ADO que se puede utilizar para agregar, eliminar o modificar vistas con la propiedad [Command](command-property-adox.md).

  - Devolver información de fecha con las propiedades [DateCreated](datecreated-property-adox.md) y [DateModified](datemodified-property-adox.md).

