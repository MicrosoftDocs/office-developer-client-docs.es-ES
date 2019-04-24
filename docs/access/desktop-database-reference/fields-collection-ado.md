---
title: Fields (colección) (ADO)
TOCTitle: Fields collection (ADO)
ms:assetid: 029aa738-8726-54a6-1813-b152813948bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248791(v=office.15)
ms:contentKeyID: 48542962
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a537756483361733c087d5dc1c6bba6e649d17d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292576"
---
# <a name="fields-collection-ado"></a>Fields (colección) (ADO)


**Se aplica a:** Access 2013, Office 2013

Contiene todos los objetos [Field](field-object-ado.md) de un objeto [Recordset](recordset-object-ado.md) o [Record](record-object-ado.md).

## <a name="remarks"></a>Comentarios

Los objetos **Recordset** tienen una colección **Fields** formada por objetos **Field**. Cada objeto **Field** corresponde a una columna del objeto **Recordset**. Puede rellenar la colección **Fields** antes de abrir el objeto **Recordset** llamando al método [Refresh](refresh-method-ado.md) en la colección.

> [!NOTE]
> [!NOTA] Para obtener una explicación más detallada sobre cómo se usan los objetos **Field**, vea el tema sobre el objeto **Field**.

La colección **Fields** tiene un método [Append](append-method-ado.md) que, provisionalmente, crea y agrega un objeto **Field** a la colección, y un método **Update** que finaliza las incorporaciones o eliminaciones.

Los objetos **Record** tienen dos campos especiales que se pueden indizar con constantes [FieldEnum](fieldenum.md). Una constante obtiene acceso a un campo que contiene la secuencia predeterminada correspondiente al objeto **Record**, y la otra obtiene acceso a un campo que contiene la cadena de la dirección URL absoluta correspondiente al objeto **Record**.

Algunos proveedores (por ejemplo, [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)) pueden rellenar la colección **Fields** con un subconjunto de campos disponibles correspondientes al objeto **Record** o **Recordset**. No se agregarán otros campos a la colección hasta que se haga referencia a ellos por su nombre o sean indizados por el código.

Si se intenta hacer referencia a un campo no existente por su nombre, se anexará un nuevo objeto **Field** a la colección **Fields** con un [Status](status-property-ado-field.md) de **adFieldPendingInsert**. Cuando se llame a [Update](update-method-ado.md), ADO creará un nuevo campo en el origen de datos si lo permite el proveedor.

