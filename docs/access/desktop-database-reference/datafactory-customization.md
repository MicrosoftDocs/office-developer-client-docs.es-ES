---
title: Personalización de DataFactory
TOCTitle: DataFactory Customization
ms:assetid: 43cd7416-1f05-87ee-22f0-6cf0d2d1b39f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249205(v=office.15)
ms:contentKeyID: 48544511
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b805f9d6ff7a1f3b27bb5600d42cabf8fce651cd
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486015"
---
# <a name="datafactory-customization"></a>Personalización de DataFactory


**Se aplica a**: Access 2013 | Office 2013

El servicio de datos remoto (RDS) permite obtener fácilmente acceso a datos en un sistema de cliente-servidor de tres niveles. Un control de datos de cliente especifica los parámetros de las cadenas de conexión y de comandos para consultar un origen de datos remoto, o bien, los parámetros del objeto [Recordset](recordset-object-ado.md) y de la cadena de conexión para llevar a cabo una actualización.

Los parámetros se pasan a un programa de servidor, que realiza la operación de acceso a datos en el origen de datos remoto. RDS proporciona un programa de servidor predeterminado denominado objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md). El objeto **RDSServer.DataFactory** devuelve cualquier objeto **Recordset** generado por una consulta al cliente.

Sin embargo, **RDSServer.DataFactory** se limita a realizar consultas y actualizaciones. No puede realizar validaciones ni procesamientos en las cadenas de conexión o de comandos.

Con ADO, se puede especificar que **DataFactory** trabaje conjuntamente con otro tipo de programa de servidor denominado * controlador*. El controlador puede modificar las cadenas de conexión y de comandos del cliente antes de que se utilicen para obtener acceso al origen de datos. Además, el controlador puede exigir derechos de acceso, que rigen la capacidad del cliente para leer y escribir datos en el origen de datos.

Los parámetros que utiliza el controlador para modificar los derechos de acceso y parámetros de cliente se especifican en las secciones de un archivo de personalización.

Vea los temas siguientes para obtener más información sobre la personalización del objeto **DataFactory**:

  - [Introducción al archivo de personalización](understanding-the-customization-file.md)

  - [Sección Connect del archivo de personalización](customization-file-connect-section.md)

  - [Sección SQL del archivo de personalización](customization-file-sql-section.md)

  - [Sección UserList del archivo de personalización](customization-file-userlist-section.md)

  - [Sección Logs del archivo de personalización](customization-file-logs-section.md)

  - [Configuración de cliente requerida](https://msdn.microsoft.com/library/ff836356\(v=office.15\))

  - [Escribir un controlador personalizado](https://msdn.microsoft.com/library/jj249402\(v=office.15\))

