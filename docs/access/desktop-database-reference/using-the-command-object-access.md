---
title: Uso del objeto Command (Access)
TOCTitle: Using the Command Object
ms:assetid: dab6f0dd-1efa-3a5c-b192-c6d6afcaabfb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250102(v=office.15)
ms:contentKeyID: 48548088
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b89d292d86035e565ad18413062274dfbfc74db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312029"
---
# <a name="using-the-command-object-access"></a>Uso del objeto Command (Access)


**Se aplica a:** Access 2013, Office 2013

Después de conectar con un origen de datos, debe ejecutar peticiones en él para obtener conjuntos de resultados. ADO encapsula este tipo de funcionalidad de comando en el objeto **Command**.

Puede usar el objeto **Command** para solicitar cualquier tipo de operación del proveedor, suponiendo que éste pueda interpretar correctamente la cadena del comando. Una operación común para los proveedores de datos es la de consultar una base de datos y devolver registros en un objeto **Recordset**. Los objetos **Recordset** se tratarán más adelante en éste y otros capítulos; por ahora, considérelos como herramientas para contener y ver conjuntos de resultados. Al igual que ocurre con muchos objetos ADO, según la funcionalidad del proveedor, algunas colecciones de objetos **Command**, métodos o propiedades podrían generar errores al hacer referencia a ellos.

No siempre es necesario crear un objeto **Command** para ejecutar un comando en un origen de datos. Puede utilizar el método **Execute** en el objeto **Connection** o el método **Open** en el objeto **Recordset**. Sin embargo, debe usar un objeto **Command** si necesita volver a usar un comando en el código o si debe pasar información detallada de parámetros con el comando. Estos escenarios se describen con más detalle posteriormente en este capítulo.

> [!NOTE]
> Algunos objetos Command pueden devolver un conjunto de resultados como una secuencia binaria o un único registro, en vez de un objeto Recordset, si el proveedor admite esa posibilidad. Además, algunos objetos Command no devuelven ningún conjunto de resultados (por ejemplo, una consulta Update de SQL). Este capítulo tratará el escenario más típico: ejecutar objetos Command que devuelven resultados en un objeto Recordset. Para obtener más información acerca de los resultados devueltos en objetos Record o Stream, vea [Capítulo 10: Objetos Record y Stream](chapter-10-records-and-streams.md).

Esta sección incluye los siguientes temas:

- [Información general sobre el objeto Command](command-object-overview.md)
- [Crear y ejecutar un comando sencillo](creating-and-executing-a-simple-command.md)
- [Parámetros del objeto Command](command-object-parameters.md)
- [Llamar a un procedimiento almacenado con un comando](calling-a-stored-procedure-with-a-command.md)
- [Comandos con nombre](named-commands.md)
