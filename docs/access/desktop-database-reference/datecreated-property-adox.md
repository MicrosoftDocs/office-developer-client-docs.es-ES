---
title: DateCreated (propiedad, ADOX)
TOCTitle: DateCreated Property (ADOX)
ms:assetid: ee975bf5-7d44-a993-d1c0-077993515698
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250209(v=office.15)
ms:contentKeyID: 48548564
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fea3e83f9a171a95eb844d9ba721039969804acf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876473"
---
# <a name="datecreated-property-adox"></a>DateCreated (propiedad, ADOX)


**Se aplica a**: Access 2013, Office 2013

Indica la fecha en la que se creó el objeto.

## <a name="return-values"></a>Valores devueltos

Devuelve un valor **Variant** que especifica la fecha de creación. El valor es nulo si **DateCreated** no es compatible con el proveedor.

## <a name="remarks"></a>Comentarios

La propiedad **DateCreated** tiene un valor nulo para objetos recién anexados. Después de anexar una nueva [vista](view-object-adox.md) o un [procedimiento](procedure-object-adox.md), debe llamar al método [Refresh](refresh-method-ado.md) de la colección [Views](views-collection-adox.md) o [Procedures](procedures-collection-adox.md) para obtener valores para la propiedad **DateCreated**.

