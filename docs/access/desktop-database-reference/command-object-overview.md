---
title: Información general sobre el objeto Command
TOCTitle: Command object overview
ms:assetid: 3d6d81c4-4cf0-0c13-adb3-0c2c5934dc21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249166(v=office.15)
ms:contentKeyID: 48544346
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f2c7697d4ae8b830afb53eee10e7dd59a7dc8db4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296167"
---
# <a name="command-object-overview"></a>Información general sobre el objeto Command

**Se aplica a:** Access 2013, Office 2013

Con las colecciones, los métodos y las propiedades de un objeto **Command**, puede hacer lo siguiente:

  - Definir el texto ejecutable del comando (por ejemplo, una instrucción SQL o un procedimiento almacenado) utilizando la propiedad **CommandText**.

  - Definir consultas parametrizadas o argumentos de procedimientos almacenados utilizando objetos **Parameter** y la colección **Parameters**.

  - Ejecutar un comando y devolver un objeto **Recordset**, si procede, usando el método **Execute**.

  - Especificar el tipo de comando mediante la propiedad **CommandType** antes de la ejecución para optimizar el rendimiento.

  - Controlar si el proveedor guarda una versión preparada (o compilada) del comando antes de la ejecución mediante la propiedad **Prepared**.

  - Establecer el número de segundos que esperará un proveedor para la ejecución de un comando mediante la propiedad **CommandTimeout**.

  - Asociar una conexión abierta con un objeto **Command** estableciendo su propiedad **ActiveConnection**.

  - Establecer la propiedad **Name** para identificar el objeto **Command** como un método en el objeto **Connection** asociado.

  - Pasar un objeto **Command** a la propiedad **Source** de un **conjunto de registros** para obtener datos.

