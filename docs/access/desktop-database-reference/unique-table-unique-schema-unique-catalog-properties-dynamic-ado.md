---
title: Propiedades dinámicas Unique Table, Unique Schema y Unique Catalog (ADO)
TOCTitle: Unique Table, Unique Schema, Unique Catalog dynamic properties (ADO)
ms:assetid: e6374782-755b-322b-21de-6d6a386dcd98
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250169(v=office.15)
ms:contentKeyID: 48548374
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5f4bf93afc200edd88e89cf5d4e90435c2476942
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313751"
---
# <a name="unique-table-unique-schema-unique-catalog-dynamic-properties-ado"></a>Propiedades dinámicas Unique Table, Unique Schema y Unique Catalog (ADO)


**Se aplica a:** Access 2013, Office 2013

Permiten controlar estrechamente las modificaciones realizadas en una tabla base concreta de un objeto [Recordset](recordset-object-ado.md) formado mediante una operación JOIN en varias tablas base.

  - **Unique Table** especifica el nombre de la tabla base en la que se permiten actualizaciones, inserciones y eliminaciones.

  - **Unique Schema** especifica el *esquema* o el nombre del propietario de la tabla.

  - **Unique Catalog** especifica el *catálogo* o el nombre de la base de datos que contiene la tabla.

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establecen o devuelven un valor de tipo **String** que es el nombre de una tabla, un esquema o un catálogo.

## <a name="remarks"></a>Comentarios

La tabla base deseada es identificada de forma exclusiva por el nombre de catálogo, esquema y tabla. Cuando se establece la propiedad **Unique Table**, los valores de las propiedades **Unique Schema** o **Unique Catalog** se utilizan para buscar la tabla base. Se recomienda, aunque no es obligatorio, que alguna de las propiedades **Unique Schema** y **Unique Catalog** o ambas se establezcan antes de establecer la propiedad **Unique Table**.

La clave principal de **Unique Table** se trata como la clave principal de todo el objeto **Recordset**. Esta es la clave que se usa con cualquier método que exija una clave principal.

Mientras se establece **Unique Table**, el método [Delete](delete-method-ado-recordset.md) sólo afecta a la tabla con nombre. Los métodos [AddNew](addnew-method-ado.md), [Resync](resync-method-ado.md), [Update](update-method-ado.md) y [UpdateBatch](updatebatch-method-ado.md) afectan a cualquier tabla base subyacente de **Recordset**.

**Unique Table** debe especificarse antes de volver a realizar cualquier sincronización personalizada. Si **Unique Table** no se ha especificado, la propiedad [Resync Command](resync-command-property-dynamic-ado.md) no tendrá ningún efecto.

Si no se puede encontrar una tabla base exclusiva, se produce un error en tiempo de ejecución.

Todas estas propiedades dinámicas se anexan a la colección **Properties** del objeto [Recordset](properties-collection-ado.md) cuando la propiedad [CursorLocation](cursorlocation-property-ado.md) está establecida en **adUseClient**.

