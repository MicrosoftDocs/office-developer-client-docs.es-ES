---
title: Value (propiedad, ADO)
TOCTitle: Value Property (ADO)
ms:assetid: ff21d122-98e3-2b48-d92f-e696b8079fc5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250310(v=office.15)
ms:contentKeyID: 48548958
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 68c0d45345dfc768f5d435689abf67bcc3d9abe2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483567"
---
# <a name="value-property-ado"></a>Value (propiedad, ADO)


**Se aplica a**: Access 2013 | Office 2013

Indica el valor asignado a un objeto [Field](field-object-ado.md), [Parameter](parameter-object-ado.md) o [Property](property-object-ado.md).

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo **Variant** que indica el valor del objeto. El valor predeterminado depende de la propiedad [Type](type-property-ado.md).

## <a name="remarks"></a>Comentarios

Utilice la propiedad **Value** para establecer o devolver datos de objetos **Field**, para establecer o devolver valores de parámetros con objetos **Parameter** o para establecer o devolver la configuración de las propiedades con objetos **Property**. El que la propiedad **Value** sea de lectura o escritura o de sólo lectura depende de varios factores; vea el tema correspondiente a cada objeto para obtener más información.

ADO permite establecer y devolver datos binarios largos con la propiedad **Value**.


> [!NOTE]
> <P>[!NOTA] En los objetos <STRONG>Parameter</STRONG>, ADO lee la propiedad <STRONG>Value</STRONG> solo una vez desde el proveedor. Si un comando incluye un objeto <STRONG>Parameter</STRONG> cuya propiedad <STRONG>Value</STRONG> está vacía y se crea un objeto <A href="recordset-object-ado.md">Recordset</A> a partir del comando, asegúrese de cerrar <STRONG>Recordset</STRONG> antes de recuperar la propiedad <STRONG>Value</STRONG>. De lo contrario, para algunos proveedores, la propiedad <STRONG>Value</STRONG> puede estar vacía y no contendrá el valor correcto.</P>



En los nuevos objetos **Field** que se han anexado a la colección [Fields](fields-collection-ado.md) de un objeto [Record](record-object-ado.md), es necesario establecer la propiedad **Value** antes de especificar cualquier otra propiedad **Field**. En primer lugar, debe haberse asignado un valor específico a la propiedad **Value** y se debe haber llamado al método [Update](update-method-ado.md) de la colección **Fields**. A continuación, será posible obtener acceso a otras propiedades como [Type](type-property-ado.md) o [Attributes](attributes-property-ado.md).

