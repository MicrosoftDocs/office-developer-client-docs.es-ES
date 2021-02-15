---
title: Propiedad DateModified (ADOX)
TOCTitle: DateModified property (ADOX)
ms:assetid: aebe8818-82e7-84a4-24d7-d97afa32e193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249827(v=office.15)
ms:contentKeyID: 48547078
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: daf72804d51c18b5875e607ce5fdb0dfe20f406c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294410"
---
# <a name="datemodified-property-adox"></a>Propiedad DateModified (ADOX)


**Se aplica a:** Access 2013, Office 2013

Indica la fecha en la que se modificó el objeto por última vez.

## <a name="return-values"></a>Valores devueltos

Devuelve un valor **Variant** que especifica la fecha de modificación. El valor es nulo si **DateModified** no es compatible con el proveedor.

## <a name="remarks"></a>Comentarios

La propiedad **DateModified** tiene un valor nulo para objetos recién anexados. Después de anexar una nueva [vista](view-object-adox.md) o un [procedimiento](procedure-object-adox.md), debe llamar al método [Refresh](refresh-method-ado.md) de la colección [Views](views-collection-adox.md) o [Procedures](procedures-collection-adox.md) para obtener valores para la propiedad **DateModified**.

