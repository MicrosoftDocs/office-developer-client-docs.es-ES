---
title: Using the Connection Object (Access)
TOCTitle: Using the Connection Object
ms:assetid: e8786411-2be4-8d75-9df7-e345d5a6a7e8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250177(v=office.15)
ms:contentKeyID: 48548423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cd3e691258fe5950f40c36a1efcaed8e79810c7a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484528"
---
# <a name="using-the-connection-object-access"></a>Using the Connection Object (Access)


**Se aplica a**: Access 2013 | Office 2013

Un objeto **Connection** representa una sesión única con un origen de datos. En el caso de un sistema de base de datos cliente/servidor, puede ser equivalente a una conexión de red real con el servidor. Según la funcionalidad admitida por el proveedor, algunas colecciones, métodos o propiedades de un objeto **Connection** podrían no estar disponibles.

Antes de abrir un objeto **Connection**, debe definir parte de la información sobre el origen de datos y el tipo de conexión. El parámetro *ConnectionString* del método **Open** del objeto de **conexión** , o la propiedad **ConnectionString** en el objeto **Connection** , normalmente contiene la mayoría de esta información. Una cadena de conexión es una cadena de caracteres que define un número variable de argumentos. Los argumentos, algunos requeridos por ADO y otros específicos del proveedor, contienen información que el objeto **Connection** debe tener para realizar su trabajo. Los argumentos que componen el parámetro *ConnectionString* se separan con punto y coma (;).


> [!NOTE]
> <P>También puede especificar un nombre del origen de datos ODBC (DSN) o un archivo de vínculo de datos (UDL) en una cadena de conexión. Para obtener más información acerca de los DSN, vea Orígenes de datos en la primera parte de <EM>Referencia del programador de ODBC</EM>. Para obtener más información acerca de los UDL, vea Introducción a la API de vínculo de datos en la <EM>Referencia del programador de OLE DB</EM>.</P>


