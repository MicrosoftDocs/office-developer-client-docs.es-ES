---
title: Objeto View (ADOX - referencia de escritorio de la base de datos de Access)
TOCTitle: View Object (ADOX)
ms:assetid: 3b2e9972-8a0d-eaa3-1c93-ae0665a47f02
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249149(v=office.15)
ms:contentKeyID: 48544280
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ca58dd83ee3d3675a4ca272e1074b8d8cc930391
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486621"
---
# <a name="view-object-adox"></a>View (objeto) (ADOX)


**Se aplica a**: Access 2013 | Office 2013

Representa un conjunto filtrado de registros o una tabla virtual. Cuando se utiliza junto con el objeto [Command](command-object-ado.md) de ADO, se puede usar el objeto **View** para agregar, eliminar o modificar vistas.

## <a name="remarks"></a>Comentarios

Una vista es una tabla virtual creada desde otras tablas de base de datos o vistas. El objeto **View** permite crear una vista sin necesidad de conocer ni utilizar la sintaxis "CREATE VIEW" del proveedor.

Con las propiedades de un objeto **View**, se puede:

  - Identificar la vista con la propiedad [Name](name-property-adox.md).

  - Especificar el objeto **Command** de ADO que se puede utilizar para agregar, eliminar o modificar vistas con la propiedad [Command](command-property-adox.md).

  - Devolver información de fecha con las propiedades [DateCreated](datecreated-property-adox.md) y [DateModified](datemodified-property-adox.md).

