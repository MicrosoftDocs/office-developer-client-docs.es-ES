---
title: DateModified (propiedad, ADOX)
TOCTitle: DateModified Property (ADOX)
ms:assetid: aebe8818-82e7-84a4-24d7-d97afa32e193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249827(v=office.15)
ms:contentKeyID: 48547078
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8465f97565d8519196b8221089121670ceedb275
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483663"
---
# <a name="datemodified-property-adox"></a>DateModified (propiedad, ADOX)


**Se aplica a**: Access 2013 | Office 2013

Indica la fecha en la que se modificó el objeto por última vez.

## <a name="return-values"></a>Valores devueltos

Devuelve un valor **Variant** que especifica la fecha de modificación. El valor es nulo si **DateModified** no es compatible con el proveedor.

## <a name="remarks"></a>Comentarios

La propiedad **DateModified** tiene un valor nulo para objetos recién anexados. Después de anexar una nueva [vista](view-object-adox.md) o un [procedimiento](procedure-object-adox.md), debe llamar al método [Refresh](refresh-method-ado.md) de la colección [Views](views-collection-adox.md) o [Procedures](procedures-collection-adox.md) para obtener valores para la propiedad **DateModified**.

