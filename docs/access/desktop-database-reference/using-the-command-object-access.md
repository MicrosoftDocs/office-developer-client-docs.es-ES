---
title: Using the Command Object (Access)
TOCTitle: Using the Command Object
ms:assetid: dab6f0dd-1efa-3a5c-b192-c6d6afcaabfb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250102(v=office.15)
ms:contentKeyID: 48548088
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1779f2c7e16e2f39a3912f271296c6a7bd0fd550
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861949"
---
# <a name="using-the-command-object-access"></a>Using the Command Object (Access)


**Se aplica a**: Access 2013 | Office 2013

Después de conectar con un origen de datos, debe ejecutar peticiones en él para obtener conjuntos de resultados. ADO encapsula este tipo de funcionalidad de comando en el objeto **Command**.

Puede usar el objeto **Command** para solicitar cualquier tipo de operación del proveedor, suponiendo que éste pueda interpretar correctamente la cadena del comando. Una operación común para los proveedores de datos es la de consultar una base de datos y devolver registros en un objeto **Recordset**. Los objetos **Recordset** se tratarán más adelante en éste y otros capítulos; por ahora, considérelos como herramientas para contener y ver conjuntos de resultados. Al igual que ocurre con muchos objetos ADO, según la funcionalidad del proveedor, algunas colecciones de objetos **Command**, métodos o propiedades podrían generar errores al hacer referencia a ellos.

No siempre es necesario crear un objeto **Command** para ejecutar un comando en un origen de datos. Puede utilizar el método **Execute** en el objeto **Connection** o el método **Open** en el objeto **Recordset**. Sin embargo, debe usar un objeto **Command** si necesita volver a usar un comando en el código o si debe pasar información detallada de parámetros con el comando. Estos escenarios se describen con más detalle posteriormente en este capítulo.

> [!NOTE]
> Determinados comandos pueden devolver un resultado de establecer como una secuencia binaria o un único registro, en lugar de un objeto Recordset, si esto es compatible con el proveedor. Además, algunos comandos no están diseñados para devolver cualquier conjunto en absoluto de resultados (por ejemplo, una consulta SQL Update). Este capítulo tratará el escenario más típico: ejecutar comandos que devuelven resultados en un objeto Recordset. Para obtener más información sobre cómo devolver los resultados en secuencias o de registros, vea [capítulo 10: objetos Record y Stream](chapter-10-records-and-streams.md).

Esta sección incluye los temas siguientes:

- [Información general del objeto Command](command-object-overview.md)

- [Creación y ejecución de un comando simple](creating-and-executing-a-simple-command.md)

- [Parámetros del objeto Command](command-object-parameters.md)

- [Llamada a un procedimiento almacenado con un comando](calling-a-stored-procedure-with-a-command.md)

- [Comandos con nombre](named-commands.md)
