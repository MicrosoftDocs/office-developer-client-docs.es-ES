---
title: Datos Shaping (referencia de escritorio de la base de datos de Access)
TOCTitle: Data Shaping
ms:assetid: 650571cc-6874-2cdb-dd76-0804d1cc4e38
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249390(v=office.15)
ms:contentKeyID: 48545305
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e498bc461c2c267dee741a2bd9a4a83eacaca935
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486603"
---
# <a name="data-shaping"></a>Forma de datos


**Se aplica a**: Access 2013 | Office 2013

La aplicación de la forma a los datos permite definir las columnas de un objeto **Recordset** con forma, las relaciones entre las entidades representadas por las columnas y la forma en que se rellena el objeto **Recordset** con datos.

Las columnas de un objeto **Recordset** con forma pueden contener datos procedentes de un proveedor de datos como Microsoft SQL Server, referencias a otro **Recordset**, valores derivados de un cálculo sobre una única fila de un **Recordset** o valores derivados de una operación sobre una columna de un **Recordset** completo; también pueden ser una columna vacía recién fabricada.

Cuando se recupera el valor de una columna que contiene una referencia a otro objeto **Recordset**, ADO devuelve automáticamente el objeto **Recordset** real representado por la referencia. Un **Recordset** que contiene otro **Recordset** se denomina Recordset jerárquico. Los Recordset jerárquicos presentan una relación *principal-secundario* en la que el elemento *principal* es el Recordset contenedor, y el elemento *secundario* es el Recordset contenido. La referencia a un objeto **Recordset** es realmente una referencia a un subconjunto del elemento secundario, que se denomina *capítulo*. Un solo elemento principal puede hacer referencia a más de un objeto **Recordset** secundario.

La sintaxis de comando Shape permite crear un objeto **Recordset** modelado mediante programación. Es posible, entonces, obtener acceso a los componentes del objeto **Recordset** mediante código de programación o a través de un control visual apropiado. Un comando Shape se emite como cualquier otro texto de comando ADO.

Los objetos **Recordset** jerárquicos se pueden construir de dos formas con la sintaxis de comando Shape. La primera forma agrega un objeto **Recordset** secundario a un objeto **Recordset** principal. Ambos normalmente tienen al menos una columna en común: el valor de la columna de una fila del elemento principal es el mismo que el valor de la columna en todas las filas del elemento secundario.

La segunda forma genera un objeto **Recordset** principal a partir de un objeto **Recordset** secundario. Los registros del objeto **Recordset** secundario se agrupan, normalmente mediante la cláusula BY, y se agrega una fila al objeto **Recordset** principal para cada grupo resultante en el elemento secundario. Si se omite la cláusula BY, el objeto **Recordset** secundario formará un grupo único, y el objeto **Recordset** principal contendrá exactamente una fila. Esto es útil para calcular agregados de "total general" sobre el objeto **Recordset** secundario completo.

Independientemente de cómo se haya formado el objeto **Recordset** principal, contendrá una columna capítulo que se utiliza para relacionarlo con un objeto **Recordset** secundario. Si lo desea, el objeto **Recordset** principal puede tener también columnas que contienen agregados (SUM, MIN, MAX, etc.) sobre las filas del recordset secundario. Tanto el objeto **Recordset** principal como el secundario pueden tener columnas que contienen una expresión sobre la fila del objeto **Recordset**, así como columnas nuevas e inicialmente vacías.

Es posible anidar objetos **Recordset** jerárquicos con cualquier profundidad (es decir, crear objetos **Recordset** secundarios de objetos **Recordset** principales sucesivamente).

Puede obtener acceso, mediante código de programación o a través de un control visual apropiado, a los componentes del objeto **Recordset** del **Recordset** con forma de datos.

Para obtener ejemplos de los comandos Shape y sus jerarquías resultantes, vea Utilizar el servicio de configuración de datos para OLE DB: información detallada.

