---
title: 'Capítulo 9: Crear formas de datos'
TOCTitle: 'Chapter 9: Data shaping'
ms:assetid: f66a319f-1b3d-c4a3-50b3-af1a47540832
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250253(v=office.15)
ms:contentKeyID: 48548739
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 43ad9d5e989bc1c6f4a54fb4882cfe3c3e357fd1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721557"
---
# <a name="chapter-9-data-shaping"></a>Capítulo 9: Crear formas de datos

**Se aplica a**: Access 2013, Office 2013

*Forma de datos* proporciona una forma de consultar un origen de datos y devolver un [objeto Recordset](recordset-object-ado.md) que representa una relación de elementos primarios y secundarios entre dos o más entidades lógicas (una jerarquía). 

Un ejemplo clásico de una relación jerárquica es customers y orders. Para cada cliente en una base de datos, puede ser cero o más pedidos. Regular SQL proporciona un medio de recuperar los datos mediante la sintaxis JOIN, pero esto puede ser ineficaz y poco flexible porque los datos primarios redundantes se repiten en cada registro devuelto para una relación de elementos primarios y secundarios determinado. Forma de datos puede estar relacionado con un solo registro primario del **objeto Recordset** primario con varios registros secundarios en el **conjunto de registros**, evitando la redundancia de una combinación secundario. La mayoría de las personas encontrar a los elementos primarios y secundarios modelo de programación de **Recordset** más natural y más sencillo trabajar con que el modelo de **conjunto de registros de** combinación solo.

La sintaxis de la forma de datos también proporciona otras funciones. Los programadores pueden crear nuevos objetos **Recordset** sin origen de datos subyacente mediante la palabra clave NEW para describir los campos de los objetos **Recordset** primarios y secundarios. El nuevo objeto **Recordset** se puede rellenar con datos y almacenar de manera permanente. Los programadores también pueden realizar varios cálculos o agregaciones (por ejemplo, SUMA, MEDIA y MAX) en los campos secundarios. Además, la forma de datos puede crear un objeto **Recordset** primario a partir de un objeto **Recordset** secundario agrupando los registros en el objeto secundario y colocando una fila en el objeto primario por cada grupo en el objeto secundario.

Vea los temas siguientes para obtener más información sobre la forma de datos:

- [Proveedores necesarios para la creación de formas de datos](required-providers-for-data-shaping.md)
- [Cláusula de forma Compute](shape-compute-clause.md)
- [Fabricación de conjuntos de registros jerárquicos](fabricating-hierarchical-recordsets.md)
- [Acceso a las filas en conjuntos de registros jerárquicos](accessing-rows-in-a-hierarchical-recordset.md)
- [Gramática de las formas formales](formal-shape-grammar.md)
- [Funciones de Visual Basic para Aplicaciones](visual-basic-for-applications-functions.md)
- [Cláusula Append de forma (ADO)](shape-append-clause.md)
- [Forma (ADO) de datos](data-shaping.md)
- [En general de forma comandos (ADO)](shape-commands-in-general.md)

