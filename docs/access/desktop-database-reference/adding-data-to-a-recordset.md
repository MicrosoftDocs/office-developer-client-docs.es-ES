---
title: Agregar datos a un conjunto de registros
TOCTitle: Adding data to a Recordset
ms:assetid: a3d121a8-f52f-66cd-8849-c3a75aeb276a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249761(v=office.15)
ms:contentKeyID: 48546797
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d16eb5871bfe55af58a89cc06b413e8404df8cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280219"
---
# <a name="adding-data-to-a-recordset"></a>Agregar datos a un conjunto de registros

**Se aplica a:** Access 2013, Office 2013

Probablemente, el objeto **Recordset** es el más usado de los objetos de ADO. En ADO, un **conjunto de registros** se entiende mejor como la combinación de un conjunto de resultados de un origen de datos y sus comportamientos de cursor asociados. Así pues, puede colocar datos en un **conjunto de registros** y luego utilizar los métodos y las propiedades del **conjunto de registros** para desplazarse por las filas de datos, ver los valores de las filas y manipular de otras maneras el conjunto de resultados.

Esta sección se centra en agregar datos al objeto **Recordset**. Para obtener información acerca de la navegación por los datos o la actualización de los datos, vea el [Capítulo 4: Modificar datos](chapter-4-editing-data.md) y el [Capítulo 5: Actualizar y almacenar datos](chapter-5-updating-and-persisting-data.md). No siempre son necesarias las características avanzadas de un objeto **Command** para agregar un conjunto de resultados a un objeto **Recordset**. A menudo, se puede ejecutar el comando si establece la propiedad **Origen** para el objeto **Recordset** o pasa una cadena de comandos al método **Open** del objeto **Recordset**.

Hay diversas formas de agregar datos a un **conjunto de registros** desde un origen de datos. La técnica que se utilice depende de las necesidades de la aplicación y de las características del proveedor.

