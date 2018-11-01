---
title: 'Capítulo 2: Obtención de datos'
TOCTitle: 'Chapter 2: Getting Data'
ms:assetid: 72d097e1-9284-cc27-fd48-e6bbb6a2a543
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249465(v=office.15)
ms:contentKeyID: 48545619
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7b045676cad97ffa1dc60f7370ec5013d4c30bdf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888079"
---
# <a name="chapter-2-getting-data"></a>Capítulo 2: Obtención de datos


**Se aplica a**: Access 2013, Office 2013

En el capítulo anterior, se presentaron cuatro operaciones principales que tenían que ver con la creación de una aplicación de ADO: obtener datos, examinar datos, editar datos y actualizar datos. Este capítulo se centrará en los detalles de los conceptos relativos a la primera operación: obtener datos.

Hay varios objetos de ADO que pueden desempeñar un rol en esta operación. Primero, hay que conectarse al origen de datos usando un objeto **Connection** de ADO (que, en ocasiones, se creará implícitamente). Después, se pasan instrucciones al origen de datos acerca de lo que se desea hacer usando un objeto **Command** de ADO (que también se puede crear de forma implícita). El resultado de pasar un comando a un origen de datos y recibir su respuesta normalmente se representará con un objeto **Recordset** de ADO.

Para obtener datos, la aplicación debe estar en comunicación con un origen de datos, como DBMS, un almacén de archivos o un archivo de texto delimitado por comas. Esta comunicación representa una *conexión* , el entorno necesario para intercambiar datos.

El modelo de objetos de ADO representa el concepto de una conexión con el objeto **Connection** (la base sobre la que se construye una parte importante de la funcionalidad de ADO). El propósito de un objeto **Connection** es:

  - Definir la información que ADO necesita para comunicarse con orígenes de datos y crear sesiones.

  - Definir las características transaccionales de la sesión.

  - Permitirle crear y ejecutar comandos en el origen de datos.

  - Proporcionar información acerca del diseño del origen de datos subyacente en forma de conjuntos de filas de esquema. Para obtener más información acerca de conjuntos de filas de esquema, vea [Método OpenSchema](openschema-method-ado.md).

En este capítulo, se tratan los temas siguientes:

  - [Creación de una conexión](making-a-connection.md)

  - [Using the Connection Object Reference (ADO)](using-the-connection-object-access.md)

  - [Using the Command Object Reference (ADO)](using-the-command-object-access.md)

  - [Adding Data to a Recordset (ADO)](adding-data-to-a-recordset.md)