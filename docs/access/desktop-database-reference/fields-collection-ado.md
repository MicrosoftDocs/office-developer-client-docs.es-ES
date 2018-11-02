---
title: Fields (colección, ADO)
TOCTitle: Fields collection (ADO)
ms:assetid: 029aa738-8726-54a6-1813-b152813948bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248791(v=office.15)
ms:contentKeyID: 48542962
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 27741f8b1a07e4fae49818b72a7239d13d069cca
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931207"
---
# <a name="fields-collection-ado"></a>Fields (colección, ADO)


**Se aplica a**: Access 2013, Office 2013

Contiene todos los objetos [Field](field-object-ado.md) de un objeto [Recordset](recordset-object-ado.md) o [Record](record-object-ado.md).

## <a name="remarks"></a>Comentarios

Los objetos **Recordset** tienen una colección **Fields** formada por objetos **Field**. Cada objeto **Field** corresponde a una columna del objeto **Recordset**. Puede rellenar la colección **Fields** antes de abrir el objeto **Recordset** llamando al método [Refresh](refresh-method-ado.md) en la colección.


> [!NOTE]
> <P>[!NOTA] Para obtener una explicación más detallada sobre cómo se usan los objetos <STRONG>Field</STRONG>, vea el tema sobre el objeto <STRONG>Field</STRONG>.</P>



La colección **Fields** tiene un método [Append](append-method-ado.md) que, provisionalmente, crea y agrega un objeto **Field** a la colección, y un método **Update** que finaliza las incorporaciones o eliminaciones.

Los objetos **Record** tienen dos campos especiales que se pueden indizar con constantes [FieldEnum](fieldenum.md). Una constante obtiene acceso a un campo que contiene la secuencia predeterminada correspondiente al objeto **Record**, y la otra obtiene acceso a un campo que contiene la cadena de la dirección URL absoluta correspondiente al objeto **Record**.

Algunos proveedores (por ejemplo, [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)) pueden rellenar la colección **Fields** con un subconjunto de campos disponibles correspondientes al objeto **Record** o **Recordset**. No se agregarán otros campos a la colección hasta que se haga referencia a ellos por su nombre o sean indizados por el código.

Si se intenta hacer referencia a un campo no existente por su nombre, se anexará un nuevo objeto **Field** a la colección **Fields** con un [Status](status-property-ado-field.md) de **adFieldPendingInsert**. Cuando se llame a [Update](update-method-ado.md), ADO creará un nuevo campo en el origen de datos si lo permite el proveedor.

