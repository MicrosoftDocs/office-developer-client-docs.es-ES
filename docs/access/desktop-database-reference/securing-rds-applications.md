---
title: Proteger aplicaciones RDS
TOCTitle: Securing RDS Applications
ms:assetid: 15f41cbb-d6e0-aca8-9c3a-97516d82c302
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248922(v=office.15)
ms:contentKeyID: 48543423
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4a531c01750117ae7abbf87e5ba4cb23daf37851
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705970"
---
# <a name="securing-rds-applications"></a>Proteger aplicaciones RDS

**Se aplica a**: Access 2013, Office 2013

## <a name="microsoft-internet-explorer-security-issues"></a>Aspectos de seguridad en Microsoft Internet Explorer

Con las nuevas mejoras de seguridad agregadas a Microsoft Internet Explorer, algunos objetos ADO y RDS están restringidos para ejecutarse sólo en un entorno de modo "seguro". Esto requiere tener en cuenta estos aspectos, incluidos las diferentes zonas, niveles de seguridad, comportamiento restrictivo, operaciones no seguras y configuraciones de seguridad personalizadas.

Para obtener más información acerca de estos aspectos, vea "ADO and RDS Security Issues in Microsoft Internet Explorer" (en inglés) en los artículos técnicos sobre Objetos de datos ActiveX (ADO).

## <a name="security-and-your-web-server"></a>Seguridad y el servidor web

Si utiliza el objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md) en el servidor web de Internet, recuerde que el hacerlo crea un riesgo potencial de seguridad. Los usuarios externos que obtienen un nombre de origen de datos (DSN) válido, un identificador de usuario y la información de contraseña podrían escribir páginas para enviar cualquier consulta a ese origen de datos. Si desea un acceso más restringido a un origen de datos, una opción consiste en eliminar el objeto **RDSServer.DataFactory** (msadcf.dll) y, en su lugar, usar objetos de negocio personalizados con consultas codificadas de forma rígida.

Para obtener más información acerca de las implicaciones de seguridad de utilizar el objeto RDSServer.DataFactory, vea el boletín de seguridad de Microsoft MS99-025 en el [sitio Web de seguridad de Microsoft](https://www.microsoft.com/en-us/security/default.aspx).

## <a name="client-impersonation-and-security"></a>Suplantación de clientes y seguridad

Si se establece la propiedad de **Autenticación de contraseña** para el servidor web IIS para la autenticación de desafío/respuesta de Windows NT (para Windows NT 4.0) o a la autenticación integrada de Windows (para Windows 2000), a continuación, se invocan los objetos de negocios en el cliente contexto de seguridad. Esto es una característica nueva en RDS 1.5 que permite la suplantación del cliente a través de HTTP. Cuando se trabaja en este modo, el inicio de sesión en el servidor web (IIS) no es anónimo pero utiliza el identificador de usuario y la contraseña que se ejecuta en el equipo cliente. Si los DSN de ODBC están configurados para usar una conexión de confianza, entonces el acceso a bases de datos, tales como SQL Server, también se produce en el contexto de seguridad del cliente. Esto solo funciona si la base de datos se encuentra en el mismo equipo que el IIS (las credenciales del cliente no se pueden transferir a otro equipo).

Por ejemplo, un cliente, Jesús Escolar, con el identificador de usuario = "JesúsE" y la contraseña = "secreto" ha iniciado una sesión en un equipo cliente. Este cliente ejecuta una aplicación basada en explorador que necesita acceso al objeto **RDSServer.DataFactory** para crear un [Recordset](recordset-object-ado.md) ejecutando una consulta SQL sobre el equipo "MiServidor" que ejecuta IIS. MiServidor, un sistema que ejecuta Windows NT Server 4.0, está configurado para usar autenticación de desafío/respuesta de Windows NT, su DSN de ODBC tiene seleccionado "Usar conexión de confianza", y el servidor también contiene el origen de datos de SQL Server. Cuando se recibe una solicitud en el servidor web, éste solicita al cliente para el identificador de usuario y la contraseña. Por lo tanto, la solicitud se registra en MiServidor como procedente de "JesúsE" / "Secret" en lugar de IUSER\_MyServer (que es el valor predeterminado cuando la autenticación de contraseña anónima está activado). Análogamente, al iniciar sesión en el servidor SQL Server, también se usa "JesúsE"/"secreto".

En consecuencia, el modo de autenticación desafío/respuesta de Windows NT para IIS permite que se creen páginas HTML sin que se pida explícitamente al usuario la información de identificador y contraseña necesaria para iniciar una sesión en la base de datos. Si se utilizara el método de autenticación básica de IIS, también se requeriría esto.

## <a name="password-authentication"></a>Autenticación de contraseña

RDS se puede comunicar con un servidor web IIS que se ejecuta en uno de los tres modos de autenticación de contraseña: anónimo, básico o autenticación de desafío/respuesta de NT (denominado autenticación integrada de Windows en Windows 2000). Estas opciones definen cómo un servidor web controla el acceso a través de él, como la necesidad de que un equipo cliente tenga privilegios de acceso explícito en el servidor web de NT.

