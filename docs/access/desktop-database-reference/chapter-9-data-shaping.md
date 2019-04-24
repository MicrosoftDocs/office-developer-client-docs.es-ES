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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296426"
---
# <a name="chapter-9-data-shaping"></a>Capítulo 9: Crear formas de datos

**Se aplica a:** Access 2013, Office 2013

La *Forma de datos* permite consultar un origen de datos y devolver un objeto [Recordset](recordset-object-ado.md) que representa una relación de objeto primario-objeto secundario entre dos o más entidades lógicas (una jerarquía). 

Un ejemplo clásico de una relación jerárquica es la de clientes y pedidos. For every customer in a database, there can be zero or more orders. Regular SQL provides a means of retrieving the data using JOIN syntax, but this can be inefficient and unwieldy because redundant parent data is repeated in each record returned for a given parent-child relationship. Data shaping can relate a single parent record in the parent **Recordset** to multiple child records in the child **Recordset**, avoiding the redundancy of a JOIN. Most people find the parent-child multiple **Recordset** programming model more natural and easier to work with than the single **Recordset** JOIN model.

La sintaxis de la forma de datos también proporciona otras funciones. Los programadores pueden crear nuevos objetos **Recordset** sin origen de datos subyacente mediante la palabra clave NEW para describir los campos de los objetos **Recordset** primarios y secundarios. El nuevo objeto **Recordset** se puede rellenar con datos y almacenar de manera permanente. Los programadores también pueden realizar varios cálculos o agregaciones (por ejemplo, SUMA, MEDIA y MAX) en los campos secundarios. Además, la forma de datos puede crear un objeto **Recordset** primario a partir de un objeto **Recordset** secundario agrupando los registros en el objeto secundario y colocando una fila en el objeto primario por cada grupo en el objeto secundario.

Vea los temas siguientes para obtener más información sobre la forma de datos:

- [Proveedores necesarios para la creación de formas de datos](required-providers-for-data-shaping.md)
- [Cláusula de forma Compute](shape-compute-clause.md)
- [Fabricación de conjuntos de registros jerárquicos](fabricating-hierarchical-recordsets.md)
- [Acceso a las filas en conjuntos de registros jerárquicos](accessing-rows-in-a-hierarchical-recordset.md)
- [Gramática de las formas formales](formal-shape-grammar.md)
- [Funciones de Visual Basic para Aplicaciones](visual-basic-for-applications-functions.md)
- [Shape Append (cláusula, ADO)](shape-append-clause.md)
- [Forma de datos (ADO)](data-shaping.md)
- [Comandos de forma en general (ADO)](shape-commands-in-general.md)

