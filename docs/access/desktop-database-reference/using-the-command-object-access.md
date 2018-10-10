---
title: Using the Command Object (Access)
TOCTitle: Using the Command Object
ms:assetid: dab6f0dd-1efa-3a5c-b192-c6d6afcaabfb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250102(v=office.15)
ms:contentKeyID: 48548088
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 36d7bf1b39186eca841e417473e31e2bfd3a2dfc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483793"
---
# <a name="using-the-command-object-access"></a>Using the Command Object (Access)


**Se aplica a**: Access 2013 | Office 2013

Después de conectar con un origen de datos, debe ejecutar peticiones en él para obtener conjuntos de resultados. ADO encapsula este tipo de funcionalidad de comando en el objeto **Command**.

Puede usar el objeto **Command** para solicitar cualquier tipo de operación del proveedor, suponiendo que éste pueda interpretar correctamente la cadena del comando. Una operación común para los proveedores de datos es la de consultar una base de datos y devolver registros en un objeto **Recordset**. Los objetos **Recordset** se tratarán más adelante en éste y otros capítulos; por ahora, considérelos como herramientas para contener y ver conjuntos de resultados. Al igual que ocurre con muchos objetos ADO, según la funcionalidad del proveedor, algunas colecciones de objetos **Command**, métodos o propiedades podrían generar errores al hacer referencia a ellos.

No siempre es necesario crear un objeto **Command** para ejecutar un comando en un origen de datos. Puede utilizar el método **Execute** en el objeto **Connection** o el método **Open** en el objeto **Recordset**. Sin embargo, debe usar un objeto **Command** si necesita volver a usar un comando en el código o si debe pasar información detallada de parámetros con el comando. Estos escenarios se describen con más detalle posteriormente en este capítulo.


> [!NOTE]
> <P>Algunos objetos <STRONG>Command</STRONG> pueden devolver un conjunto de resultados como una secuencia binaria o un único <STRONG>registro</STRONG>, en vez de un objeto <STRONG>Recordset</STRONG>, si el proveedor admite esa posibilidad. Además, algunos objetos <STRONG>Command</STRONG> no devuelven ningún conjunto de resultados (por ejemplo, una consulta Update de SQL). Este capítulo tratará el escenario más típico: ejecutar objetos <STRONG>Command</STRONG> que devuelven resultados en un objeto <STRONG>Recordset</STRONG>. Para obtener más información acerca de los resultados devueltos en objetos <STRONG>Record</STRONG> o <STRONG>Stream</STRONG>, vea <A href="chapter-10-records-and-streams.md">Capítulo 10: Objetos Record y Stream</A>.</P>


